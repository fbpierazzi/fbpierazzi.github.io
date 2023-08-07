---
layout: post
title:  Introduction to Python multiprocessing
date: 2019-03-02 21:01:00
description: This post gives an introduction to the use of Python multiprocessing
tags: tutorial python multiprocessing
categories: tutorial
toc:
  sidebar: left

giscus_comments: false
---


In the past few years, I have been frequently asked how to easily parallelize in Python. It seems that people is often confused by the documentation online and are not sure which solution to go for. So, I decided to write a blog post about a minimum working example of `multiprocessing`,  which should be pretty easy and straightforward to use for a lot of situations.

## Requirements

We need to import a couple of libraries: `multiprocessing` and (optionally) `tqdm`. In `Python3` (stable at 3.7 at the time of writing), the `multiprocessing` library is natively included; this library  allows you to define a function that you can spawn with different parameters on separate processes (it does not perform multithreading).


```python
import multiprocessing
```

The second library I would recommend is `tqdm`, which is not required but it has made my coding life so much easier since I started using it. This library creates a smart progress bar when it is used to wrap an iterable object (e.g., a list in a for cycle). To install it, just run `pip3 install tqdm --upgrade`. We will see how to use `tqdm` in its very basic form, but I recommend you to have a look at its [official documentation](https://github.com/tqdm/tqdm) for more advanced usage.


```python
from tqdm import tqdm
```

## Function to parallelize

First, let us define the function that you would like to parallelize. You often have to rethink the logic of your program, but if you have some independent cpu-intensive operations (e.g., training, parsing of long files, preprocessing), chances are there is a way to rethink your code to create a single, independent function that will run on a separate process.  

Let us define here a function, namely `function_to_parallelize`, that just takes two parameters as input and sums them. In this function you can actually do any sort of processing, as long as it is dependent solely on the input
parameters. It is relevant to observe that you must use a **single input parameter** for this function. This is not a problem, as this single parameter can be a dictionary containing many parameters that you can unpack. For the purpose of this tutorial, I am using `param1` and `param2` as parameter names, but of course you can use any name and number of parameters (as long as you embed them within a single `params` dictionary).

Of course, parameter names need to match the names in the list you pass to the `multiprocessing` library (as we will see in a bit).


```python
def function_to_parallelize(params):
    param1 = params['param1']
    param2 = params['param2']

    # I would recommend to use a dictionary
    # so you can create richer results
    # to return to the main process
    result = {}

    # Do your processing with param1 and param2.
    # Here, you can do any sort of processing, and
    # it will be executed independently on a separate process
    # on a separate (virtual) core of your CPU
    result['sum'] = param1+param2

    return result
```

## Parallelization

To perform the actual parallelization, we need to define the number of (virtual) cores that we want to use, and we need to define a-priori the list of parameter combinations that we are going to spawn in parallel.

---

You can check how many (virtual) cores you have by using the command line tools `htop` or `glances`. I would recommend always leaving a couple of cores free, to avoid your machine to go into thrashing with the experts.


```python
# This chooses all cores except 2, unless there are only two or less cores.
NCPU = multiprocessing.cpu_count() - 2 if multiprocessing.cpu_count() > 2 else 1
```

Then, you need to define the parameters that each process will receive as input. You have to basically create a list of parameters. They can be in any number and quantity, and I usually prefer to define them as a `generator` of a `dict comprehension` for brevity.

```python
# Create a Python generator containing a set comprehension of parameters.
# You need to identify what you would like to parallelize on, and then build
# the parameters dictionary
X_values = [10,22,35,4,532,12,42,53,23]
params = ({
    'param1': x,
    'param2': 15
} for x in X_values)

```

**Note**: I recommend *not* to pass big structures as parameters (e.g., large matrices) because it can create a lot of inter-process communication that can cause severe delays or memory errors (e.g., use all the RAM in the machine). When possible, use [Python generators](https://docs.python.org/3/tutorial/classes.html#generators) instead of Python lists (as shown above); in this way, the parameters list will not be pre-allocated all at once, but instead it will be allocated while iterating through the cycle.

---

Now we are ready to start the actual multiprocessing. We create a `Pool` of processes that is managed by the `multiprocessing` library itself. Then, Python allows us to iterate through the Pool and get back the results. The function `p.imap` returns the results in order.


```python
with multiprocessing.Pool(processes=NCPU) as p:    

    # If you use "generators" for the params list,  
    # tqdm will not know the total length of the array
    # (required for the progress bar),
    # so you have to specify it explicitly,
    # or derive it from your params.
    MAX_COUNT = len(X_values)

    for res in tqdm(p.imap(function_to_parallelize, params),total=MAX_COUNT):
        if res is not None:
            print(res['sum'])

```

      0%|          | 0/9 [00:00<?, ?it/s]


## Troubleshooting

1. **Machine becomes slow and unresponsive after using multiprocessing**

    I have noticed that sometimes the `multiprocessing` library, for very large batches of experiments, leaves some operating system reources in usage---hence, the virtual machine in which you may be running your experiments could become slow and unresponsive after many days of experiments. It may be a problem of the infrastructure I am using to do the experiments, but I have seen this also happening to other colleagues that use other infrastructures. My best recommendation so far is to **restart the VM** if it becomes very slow after using the `multiprocessing` library. I know this is a kind of "Have you tried to turn it off and on?" solution, but it has worked so far. I will dig deeper into this, or if you have any insight please do not hesitate to leave a comment below.

2. **Each iteration is too slow/Too much RAM is being used**

    Double check that you are using a Python `generator` (and not a `list`) for the list of parameters (the object named `params` in the above code). Also, if you are passing big data structures (e.g., huge feature matrices), remember that that RAM will be used for each process spawned. So, I recommend to do slicing (if possible) before passing big matrices as parameters if you do not need all the rows/columns for your processing.

## Final Considerations

I hope you have found this tutorial useful. Many people go for complex solutions for parallelizing Python code, but in most cases I found out that this easy solution is quite as effective. I have put the full code of this minimum working example on GitHub, [here](https://github.com/fbpierazzi/mwe-python-multiprocessing). If you have any suggestion to improve this tutorial or any parts that are not clear, just leave a comment!

I would be happy to hear if you have other suggestions to perform multiprocessing in a more effective way.
