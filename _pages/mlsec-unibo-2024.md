---
layout: page
permalink: /courses/mlsec-unibo-2024/
title: Ph.D. Course at UniBo (2024)
description: 
nav: false
toc:
  sidebar: left
---


April 8th--12th, 2024\\
Duration: 20 hours

### Risk Assessment of Machine Learning for Cybersecurity

Machine Learning (ML) has shown incredible success in many applications, and this trend was  followed also by cybersecurity to deal with an increasing number of threats in network intrusion and malware detection. However, using ML increases also attack surface, and opens the way to attackers to evade detection systems. It is then important to understand how to assess the risks and the attack surface of ML models.

**Objectives**: This course will provide you with an overview of the challenges and trends in assessing risks and robustness of applying machine learning in cybersecurity, i.e., contexts that consider the presence of an adversary, and that require modification of complex objects (e.g., software). 

**Outcome**: An understanding of fundamental challenges of applying machine learning in adversarial settings with evolving scenarios, with case studies and labs on the malware detection domain.

The indicative outline of the course is as follows:

* [5h] **Introduction to Machine Learning (ML) for Cybersecurity**
	* Basics of ML for Computer Vision
	* Feature engineering in cybersecurity: Android malware, network traffic, PDFs, Windows PEs
	* Strenghts and weaknesses of abstract representations, semantic gaps
	* Challenges specific to machine learning for cybersecurity
	* Python Lab on Android malware classification, and performance metrics

* [5h] **Concept Drift (Distribution Shift)**
	* Measuring the decay in the Android, Windows and PDF domains
	* Reasoning about mitigations: retraining, active learning, online learning, classification by rejection, continuous learning, ability not to forget
	* Python Lab on Android malware classification in presence of time evolution

* [4h] **Realistic Deployments**
	* Recommendations for real-world deployments of Machine Learning for cybersecurity
	* Bridging the gap between academia and industry
	* Python Lab on the impact of sampling bias in evaluations

* [6h] **Adversarial Machine Learning**
	* Threat models and brief history of adversarial ML 
	* Gradient-based attacks in computer vision
	* Inverse feature mapping problem in cybersecurity
	* Reformulation of input-space attacks with real-world modifications
	* Defense directions (e.g., certified robustness, adversarial training, robust optimization)
	* Python Lab on adversarial machine learning on Android malware classification

The Python Labs will follow the guidelines at [this link](https://github.com/isneslab/mlsec-labs).

### Registration

To participate, you need to complete [this registration form](https://forms.gle/dy8FBAKXG9VP1nCo9). In-person places are on a first-come first-served basis. 


### Required skills

The course offers a 3-hour introductory part that will provide you with all the basics and context required to understand the challenges. Do not get scared by the word 'cybersecurity' in the title: we will use cybersecurity as a scenario that has specific constraints that make machine learning very challenging. Yet, we will discuss all the existing trends and solutions to these problems that are the focus of extensive research from both the security and ML communities. 

Required: 

* Computer Science background
* Software engineering basics
* Networking basics
* Basic Python programming skills

Preferred (but not required):

* Machine Learning basics
* Cybersecurity



### Timetable

| Date                       | Time &nbsp; &nbsp; | Location                                        |
|----------------------------|-------|-------------------------------------------------|
| Monday, April 8th, 2024    | 14-18 | Aula VII piano Matematica                       |
| Tuesday, April 9th, 2024   | 09-13  | Aula Bodoniana 5 - Via San Donato 19/2, ingresso da Ristorante Le Salentine |
| Wednesday, April 10th, 2024 | 14-18 | Aula Bodoniana 5                                |
| Thursday, April 11th, 2024  | 14-18 | Aula Arzelà Matematica                          |
| Friday, April 12th, 2024    | 09-13  | Location TBC                                    |
|----------------------------|-------|-------------------------------------------------|

<br/>

### Assessment (Optional)

This course offers an optional exam, for students who opt-in to do it (e.g., for getting credits in their Ph.D. programme). 

The assessment requires to write an extended abstract (min 1000-max 1500 chars, spaces included) that summarizes how your research relates to (and can be improved) by one paper of your choice from the References list below. The abstract should contain:
 1. Statement of a problem in your own research that is related to your chosen paper
 2. Idea for a possible novel solution that integrates the chosen paper and your research
 3. Novelty with respect to the state of the art

Submit your extended abstract **by May 15th, 2024** via this form: _Link TBC_

Assessment criteria: 
- Demonstrating understanding of the chosen paper content and topic
- Ability to position your own research within the context of robust machine learning and security
- Clarity of presentation 
- Correct use of technical terms seen in this short course
- Quality of the idea proposed

You will also receive a personalized feedback on your abstract. 


### Lecturer Biography

Dr. Fabio Pierazzi is a Senior Lecturer (Associate Professor) in Computer Science and Deputy Head of the Cybersecurity group at the Department of Informatics of King's College London, and affiliated with UCL's Systems Security Research Lab (S2Lab). His research interests are at the intersection of systems security and machine learning, with a particular emphasis on settings in which attackers adapt quickly to new defenses (i.e., high non-stationarity, adaptive attackers). Previously, he obtained his Ph.D. in Computer Science at University of Modena, Italy (2014–2017), he visited University of Maryland, College Park, USA (2016), and he was a Post-Doctoral Research Associate at Royal Holloway, University of London (2017–2019). Home page: [https://fabio.pierazzi.com](https://fabio.pierazzi.com)

### References

See [advice on reviewing literature for systems security](http://localhost:8080/blog/2021/literature-review-systems-security/).

Best Practices for MLSec
* Arp et al., "[Dos and Don'ts of Machine Learning in Computer Security](dodo-mlsec.org)", USENIX Security Symposium, 2022 (Distinguished Paper Award)

Adversarial ML: Evasion
* Carlini and Wagner, [Towards Evaluating the Robustness of Neural Networks](https://arxiv.org/abs/1608.04644), IEEE Symposium on Security & Privacy, 2016 (Best Paper Award)
* Pierazzi et al., "[Intriguing Properties of Adversarial ML Attacks in the Problem Space](https://fabio.pierazzi.com/papers/pierazzi_intriguing.pdf)", IEEE Symposium on Security & Privacy, 2022

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


Distribution Shift
- Pendlebury et al., [TESSERACT: Eliminating Experimental Bias in Malware Classification across Space and Time](https://fabio.pierazzi.com/papers/tesseract.pdf), USENIX Security Symposium, 2019
- Chen et al., [Continuous learning for malware detection](https://arxiv.org/abs/2302.04332), arXiv, 2023
- Barbero et al., "[Transcending TRANSCEND: Revisiting Malware Classification in the Presence of Concept Drift](https://arxiv.org/abs/2010.03856)", IEEE Symposium on Security & Privacy, 2022


Other MLSec Applications
- Pearce et al., [Asleep at the Keyboard? Assessing the Security of GitHub Copilot's Code Contributions](https://arxiv.org/abs/2108.09293), IEEE S&P 2022 (Distinguished Paper Award)
- Mirsky et al., "[Kitsune: An Ensemble of Autoencoders for Online Network Intrusion Detection](https://www.ndss-symposium.org/wp-content/uploads/2018/02/ndss2018_03A-3_Mirsky_paper.pdf)", NDSS 2018
- Quiring et al., "[Misleading Authorship Attribution of Source Code using Adversarial Learning](https://www.usenix.org/system/files/sec19-quiring.pdf)", USENIX Security Symposium, 2019

Socio-technical MLSec
- Aonzo et al., "[Humans vs. Machine in Malware Classification](https://www.usenix.org/system/files/sec23summer_241-aonzo-prepub.pdf)", USENIX Security Symposium, 2023

Malware Detection
- Arp et al., [Drebin: Effective and explainable detection of android malware in your pocket.](https://mlsec.org/docs/2014-ndss.pdf), NDSS, 2014

<br/>

### Acknowledgments 

This PhD course was supported by project SERICS (PE00000014) under the MUR National Recovery and Resilience Plan funded by the European Union - NextGenerationEU.