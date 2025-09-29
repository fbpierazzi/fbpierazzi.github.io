---
layout: page
permalink: /resources/literature-review
title: How to Review Literature in Systems Security
description: Advice on how to do literature review and related work.
tags: tutorial writing
categories: tutorial
nav: false
nav_order: 5
toc:
  sidebar: left
featured: true
giscus_comments: false
---

Are you a BSc or MSc student embarking on your dissertation, or an early-stage Ph.D. researcher feeling uncertain about how to approach a literature review in systems security? If so, this post is for you. Here, I’ll share practical advice and guidance to help you navigate the process of reviewing the literature and positioning your work within the current state of the art in systems security research. 

**Friendly Note:** Everything in this post comes from my own experience (which is always growing and changing!), and reflects my personal take on reviewing literature in Systems Security & AI. My goal is simply to share some tips and starting points for students who are beginning their first big research project and want to get a handle on how to approach a literature review. If you have thoughts, questions, or suggestions, If you have any feedback, I'd be more than happy to challenge my views, and revise my recommendations! 

---

## Getting Started with Literature Reviews

Over the years as an academic supervisor, I’ve noticed that many students can feel intimidated or even a bit overwhelmed when it comes to conducting a literature review. This is completely understandable: the field of systems security is expanding rapidly, with more and more high-quality papers published every year, making it challenging to find a clear route at first. Each area within Computer Science has its own venues and conventions, and learning how to navigate and connect these can seem daunting. However, developing this skill is fundamental for your growth as a researcher, and this guide is here to help you take those first steps, especially within the context of systems security.

During my own undergraduate dissertation, I really struggled to understand what it meant to write a "Related Work" section. I got confused because---to me---it looked very similar to the "Introduction" section. (Side note: [this article](https://www.cs.columbia.edu/~hgs/etc/intro-style.html) is my go-to guide for writing excellent introductions!). 
Moreover, I felt intimidated to approach and read "research papers" written by experts, as I thought you needed to be a "genius" to read one of those.

In reality, a BSc or MSc in Computer Science provides you with all the basic tools you need to start reading research papers. Focus on papers within your area of expertise, and remember that understanding them takes time and persistence: you probably won’t grasp everything on your first read, and that’s completely normal. It’s also important to develop the skill of navigating the literature, so you can gradually build the background knowledge needed for more advanced topics. The good news is that, although research papers can be technical, they are usually written and organized clearly, with the goal of being accessible to a technical audience.


---

## Publication Quality

Determining the quality of publications is a hard problem that requires expertise and in-depth critical assessment of what you are reading. However, you may use some criteria to prioritize your literature review and identify papers which are more relevant to your research.

### Publication venues

In academia, most research articles are published through **peer review**. This means that, before a paper is published, it is evaluated by other experts in the field to check its originality, quality, and significance. The reviewers provide feedback and recommend whether the paper should be published, revised, or rejected. This process helps ensure that published research is reliable and meets the standards of the community. For your literature review, focusing on peer-reviewed papers is a good way to find trustworthy and relevant work.

Therefore, the **publication venue** is a useful initial indicator of quality. While even top venues can publish some weaker papers (and vice versa), prestigious venues generally feature higher-quality work. As a student, focusing on papers from these venues can help you navigate the vast literature more confidently.

Academic research is mainly shared through two types of venues: **conferences** and **journals**. In systems security (and in computer science,  in general) people usually prefer conferences. I do not know the exact reasons, but two that come to mind are: (1) conferences tend to publish work more quickly, which is really helpful in a fast-changing field like ours; (2) conferences offer a great opportunity for networking and getting to know other people working in your field.

In the remainder, I do provide some pointers for the most relevant conferences and journals within my field. The list does not mean to be exhaustive, and you may integrate this with other sources, such as:

- [Influental Security Papers](https://www.mlsec.org/topnotch/index.html), by Prof. Konrad Rieck, TU Berlin
- [System Security Circus](https://www.s3.eurecom.fr/~balzarot/security-circus/), by Prof. Davide Balzarotti, S3@Eurecom


### Academic Conferences

Academic conferences typically have one edition per year in which authors meet together to discuss and present the works published in that year's proceedings. Now it has become more frequent to have multiple submission deadlines throughout the years, but each conference remains with a yearly edition in which works are presented.

In systems security, there are typically four main academic conferences which are commonly considered **top-tier conferences** by the community:

- [IEEE Symposium on Security & Privacy (S&P, Oakland)](https://www.ieee-security.org/TC/SP2026/)
- [USENIX Security Symposium (Sec)](https://www.usenix.org/conference/usenixsecurity26)
- [ACM Computers and Communication Security (CCS)](https://www.sigsac.org/ccs/CCS2025/)
- [The Network and Distributed System Security (NDSS) Symposium](https://www.ndss-symposium.org/ndss2026/#)

Apart from the "top four", other highly reputable venues in Systems Security include (but are not limited to):

- [IEEE European Symposium on Security and Privacy (EuroS&P)](http://www.ieee-security.org/TC/EuroSP2021/)
- [IEEE Conference on Safe and Trusthorthy Machine Learning (SaTML)](https://satml.org)
- [USENIX WOOT Conference on Offensive Technologies](https://www.usenix.org/conference/woot25)
- [Annual Computer Security Applications Conference (ACSAC)](https://www.acsac.org)
- [International Symposium on Research in Attacks, Intrusions and Defenses (RAID)](https://raid2021.org)
- [ACM ASIA Conference on Computer and Communications Security (ASIACCS)](https://asiaccs2022.conferenceservice.jp/)
- [Conference on Detection of Intrusions and Malware & Vulnerability Assessment (DIMVA)](https://dimva2021.campus.ciencias.ulisboa.pt)
- [European Symposium on Research in Computer Security (ESORICS)](https://esorics2021.athene-center.de)
- [ACM Conference on Data and Application Security and Privacy (CODASPY)](http://www.codaspy.org/2022/)


There are also **top workshops** on specific sub-topics, such as: [AISec](https://aisec.cc), [DLSP](https://www.ieee-security.org/TC/SP2021/SPW2021/dls_website/), which are often co-located with top conferences. Workshops typically publish preliminary results or interesting new ideas, which maybe do not have yet a sufficiently large experimental evaluation or fully fledged theory behind them.

Sometimes work in systems security can also be published in closely-related venues but more focused on Data Mining, ML, AI. For example, [ACM Web Conference](https://www2022.thewebconf.org) (previously known as "WWW") which is a first-tier conference in data mining has a Security & Privacy track. Other top tier venues in data mining, AI and ML include: **ICML**, **ICLR**, **WSDM**, **NeurIPS**, **IJCAI**, **AAAI**.

### Academic Journals

Journals in systems security are typically used for extensions or consolidation of research results of a conference version, but often host also original research works.

Here is an indicative list of some reputable journals in systems security:

- [ACM Transactions on Privacy and Security (TOPS; ex-TISSEC)](https://dl.acm.org/journal/tops)
- [IEEE Transactions on Information Forensics and Security (TIFS)](https://ieeexplore.ieee.org/xpl/RecentIssue.jsp?punumber=10206)
- [IEEE Transactions on Dependable and Security Computing (TDSC)](https://ieeexplore.ieee.org/xpl/RecentIssue.jsp?punumber=8858)
- [Journal of Computer Security](https://www.iospress.com/catalog/journals/journal-of-computer-security)
- [Elsevier Computers & Security](https://www.journals.elsevier.com/computers-and-security)

Typically, ACM and IEEE journals with "Transactions" in their name tend to be the more prestigious ones, but there are also other highly reputable journals which build a reputation for themselves.

In the field of AI and ML, some very good journals include also [Pattern Recognition](https://www.journals.elsevier.com/pattern-recognition), and [JMLR](https://www.jmlr.org), just to mention a couple.


### Number of citations

As humans, we like to measure things. Many systems refer to **number of citations** as a proxy for quality and impact. While this correlation of citation and impact is not always true (e.g., some papers may have high citation count because they have a title containing popular keywords),  papers with high citations may be very influential papers that heavily influenced research in a certain field.

Typically, you should also look out for "**Test of Time Awards**", which are given to influental papers after about 10 years of their publications (e.g., see [rules for ToT at NDSS](https://www.ndss-symposium.org/ndss-test-of-time-award/nominations/#:~:text=The%20NDSS%20Test%20of%20Time,Time%20Award%20committee%20for%20consideration.)).

### Technical reports, white papers and pre-prints

Industry frequently publishes technical reports or white papers on some new, emerging technology. Sometimes, also academics do it (calling them "technical reports"). While technical reports can undoubtedly be informative, it is important to note that they are **not peer-reviewed**.

Hence, even when you find paper pre-prints on websites such as [arXiv](https://arxiv.org), be sure to double-check if they are published somewhere.

Sometimes the authors' name, reputation and affiliation is used as proxy for the quality, but you always need to be more cautious if has not been peer-reviewed, and to critically assess the work itself. It is important to remember, as **Richard Feynman** said:

> "If [a theory] disagrees with experiments, it's wrong. And that simple statement is the key to science. It doesn't make a difference how beautiful your guess is, it doesn't make a difference  how smart you are who made the guess, or what his name is: if it disagrees with the experiment, it's wrong. That's all there is to it." -  [Richard Feynman](https://youtu.be/LIxvQMhttq4)


There can be a variety of valid reasons for which a work isn't published yet (maybe it is currently under review). Nevertheless, it is important that you keep in mind that accepted work has been peer-reviewed by experts, and hence you should generally hold it to a higher standard than technical reports.

### Publication years

Keep in mind that **research is incremental**: findings at time _t_ may be disproved at time _t+1_. We always build on the shoulders of giants, but it is a neverending process. While it is fundamental not to forget prior research, it is important to check that your references are up to date with the current state of the art. Even 5 years in the field of computer security can be a long time!

---

## How to find related works

I try to summarize some useful tips and tricks to find relevant research papers while conducting a literature review:

- **Paper search engines**: it may sound trivial, but I think [Google Scholar](https://scholar.google.com) is your best search engine at the moment for finding research papers. If you do not have access to scholar, also [dblp](https://dblp.org) is a good place to look into.
- **Read "Related Work" sections of papers**: If you find one paper that is very close to what you are doing, look at the papers they cite. This is often a good source of information, and provides
- **Look at the "Cited by" field on Google Scholar**: If you click on the "Cited by" field on Google Scholar, you will also find a list of papers who cited that one, typically sorted by citation number. It can be useful to track more recent advancements of the state of the art.
you interesting references to look into.
- **Surveys** and **Systemization of Knowledge (SoK)** papers are also a great place where to understand better the state of the art in a more condensed way. Sometimes also **Reading Lists** are published by prominent researchers in a field, such as the [Adversarial Machine Learning Reading List
](https://nicholas.carlini.com/writing/2018/adversarial-machine-learning-reading-list.html) from Nicholas Carlini. Here are a couple of useful resources to search for SoKs:
  - [Systematization of Knowledge Papers](https://oaklandsok.github.io)
  - [Shujun Li's Online Bibliography of SoK papers](https://www.hooklee.com/Research/SoK/SoK.html)
- **Search academics profiles**: If a researcher has published a top paper on a certain systems security topic, if you look at their research profile (e.g., personal home page, dblp, or Google Scholar), you may find other interesting works in the topic.
- **"Sessions" of recent security conferences**: Conferences are held once per year, and their "program" is typically divided into "sessions" of a certain topic. For example, if you are doing research in Web Security, a conference may have a "Web Security" session in its program, which can be useful to find relevant works in that area at the moment.
- **Use LLMs (Large Language Models) as assistants, but verify their output**: Tools like ChatGPT or other LLMs can help you brainstorm keywords, summarize papers, or suggest related works. However, always double-check any references or summaries they provide, as LLMs can sometimes generate inaccurate information or "hallucinate" sources that do not exist. Use them as a starting point, not a substitute for reading and critical assessment.
- **Be creative in your keywords search**: Keywords and trends change over time, even for the same topic. Unfortunately---to the best of my knowledge---most paper search engines rely mostly on paper titles, not much on its content. Hence, you need to be smart in your keywords search, since some papers may be using different terminologies. For example, back in 2016, when I started doing research in Android malware analysis, I looked up for "Android clustering" on Google Scholar, or "mobile malware clustering", and nothing was coming out of my searches. I initially thought no one else did it, until I found out that people was mostly framing it as "malware family identification"!

### "There is no work on this topic"

Students often come back to me saying they did not find anything on a certain topic. Well, there can be two possibilities:

- (a) You truly have a brand new idea that no one has worked on before. That's fantastic!
- (b) You just haven't found the related work yet.

Unfortunately, most of the time, it's option (b). 

Sometimes, you need to be creative in your literature review as well. Let me give a concrete example from personal experience. Maybe you are doing a research on identifying a new type of network attacks that came out earlier this year. But in most cases, even new attacks rely on component previously proposed in old versions. For example, if you want to identify attacker communications within internal networks, there has been a lot of research on "computer worms". Or maybe even research on graphs and social network may be relevant with respect to the algorithms you are using.

Fun anecdote: I always discourage my students to claim "_We are the first to do X_"; because, statistically, there is always at least another paper who tried something very similar before.

---

## Advice on reading research papers

When you first approach a literature review, you will find tens or hundreds of papers related to your work. It can be quite intimidating, and you may feel overwhelmed by the sheer amount of papers that pile up in your "to-read" folder. Indeed, reading thoroughly all of the papers published in a field would be a quite challenging task, if not impossible.

I do have the following recommendations and advice:

- **Be kind on yourself**. First of all, accept that you cannot possibly read everything thoroughly. Moreover, **understanding is an incremental process**. You will not understand 100% of a paper on a first read. At least, I don't. It takes time. The more you read about a certain topic, or re-read certain sections, the more you understand about it. I myself still go back and re-read some seminal papers, and always learn something new from a refreshed perspective. You will continuously grow as a researcher and as a professional, and so will your ability to capture connections and meanings in what you read.
- **Read abstracts before choosing which papers to dive into**. Abstracts are there for a reason: to give you an idea of what the paper is contributing to the state of the art. Reading abstracts from many papers should give you an idea of what are the relevant challenges tackled by people, and a small intuition on how they managed to overcome prior works. Of course, abstracts are not sufficient to fully understand a work, but even reading one hundred abstracts becomes a manageable task, versus reading in detail one hundred papers papers. While you are still looking at the literature at a high level, it is also a good practice to skim papers by reading **introduction**, **conclusions**, and going over main results and figures. This is just to identify the works which are most relevant with your research, and which you should read more thoroughly.
- **Talk to colleagues/supervisors**. People will have advice on which papers to read on a certain topic, especially if they're experts in that sub-area. You can also ask feedback of whether a certain paper you found could be considered relevant or not for your project. 
- **Try to (re)implement small ideas**. It is often the case that you may get stuck into "reading mode", and blocked by the high amount of information. If you try to implement or replicate someone else's approach, see it as a great learning opportunity which will also benefit your literature review: you will start understanding better how other people have solved certain issues, and what are important questions that need answers. You may also identify missing bits in the literature.
- **Reading groups** are also a valuable option to learn more about existing papers. In reading groups, each person reads and summarizes a recent paper to the other members (people rotate this responsibility). This helps scaling, networking and an opportunity to work on presentation skills.

---

## Positioning your work within the state of the art

In your research dissertation or paper, your goal is not just to provide a "summary" of related work. Instead, you need to critically analyze existing literature to identify research gaps, and **position** your own work within the state of the art.

In simple terms, "the state of the art" refers to the most current and advanced knowledge, methods, and developments in your research topic. For example, in malware detection the state of the art is represented by the best-performing detection approach published to date. By understanding the state of the art most closely related to your approach, you can clearly show how your work fits in, what makes it new, and why it matters.

In other words, positioning implies that you "compare and contrast" your proposed approach with existing literature, and the state of the art most related to your work. This is often hard to do, and requires proper reflection and thinking. 

Here is some advice I always refer to, as a starting point:

> [...] "At a high level what are the differences in what you are doing, and what others have done? Keep this at a high level, you can refer to a future section where specific details and differences will be given. But it is important for the reader to know at a high level, what is new about this work compared to other work in the area." - [Jim Kurose (UMass), Writing a Good Introduction](https://www.cs.columbia.edu/~hgs/etc/intro-style.html)

In this previous quote, Jim Kurose is talking about the "Introduction" section, where you should just give a high-level intuition of what you are doing that is novel. The "Related Work" section is entirely dedicated to diving deeper into that comparison, and answering in more details many questions, such as:

- Is your approach relying on previous techniques?
- Are you solving a new problem? Are there other works solving similar problems?
- What makes your approach better than the "state of the art"? Is it faster? Is it more efficient? Is it more reliable?

Hence, it is not sufficient to just "list" existing literature, but you really need to explicitly write how each work is related to yours, and where you are improving the state of the art.

The "Related Work" section need to be easily accessible to readers, as there is a risk of listing and comparing against a huge amount of papers and losing the "big picture". So, I find it often useful for clarify to **identify two/three macro-areas of related research** and summarize my contributions with respect to works in each of those areas. You find this pattern in most top papers as well.

---

## Final Considerations

To wrap up, this guide has aimed to demystify the process of conducting a literature review in systems security by sharing practical strategies and highlighting important considerations. Remember: focus on reputable peer-reviewed venues, use abstracts and introductions to filter papers, seek advice from colleagues, and don’t be afraid to revisit or (re)implement ideas as you learn. Most importantly, your goal is not just to summarize prior work, but to critically position your own research within the broader landscape.

These tips are just a starting point. Your own approach will evolve as you gain experience. If you have additional insights or suggestions for navigating the literature, I’d love to hear your thoughts!

---

#### Changelog

- v1.0: Nov 16, 2021: First version published.
- v1.0.1: Nov 17, 2021: Fixed System Security Circus link; added Carlini adversarial reading list
- v2.0: Sep 8, 2025: this is a major update to the article, including fixing link, new venues that became popular in the past four years, and I moved it as a "resource" rather than a dated blog post, because it is meant to support students in the long term. This version was also prepared with the support of Claude and Cursor. 