---
layout: page
permalink: /resources/meetings
title: Preparing Slides for Research Progress Meetings
description: Advice on how to do prepare slides for progress meetings.
tags: tutorial writing
categories: tutorial
nav: false
nav_order: 5
toc:
  sidebar: left
featured: true
giscus_comments: false
---

Preparing slides for research meetings is an important skill for all students, whether you are working on your BSc/MSc dissertation or pursuing a PhD. In Computer Science, it is common that during a project there are results to be discussed, and it is important to learn how to present them clearly, and in realtion to the project objectives. 

This article offers some general advice on how to prepare effective meeting slides, based on my experience supervising a range of student projects, at BSc/MSc/PhD level, primarily in the area of AI and Systems Security. 

Please treat this as a flexible guide: take what is most useful for your own style and project. Even if your supervisors prefer not having slides, you may see this as a useful guide for structuring your updates more effectively.  

### Preliminaries

Before we start, I would like to clarify a few aspects that are closely related to presenting updates and progress in research meetings.  

* **Think about your audience.**  Slides are intended to deliver a message to a certain audience. For example, _Teaching Slides_ will be probably reviewed by undergraduates to study, hence they may be text-heavy; _Conference Presentation Slides_ need to be very catchy and visually appealing, working as a "sort of" trailer of your own paper and research. Instead, research meetings slides have the primary objective of updating your team (including supervisor or any collaborators) on the progress on your project, and asking feedback and advice on any potential blockers you have encountered. Keep this objective in mind, as you read through this article, because it is important to remember that "each presentation has its audience", and need to be re-targeted accordingly.

* **A note on independence.** While you work towards your BSc/MSc/PhD dissertations, it is often emphasize that the work you conduct needs to demonstrate research independence. Oftentimes, student mistake this as working in isolation, completing as much as possible without ever "bothering" the supervisors/collaborators, and try to come to them with a finished product. Instead, at least in my view, real independence means being able to communicate your progress, questions, and blockers clearly and efficiently, so that you can make the most of the time you have with your supervisors and collaborators. It means also always try to be resourceful to resolve the problems yourself first, but known also when you should ask for advice, and how to ask the right questions. Hence, I hope this guide will also provide valuable feedback for you. 

---

### Meeting Slides Guidelines

A well-prepared set of meeting slides typically includes:
* A brief recap of what was discussed in previous meetings, to help everyone get back up to speed.
* A summary of the project’s main objective, to keep the discussion focused.
* An update on any progress (e.g., new results), or any blockers; and what you plan as next steps. 

The next sections provide more detailed advice on what to present. Not all sections apply at all times (e.g., literature review may only occur in certain stages of the project). 

#### Meeting Slides: Opening 

A common "mistake" is to skip the opening slides of the project, and dive deep into a technical challenge you had, or some results you got.  Your supervisor/collaborators are (very likely) following a vast amount of projects at once, and hence having some opening slides to refocus the scope of participants is quite crucial. Otherwise people may struggle to remember exactly where you left, even if your last meeting was a week ago. And it is important to highlight that these slides can take up just one or two minutes of time, but it can be invaluable to bring everyone up to speed.

In the opening slides, you need to integrate: 

* **Remind project title and objectives.** This should be a concise list of the main objectives of the project. If you are working towards a research publication, you may list the current target list of "novel contributions" that you are proposing. This may change over time, as you learn new things, so it is important to keep a "sketch" for everyone to review at each progress meeting.

* **Points to be discussed.** You may also add a few, concise bullet points describing the main experiments/things you want to discuss during this meeting. This is particularly important if time is tight, and you want to discuss many things. This helps also setting the pace for how many things you want to go over. 

* **Review of "Next Steps" from previous meeting(s)**. If this is your first meeting, ignore this point. As you will see later, it is important to have a target set of next steps that everyone agrees on by the end of the meeting; and it is important to pick it back up to see what items have been completed, and whether any item may no longer be relevant. 

#### Meeting Slides: Literature Review

At some key steps fo the project (e.g., the beginning), you may be asked to provide a summary of relevant related literature. This is important to establish the novelty of your own proposal, as well as your understanding of the state of the art. I would recommend you also to review my [other article on literature review](/resources/literature-review), to see how to conduct it. Here, we focus on "presenting" a literature review. 

For very closely-related papers (doing something very very similar to what you are doing), you should identify the 2-3 most related and have one slide per paper, each slide including: 
* Paper objective
* Main intuition of their proposal
* Experimental configurations used / dataset evaluated
* How it relates to your own project

Remember to report a full citation of the key papers mentioned, such as in this format, at the bottom of slides:
> Tsingenopoulos et al., " The Adaptive Arms Race: Redefining Robustness in AI Security" , RAID, 2025

which is: first author, title, venue, year. To keep the presentations more lightweight, you may also decide to just report venue/year, such as [RAID25] (at least to contextualize where it was published), and then have references in an ending slide. 

Then, for a more generic litearture review, a slide with key bullet points identified the main related areas, and how they relate to you, would be more appropriate. 

#### Meeting Slides: Results 

Most of the progress meetings, at least in my area, are about reporting and discussing new experimental results. In this context, while presenting any results, it is crucial to:
* **Explain experimental settings in detail.** Here you may re-cycle slides from previous meetings if it is an experiment we already discussed. It is important to define dataset splits, feature space used. 
* **Clarify objective of the experiment.** What is the hypothesis we were testing with this experiment? If the research question is lost, maybe the experiment was ill-posed. This needs to re-connect with the project objectives in the opening slides. If your supervisor or collaborators ask for an experiment, but you do not understand the objective, feel free to challenge it during a meeting, with reasoning and argumentation.  
* **Include your own observations on the results.** Sometimes it is easy to get lost in the details, and come to the meetings with many, many results, plots, tables, but no clear idea on how to interpret them. You should always try and reflect before the meeting and come up with some key bullet points of what the results may entail, and not wait for your supervisor/collaborators to infer it. 

* **Make sure figures are polished**. Make sure that any plot in your presentation has the following:
  * Make sure the plot is clearly readable. If you need help to make it readable, ask colleagues or the supervisor beforehand. Capture also to any feedback provided during your presentations, on how to make plots more readable.
  * Make sure that X-label and Y-label are present.
  * Makre sure that colors are distinguishable (e.g., color-blind friendly), and different lines/bars have different styles.
  * Make sure there is a legend for the different lines. Each configuration name in the legend is clearly explained.
  * If using performance metrics such as F1-Score, make sure Y-axis is normalized between 0 and 1 (for comparing plots fairly). 
  * Each plot needs to have a clear title in the slides. This is to clearly connect a plot with a certain experimental settings.

If you are using matplotlib to make your plots, you may consider also using this function to make the plots more readable and adjust the size of the fonts:
```python
def set_fontsize(fontsize):
    matplotlib.rcParams['pdf.fonttype'] = 42
    matplotlib.rcParams['ps.fonttype']  = 42
    font = {
        'family' : 'serif',
        'weight' : 'normal',
        'size' : fontsize
    }
    matplotlib.rc('font', **font)
    matplotlib.rc('text', usetex=True)
```

#### Meeting Slides: Questions and Blockers

This is one of the key parts of meeting slides. This is when you have opportunities to ask clarifications or advice to your supervisor and collaborators on any blockers you may have encountered. 

While it is difficult to provide generic advice on this part, make sure that:
* Use a few, concise bullet points to identify the major roadblockers or things that need to be decided. This is fundamental for promoting healthy conversations and brainstorming. 
* Plan time in the presentation to arrive on this part. Oftentimes meetings run out of time, and you should make sure to inform your supervisor if you have a major road blocker. 
* Try to be proactive: clarify what you attempted so far to solve the issue, and, if feasible, provide options on how this could be resolved.

The clarify of this part is very co-dependent with the clarity of all the other slides you presented, especially the "opening" and "results" slides.


#### Meeting Slides: Next Steps

At the end of each meeting, it is always useful to share what you plan to do as next steps on the project. Again, just a few bullet points. If new experiments are proposed, it should be clear what are the experimental hypotheses that need to be tested. 

While sharing "next steps" feel hard, it will also allow to get feedback on what your supervisor advises to prioritize, or whether they think an experiment may not indeed be needed. Preparing this part of the slides can save a lot of time along the way, and it will be a good review point at the beginning of the next meeting. 

### General Style Notes

Finally, some general mixed considerations about style of the meeting slides. The main objective here is to deliver updates clearly, not to present the project to an external audience. Hence, readability and clarity should be prioritized over everything else.

Here are some important notes to consider: 

- **Add slide numbers** to every slide. This makes it easier to reference and discuss specific slides during the meeting.
- **Use large, readable fonts** (minimum 18-24pt) so that text is clear even when slides are shared via screen or projected.
- **Avoid fancy templates that are harder to read**. Nowadays, presentation tools (e.g., PowerPoint) offer automated template suggestions to make the slides "look nicer", but they often compromise readability (using low-contrast color combinations, or putting the text too small or in odd places).
- **Be wise about quantity of text:** Limit the amount of text per slide, so that the slide remains clear. Use concise bullet points, and avoid long sequences of text (unless necessary for discussion: e.g., asking feedback on a theorem).
- **Ensure all figures and tables are legible:** Axis labels, legends, and data points should be easily readable at a glance. Figures should not be blurred. Tables should not be too small. 
- **Reflect on using descriptive slide titles** to help the team quickly grasp the main points of each slide.
