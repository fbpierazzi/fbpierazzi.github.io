---
layout: page
permalink: /courses/mlsec-unimo-2025/
title: Ph.D. Course at UniMo (2025)
description: 
nav: false
toc:
  sidebar: left
---


July 7th--11th, 2025\\
Duration: 20 hours

## Trends and Challenges for the Security of Machine Learning Systems

Machine Learning (ML) has shown incredible success in many applications, and this trend was followed also by cybersecurity to deal with an increasing number of threats in network intrusion and malware detection. However, using ML increases also attack surface, and opens the way to attackers to evade detection systems. It is then important to understand how to assess the risks and the attack surface of ML models.

While Machine learning is going to be a main focus, we will focus in general on _hostile environments_ in which attackers aim to compromise systems to take some advantage out of it (e.g., compromising the availability, integrity or confidentiality of a Machine Learning system).

**Objectives:** This course will provide you with an overview of the challenges and trends in assessing risks and robustness of applying machine learning in contexts such as cybersecurity that consider the presence of an adversary, and that may require modifications of complex applications.

**Outcome:** An understanding of fundamental challenges of applying machine learning in adversarial settings with evolving scenarios, with case studies and labs applied on the malware detection domain.


## Timetable


| Date                       | Time &nbsp; &nbsp; &nbsp; &nbsp; | Location                                        |
|----------------------------|-------|-------------------------------------------------|
| Monday, July 7th, 2025    | 09-13, 14-16 | Sala Riunioni Primo Piano - DIEF MO27                       |
| Tuesday, July 8th, 2025   | 09-13, 14-16  | Sala Riunioni Primo Piano - DIEF MO27 |
| Wednesday, July 9th, 2025 | 09-13 | Sala Riunioni Primo Piano - DIEF MO27                                |
| Thursday, July 10th, 2024  | 14-18 | Sala Riunioni Primo Piano - DIEF MO27                          |
| Friday, July 11th, 2024    | 09-13  | Sala Riunioni Primo Piano - DIEF MO27               |
|----------------------------|-------|-------------------------------------------------|

## Syllabus 

The indicative outline of the course is as follows:

- [4h] **Introduction to Machine Learning (ML) and Cybersecurity**
  - Overview of Machine Learning Pipeline for Cybersecurity tasks 
  - Feature engineering in cybersecurity: Android malware, network traffic, PDFs, Windows PEs
  - Strengths and weaknesses of abstract representations, semantic gaps
  - Challenges specific to machine learning in hostile environments with adversaries
  - Python Lab on Android malware classification task, and performance metrics

- [5h] **Concept Drift (Dataset Shift)**
  - Performance decay due to distribution shifts, and types of distribution shifts
  - Sources of dataset shifts
  - Reasoning about mitigations: retraining, active learning, online learning, classification by rejection, continual learning, few-shot learning
  - Python Lab on Android malware classification in presence of time evolution

- [7h] **Adversarial Machine Learning**
  - Threat models and brief history of Adversarial ML
  - Gradient-based attacks in computer vision
  - Inverse feature mapping problem in other domains (e.g., cybersecurity)
  - Reformulation of input-space attacks with real-world modifications
  - Defense directions (e.g., adversarial training, robust optimization)
  - Security of Generative AI
  - Python Lab on adversarial machine learning on Android malware classification

- [4h] **Realistic Deployments**
  - Recommendations for real-world deployments of Machine Learning for cybersecurity
  - Bridging the gap between academia and industry
  - Python Lab on the impact of sampling bias in evaluations

The Python Labs will follow the guidelines at [this link](https://github.com/isneslab/mlsec-labs).

## Required skills

The course offers a 3-hour introductory part that will provide you with all the basics and context required to understand the challenges. We will consider primarily cybersecurity as a scenario that has specific constraints that make machine learning very challenging to be applied successfully. Yet, we will discuss all the existing trends and solutions to these problems that are the focus of extensive research from both the security and ML communities.

Required:
- Computer Science background
- Software engineering basics
- Basic Python programming skills

Strongly recommended:
- Machine Learning (at least the basics)

Preferred (but not required):
- Cybersecurity (e.g., malware detection, software security, security principles such as CIA triad)

## Assessment (Optional)

This course offers an optional exam, for students who opt-in to do it (e.g., for getting credits in their Ph.D. programme).

The assessment requires to write an extended abstract (min 1000-max 1500 chars, spaces included) that summarizes how your research relates to (and can be improved) by one paper of your choice from the References list below. The abstract should contain:

  1. Statement of a problem in your own research that is related to your chosen paper
  2. Idea for a possible novel solution that integrates the chosen paper and your research
  3. Novelty with respect to the state of the art

Assessment criteria:
- Demonstrating understanding of the chosen paper content and topic
- Ability to position your own research within the context of robust machine learning and security
- Clarity of presentation
- Correct use of technical terms seen in this short course
- Quality of the idea proposed

You will also receive a personalized feedback on your abstract.

### Lecturer Biography

Fabio Pierazzi is Associat Professor in Computer Science at UCL. His research interests are at the intersection of systems security and machine learning, with a particular emphasis on settings in which attackers adapt quickly to new defenses (i.e., high non-stationarity, adaptive attackers). Previously, he obtained his Ph.D. in Computer Science at University of Modena, Italy (2014–2017), he visited University of Maryland, College Park, USA (2016), and he was a Post-Doctoral Research Associate at Royal Holloway, University of London (2017–2019), and (Senior) Lecturer at King's College London (2019--2024). Home page: [https://fabio.pierazzi.com](https://fabio.pierazzi.com)

### References

See [advice on reviewing literature for systems security](../../blog/2021/literature-review-systems-security/).

Best Practices for MLSec
* Arp et al., "[Dos and Don'ts of Machine Learning in Computer Security](dodo-mlsec.org)", USENIX Security Symposium, 2022 (Distinguished Paper Award)

Adversarial ML: Evasion
* Carlini and Wagner, [Towards Evaluating the Robustness of Neural Networks](https://arxiv.org/abs/1608.04644), IEEE Symposium on Security & Privacy, 2016 (Best Paper Award)
* Pierazzi et al., "[Intriguing Properties of Adversarial ML Attacks in the Problem Space](https://fabio.pierazzi.com/papers/pierazzi_intriguing.pdf)", IEEE Symposium on Security & Privacy, 2022
* Athalye et al. "[Obfuscated gradients give a false sense of security: Circumventing defenses to adversarial examples](https://proceedings.mlr.press/v80/athalye18a/athalye18a.pdf)", ICML, 2018.
- Quiring et al., "[Misleading Authorship Attribution of Source Code using Adversarial Learning](https://www.usenix.org/system/files/sec19-quiring.pdf)", USENIX Security Symposium, 2019

Adversarial ML: Backdoor
* Yang et al., "[Jigsaw Puzzle: Selective Backdoor Attack to Subvert Malware Classifiers](https://kclpure.kcl.ac.uk/portal/files/204793925/IEEESP23_Jigsaw_Puzzle.pdf)", IEEE Symposium on Security & Privacy, 2023

Adversarial ML: Poisoning
* Shan et al., "[Poison forensics: Traceback of data poisoning attacks in neural networks](https://www.usenix.org/conference/usenixsecurity22/presentation/shan)." USENIX Security Symposium, 2022

Adversarial ML: General and Defenses
- Tramer et al., [On Adaptive Attacks to Adversarial Example Defenses](https://arxiv.org/abs/2002.08347), NeurIPS, 2020
- Biggio and Roli, [Wild Patterns: Ten Years After the Rise of Adversarial Machine Learning](https://arxiv.org/abs/1712.03141), Pattern Recognition, 2018
- De Cristofaro, [A Critical Overview of Privacy in Machine Learning](https://emilianodc.com/PAPERS/IEEESP2021.pdf), IEEE Security & Privacy Magazine, 2021
- Papers cited by Nicholas Carlini in his [Adversarial ML Reading List](https://nicholas.carlini.com/writing/2018/adversarial-machine-learning-reading-list.html)
- Demontis et al., "[Yes, machine learning can be more secure! A case study on android malware detection](https://arxiv.org/abs/1704.08996)" IEEE Transactions on Dependable and Secure Computing (TDSC), 2017

Socio-technical MLSec
- Aonzo et al., "[Humans vs. Machine in Malware Classification](https://www.usenix.org/system/files/sec23summer_241-aonzo-prepub.pdf)", USENIX Security Symposium, 2023

Malware Detection
- Arp et al., [Drebin: Effective and explainable detection of android malware in your pocket.](https://mlsec.org/docs/2014-ndss.pdf), NDSS, 2014

<br/>