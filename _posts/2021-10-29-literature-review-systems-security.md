---
layout: post
title:  How to Review Literature in Systems Security
date: 2021-10-29 21:00:00
description: Advices on how to do literature review and related work in the field of computer security.
tags: tutorial writing
categories: tutorial
toc:
  sidebar: left

featured: false
giscus_comments: false
---

This post is targeted mostly for BSc/MSc students doing their dissertations, or early career Ph.D. students who need support in understanding how to conduct a proper literature review in systems security, and to position your work within the state of the art.

**Disclaimer**: Please note that this post represents my own personal opinion (which also evolves over time as I learn more :-) ), based on my experience so far as a researcher working in Systems Security & AI. My intent is solely to provide initial recommendations to early career research students tackling their first large project who want to understand better how to conduct a literature review. If you have any feedback, I'd be more than happy to challenge my views and integrate and revise my recommendations!

---

In these years as a faculty member and academic supervisor, I see students struggle more and more with understanding how to conduct a literature review. This is understandable: the field has been growing extensively, and more and more papers get published in reputable venues, so it is hard to create a "mental compass" to orient yourself in this sea of literature. Even within Computer Science, every discipline has different venues and understanding how to look for related works requires some effort and experience. Indeed, this guide is meant mostly for Systems Security.

During my undergraduate dissertation, I really struggled to understand what it meant to write a "Related Work" section. I got confused because---to me---it looked very similar to the "Introduction" section. Moreover, I felt intimidated to approach and read "research papers" written by experts, as I thought you needed to be a "genius" to read one of those.

In practice, a BSc/MSc in Computer Science should give you all the ingredients you need to first approach a research paper. You need to read within your area of expertise, and be patient and persistent: you will not understand everything after one read, and you need to be patient to really understand concepts sometimes. Another important skill is to learn how to navigate the literature, so you can build the foundational knowledge you need to understand more advanced topics. Nevertheless, good research papers---while technical---are also written and structured in an extremely clear way, as they are meant to be understood by a technical audience.



---

## Publication Quality

Determining the quality of publications is a hard problem that requires expertise and in-depth critical assessment of what you are reading. However, you may use some criteria to prioritize your literature review and identify papers which are more relevant to your research.

### Publication venues

In academia, research articles are mostly published via **peer-review**. In **academic conferences**, a program committee of experts reviews the paper independently and determines whether its originality, rigor and significance is sufficient to be published at a certain venue. In **academic journals**, there is a committee of "associate editors" which then invite external experts to coordinate the review process.  

Hence, **publication venue** can be typically used as initial proxies of quality.

Keep in mind there could still be bad papers published in good venues (and viceversa), but indicatively venues that are quite selective tend to contain work of higher quality. I find this could be useful especially when you start as a student to read research paper and you feel "lost in the sea".

My list does not intend to be exhaustive, but just indicative.

Two highly recommended reads are the following:

- [Influental Security Papers](https://www.sec.cs.tu-bs.de/~konrieck/topnotch/), by Konrad Rieck, TU Braunschweig
- [System Security Circus](https://www.s3.eurecom.fr/~balzarot/notes/top4_2020/), by Davide Balzarotti, S3@Eurecom


#### Conferences

Academic conferences typically have one edition per year in which authors meet together to discuss and present the works published in that year's proceedings. Now it has become more frequent to have multiple submission deadlines throughout the years, but each conference remains with a yearly edition in which works are presented.

In Systems Security, there are typically four main academic conferences which are commonly considered **top-tier conferences** by the community:

- [IEEE Symposium on Security & Privacy (S&P, Oakland)](https://www.ieee-security.org/TC/SP2022/)
- [USENIX Security Symposium (Sec)](https://www.usenix.org/conference/usenixsecurity22)
- [ACM Computers and Communication Security (CCS)](https://www.sigsac.org/ccs/CCS2021/)
- [The Network and Distributed System Security (NDSS) Symposium](https://www.ndss-symposium.org/ndss2022/#)

Apart from the "top four", other highly reputable venues in Systems Security include (but are not limited to):

- [IEEE European Symposium on Security and Privacy (EuroS&P)](http://www.ieee-security.org/TC/EuroSP2021/)
- [Annual Computer Security Applications Conference (ACSAC)](https://www.acsac.org)
- [ACM ASIA Conference on Computer and Communications Security (ASIACCS)](https://asiaccs2022.conferenceservice.jp/)
- [International Symposium on Research in Attacks, Intrusions and Defenses (RAID)](https://raid2021.org)
- [Conference on Detection of Intrusions and Malware & Vulnerability Assessment (DIMVA)](https://dimva2021.campus.ciencias.ulisboa.pt)
- [European Symposium on Research in Computer Security (ESORICS)](https://esorics2021.athene-center.de)
- [ACM Conference on Data and Application Security and Privacy (CODASPY)](http://www.codaspy.org/2022/)

There are also **top workshops** on specific sub-topics, such as: [ScAInet](https://www.usenix.org/conference/scainet20), [AISec](https://aisec.cc), [w00t](https://www.ieee-security.org/TC/SP2021/SPW2021/WOOT21/), [DLS](https://www.ieee-security.org/TC/SP2021/SPW2021/dls_website/), which are often co-located with top conferences. Workshops typically publish preliminary results or interesting new ideas, which maybe do not have yet a sufficiently large experimental evaluation or fully fledged theory behind them.

Sometimes work in Systems Security can also be published in closely-related venues but more focused on Data Mining, ML, AI. For example, [The Web Conference ACM](https://www2022.thewebconf.org) which is a first-tier conference in data mining has a Security & Privacy track. Other top tier venues in data mining, AI and ML include: **ICML**, **ICLR**, **WSDM**, **NeurIPS**, **IJCAI**, **AAAI**.

#### Journals

Journals in Systems Security are typically used for extensions or consolidation of research results of a conference version, but often host also original research works.

Here is a rough list of reputable journals in Systems Security:

- [ACM Transactions on Privacy and Security (TOPS; ex-TISSEC)](https://dl.acm.org/journal/tops)
- [IEEE Transactions on Information Forensics and Security (TIFS)](https://ieeexplore.ieee.org/xpl/RecentIssue.jsp?punumber=10206)
- [IEEE Transactions on Dependable and Security Computing (TDSC)](https://ieeexplore.ieee.org/xpl/RecentIssue.jsp?punumber=8858)
- [Journal of Computer Security](https://www.iospress.com/catalog/journals/journal-of-computer-security)
- [Elsevier Computers & Security](https://www.journals.elsevier.com/computers-and-security)

Typically, ACM and IEEE journals with the name "Transactions" in it tend to be the more prestigious ones, but there are also other highly reputable journals which build a reputation for themselves.

In the field of AI and ML, some very good journals are also [Pattern Recognition](https://www.journals.elsevier.com/pattern-recognition), and [JMLR](https://www.jmlr.org).


### Number of citations

As humans, we like to measure things. Many systems refer to **number of citations** as a proxy for quality and impact. While this is not necessarily true, papers with high number of citations may be either false positives (e.g., papers cited just because people searched for "computer worm" and cited the first result on scholar), or actually be very influential papers that heavily influenced research in a certain field.

Typically, you should also look out for "**Test of Time Awards**", which are given to influental papers typically after 10 years of their publications.

### Technical reports, white papers and pre-prints

Industry frequently publishes technical reports or white papers on some technology. Sometimes, also academics do it (although they mostly call them "technical reports"). While technical reports can undoubtedly be informative, it is important to note that they are **not peer-reviewed**.

Hence, even when you find paper pre-prints on websites such as [arXiv](https://arxiv.org), be sure to double-check if they are published somewhere.

Sometimes the authors' name, reputation and affiliation is used as proxy for the quality, but you always need to be more cautious if has not been peer-reviewed, and to critically assess the work itself. It is important to remember, as **Richard Feynman** said:

> "If [a theory] disagrees with experiments, it's wrong. And that simple statement is the key to science. It doesn't make a difference how beautiful your guess is, it doesn't make a difference  how smart you are who made the guess, or what his name is: if it disagrees with the experiment, it's wrong. That's all there is to it."

> [Richard Feynman](https://youtu.be/LIxvQMhttq4)


There can be a variety of valid reasons for which a work isn't published yet (maybe it is currently under review). Nevertheless, it is important that you keep in mind that accepted work has been peer-reviewed by experts, and hence you should generally hold it to a higher standard than technical reports.

### Publication years

Keep in mind that **research is incremental**: findings at time _t_ may be disproved at time _t+1_. We always build on the shoulders of giants, but it is a neverending process. While it is fundamental not to forget prior research, it is important to check that your references are up to date with the current state of the art. Even 5 years in the field of computer security are a lot of time.

---

## How to find related works

I try to summarize some useful tips and tricks to find relevant works in your field:

- **Paper search engines**: it may sound trivial, but I think [Google Scholar](https://scholar.google.com) is your best search engine at the moment for finding research papers. If you do not have access to scholar, also [dblp](https://dblp.org) is a good place to look into.
- **Read "Related Work" sections**: If you find one paper that is very close to what you are doing, look at the papers they cite. This is often a good source of information, and provides
- **Look at the "Cited by" field on Google Scholar**: If you click on the "Cited by" field on Google Scholar, you will also find a list of papers who cited that one, typically sorted by citation number. It can be useful to track more recent advancements of the state of the art.
you interesting references to look into.
- **Surveys** and **Systemization of Knowledge (SoK)** papers are also a great place where to understand better the state of the art in a more condensed way. Sometimes also **Reading Lists** are published by prominent researchers in a field, such as the [Adversarial Machine Learning Reading List
](https://nicholas.carlini.com/writing/2018/adversarial-machine-learning-reading-list.html) from Nicholas Carlini. 
- **Search researchers profiles**: If a researcher has published a top paper on a certain systems security topic, if you look at their research profile (e.g., personal home page, dblp, or Google Scholar), you may find other interesting works in the topic.
- **Sessions of recent security conferences**: Conferences are held once per year, and their presentation program is typically divided into "sessions" of a certain topic. For example, if you are doing research in Web Security, a conference may have a "Web Security" session in its program, which can be useful to find relevant works in that area at the moment.
- **Be creative in your keywords search**: Keywords and trends change over time, even for the same topic. Unfortunately---to the best of my knowledge---most paper search engines rely mostly on paper titles, not much on its content. Hence, you need to be smart in your keywords search, since some papers may be using different terminologies. For example, back in 2016, when I started doing research in Android malware analysis, I looked up for "Android clustering" on Google Scholar, or "mobile malware clustering", and nothing was coming out of my searches. I initially thought no one else did it, until I found out that people was mostly framing it as "malware family identification"!

### "There is no work on this topic"

Students often come back to me saying they did not find anything on a certain topic. Well, there can be two situations:

- You had a novel idea for opening a new research field that no one else had before. Amazing!
- You did not "yet" find anything related.

Unfortunately, it is often the second case.

Sometimes you need to be creative in your literature review as well. Let me give an example. Maybe you are doing a research on identifying a new type of network attacks that came out earlier this year. But in most cases, even new attacks rely on component previously proposed in old versions. For example, if you want to identify attacker communications within internal networks, there has been a lot of research on "computer worms". Or maybe even research on graphs and social network may be relevant with respect to the algorithms you are using.

---

## Advice on reading research papers

When you first approach a literature review, you will find tens or hundreds of papers related to your work. It can be quite intimidating, and you may feel overwhelmed by the sheer amount of papers that pile up in your "to-read" folder. Indeed, reading thoroughly all of the papers published in a field would be a quite challenging task, if not impossible.

I do have the following advices:

- **Be kind on yourself**. First of all, accept that you cannot possibly read everything thoroughly. Moreover, **understanding is an incremental process**. You will not understand 100% of a paper on a first read. At least, I don't. It takes time. The more you read about a certain topic, or re-read certain sections, the more you understand about it. I myself still go back and re-read some seminal papers, and always learn something new from a refreshed perspective. You will continuously grow as a researcher and as a professional, and so will your ability to capture connections and meanings in what you read.
- **Read abstracts before choosing which papers to dive into**. Abstracts are there for a reason: to give you an idea of what the paper is contributing to the state of the art. Reading abstracts from many papers should give you an idea of what are the relevant challenges tackled by people, and a small intuition on how they managed to overcome prior works. Of course, abstracts are not sufficient to fully understand a work, but even reading one hundred abstracts becomes a manageable task, versus reading in detail one hundred papers papers. While you are still looking at the literature at a high level, it is also a good practice to skim papers by reading **introduction**, **conclusions**, and going over main results and figures. This is just to identify the works which are most relevant with your research, and which you should read more thoroughly.
- **Talk to colleagues/supervisors**. People will have advice on which papers to read on a certain topic, especially if they're experts in that sub-area. You can also ask feedback of whether a certain paper you found could be considered relevant or not for your project.
- **Try to (re)implement small ideas**. It is often the case that you may get stuck into "reading mode", and blocked by the high amount of information. If you try to implement or replicate someone else's approach, see it as a great learning opportunity which will also benefit your literature review: you will start understanding better how other people have solved certain issues, and what are important questions that need answers. You may also identify missing bits in the literature.
- **Reading groups** are an option where each person reads and summarizes a recent paper to the other members of the reading group. This helps scaling, and improves networking and presentation skills.

---

## Positioning your work

Understanding how to **position** your work within the state of the art is hard.

In your research dissertation/paper, you do not only need to provide a "summary" of the related work. Positioning implies that you "compare and contrast" your proposed approach with existing literature.

Here is some advice I always refer to as a starting point:

> [...] "At a high level what are the differences in what you are doing, and what others have done? Keep this at a high level, you can refer to a future section where specific details and differences will be given. But it is important for the reader to know at a high level, what is new about this work compared to other work in the area."

> [Jim Kurose (UMass), Writing a Good Introduction](https://www.cs.columbia.edu/~hgs/etc/intro-style.html)

In the previous quote, the author is talking about the Introduction section, where you should just give a high-level intuition of what you are doing that is novel. The Related Work section is dedicated to diving deeper into that comparison, and answering in more details many questions, such as:

- Is your approach relying on previous techniques?
- Are you solving a new problem? Are there other works solving similar problems?
- What makes your approach better than the state of the art? Is it faster? Is it more efficient? Is it more reliable?

Hence, it is not sufficient to just "list" existing literature, but you really need to explicitly write how each work is related to yours, and where you are improving the state of the art.

The "Related Work" section need to be easily accessible to readers, as there is a risk of listing and comparing against a huge amount of papers and losing the "big picture". So, I find it often useful for clarify to **identify two/three macro-areas of related research** and summarize my contributions with respect to works in each of those areas.



---

## Final Considerations

I hope you have found this post useful.

This is not meant to be an exhaustive list of relevant publication venues, and tips for conducting a literature review. In general, you should see this just as an initial advice to help you navigate more confidently within the state of the art of Systems Security, upon venturing in it for the first time.

I would be very happy to hear what are your experiences and if you have any other relevant advice into conducting literature review.

---

#### Changelog


- v1.0: Nov 16, 2021
- v1.0.1: Nov 17, 2021 - _Fixed System Security Circus link; added Carlini adversarial reading list_
