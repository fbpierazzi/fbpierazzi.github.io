---
layout: page
title: "XAdv: Robust Explanations for Malware Detection"
description: "EPSRC New Investigator Award"
# img: assets/img/12.jpg
importance: 1
category: grants
related_publications: chow2023driftforensics, pierazzi2020intriguing, pendlebury2019tesseract, kan2024tesseract
---

## Project Information

* Project Lead: Dr. Fabio Pierazzi
* Dates: October 2023--September 2026
* Grant Reference Number: [EP/X015971/1](https://gow.epsrc.ukri.org/NGBOViewGrant.aspx?GrantRef=EP/X015971/1)


## Project Background

Malware (short for malicious software) refers to any software that perform malicious activities, such as stealing information (e.g., spyware) and damaging systems (e.g., ransomware). Malware authors constantly update their attack strategies to evade detection of antivirus systems, and automatically generate multiple variants of the same malware that are harder to recognize than the original. Traditional malware detection methods relying on manually defined patterns (e.g., sequences of bytes) are time consuming and error prone. Hence, academic and industry researchers have started exploring how Machine Learning (ML) can help in detecting new, unseen malware types.

In this context, explaining ML decisions is fundamental for security analysts to verify correctness of a certain decision, and develop patches and remediations faster. However, it has been shown that attackers can induce arbitrary, wrong explanations in ML systems; this is achieved by carefully modifying a few bytes of their malware.

## Project Objectives

The EPSRC project XAdv (X for explanation, and Adv for adversarial robustness), aims to design robust explanations for malware detection, i.e., explanations of model decisions which are easy to understand and visualize for security analysts (to support faster verification of maliciousness, and development of patches), and which are trustworthy and reliable even in presence of malware evolution over time and evasive malware authors.

Robustness of explanations will be evaluated from two main perspectives: concept drift (i.e., malware evolution over time), and adversarial ML (i.e., ML-aware attackers, who carefully craft malicious samples to evade detection systems).

Moreover, this project will explore how robust explanations can be used to automatically adapt ML-based malware detection models to new threats over time (e.g., into novel active learning strategies), as well as to integrate domain knowledge from security analysts' feedback from robust explanations to improve detection accuracy.





