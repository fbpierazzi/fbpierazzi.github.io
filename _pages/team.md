---
layout: page
permalink: /team/
title: team
description: 
nav: true
nav_order: 4
---

To explore vacancies and opportunities, see [this page](/opportunities/).

<style>
  .team-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(200px, 1fr)); gap: 1.5rem; margin: 1.25rem 0 3rem; }
  .team-card {
    text-align: center; padding: 2rem 1.25rem 1.5rem; border-radius: 1rem;
    background: var(--global-card-bg-color);
    border: 1px solid var(--global-divider-color);
    box-shadow: 0 1px 2px rgba(0, 0, 0, 0.04), 0 4px 16px rgba(0, 0, 0, 0.06);
    transition: transform 0.2s ease, box-shadow 0.2s ease;
  }
  .team-card:hover { transform: translateY(-4px); box-shadow: 0 2px 4px rgba(0, 0, 0, 0.06), 0 12px 28px rgba(0, 0, 0, 0.12); }
  .team-photo {
    width: 112px; height: 112px; border-radius: 50%; object-fit: cover; object-position: center 30%;
    display: block; margin: 0 auto 1.1rem;
    box-shadow: 0 0 0 4px var(--global-card-bg-color), 0 0 0 6px var(--global-theme-color);
  }
  .team-initials {
    display: flex; align-items: center; justify-content: center;
    background: var(--global-theme-color);
    background: linear-gradient(135deg, var(--global-theme-color), color-mix(in srgb, var(--global-theme-color) 55%, #000));
    color: #fff; font-size: 2.2rem; font-weight: 300; letter-spacing: 0.06em;
  }
  .team-name { font-size: 1.05rem; font-weight: 600; line-height: 1.3; }
  .team-name a { color: inherit; text-decoration: none; }
  .team-name a:hover { color: var(--global-theme-color); }
  .team-name a i { font-size: 0.65em; margin-left: 0.3em; vertical-align: 0.15em; opacity: 0.5; }
  .team-years { margin-top: 0.5rem; }
  .team-years span {
    display: inline-block; padding: 0.15rem 0.65rem; border-radius: 999px;
    font-size: 0.75rem; font-weight: 500; letter-spacing: 0.02em;
    color: var(--global-theme-color);
    background: var(--global-divider-color);
    background: color-mix(in srgb, var(--global-theme-color) 12%, transparent);
  }
  .team-topic { font-size: 0.875rem; margin-top: 0.85rem; line-height: 1.45; color: var(--global-text-color-light); }
  .team-note {
    font-size: 0.75rem; font-style: italic; line-height: 1.4; color: var(--global-text-color-light); opacity: 0.85;
    margin-top: 0.75rem; padding-top: 0.65rem; border-top: 1px dashed var(--global-divider-color);
  }
</style>

{% for group in site.data.team.current %}

## {{ group.group }}

<div class="team-grid">
  {%- for m in group.members -%}
  <div class="team-card">
    {%- if m.image -%}
    <img class="team-photo" src="{{ m.image | prepend: '/assets/img/' | relative_url }}" alt="{{ m.name }}" loading="lazy">
    {%- else -%}
    {%- assign name_parts = m.name | split: ' ' -%}
    <div class="team-photo team-initials" aria-hidden="true">{{ name_parts.first | slice: 0 }}{{ name_parts.last | slice: 0 }}</div>
    {%- endif -%}
    <div class="team-name">{% if m.url %}<a href="{{ m.url }}">{{ m.name }}<i class="fa-solid fa-arrow-up-right-from-square" aria-hidden="true"></i></a>{% else %}{{ m.name }}{% endif %}</div>
    <div class="team-years"><span>{{ m.years }}</span></div>
    {%- if m.topic -%}<div class="team-topic">{{ m.topic | markdownify | remove: '<p>' | remove: '</p>' | strip }}</div>{%- endif -%}
    {%- if m.note -%}<div class="team-note">{{ m.note | markdownify | remove: '<p>' | remove: '</p>' | strip }}</div>{%- endif -%}
  </div>
  {%- endfor -%}
</div>

{% endfor %}

***

## Past Members: Ph.D. Alumni

- **[Theo Chow](https://www.linkedin.com/in/theo-chow-07519b17b/)** (2021--2026)
    - Ph.D. Thesis title: "Addressing Dataset Bias in Android Malware Classifiers under Distribution Shift"
    - First job after graduation: ML Researcher and Engineer @ Aeris-UK
- **[Jacopo Cortellazzi](https://www.linkedin.com/in/jacopocortellazzi/)** (2019--2024)
    - Ph.D. Thesis title: "Robustness of Machine Learning-based Malware Detection Models" 
    - First job after graduation: AI Security Researcher @ Apple
- **[Marcus Zeliang Kan](https://www.linkedin.com/in/markkan945/)** (2019--2024)
    - Ph.D. Thesis title: "Evaluating and Mitigating Concept Drift in Machine Learning Security Tasks"
    - First job after graduation: AI Security Researcher @ HiddenLayer
- **[Feargus Pendlebury](https://www.linkedin.com/in/feargus-pendlebury/)** (2017--2021), as _Second Supervisor_ 
    - Ph.D. Thesis title: "Machine Learning for Security in Hostile Environments" 
    - First job after graduation: Software Engineer @ Meta

## Past Members: PostDocs

- **[Mario Lilli](https://www.linkedin.com/in/mario-lilli-95236a208/)** (2024--2026), [KTP](https://www.ukri.org/councils/innovate-uk/guidance-for-applicants/guidance-for-specific-funds/knowledge-transfer-partnership-guidance/) Research Associate on Formal Methods for Security at King's College London (co-supervised with [Prof. Luca Viganò](https://www.kcl.ac.uk/people/luca-vigano) and [ControlPlane](https://control-plane.io/))
    - First job after position: Senior Security Researcher @ Darktrace

## Past Members: Research Visitors

- Silvio Russo (May 2025, 6 months), _University of Bologna, Italy_
- Jenjira Jaimunk (April 2025, 2 months), _Chiang Mai University, Thailand_
- Alessandro Sanna (Mar 2024, 3 months), _University of Cagliari, Italy_
- Hamid Bostani (Oct 2023, 6 months), _Radboud University, Netherlands_
- Marcello Maugeri (Oct 2023, 6 months), _University of Catania, Italy_
- Feng Wei (Oct 2023, 6 months), _University at Buffalo, USA_
- Mario D'Onghia (May 2023, 6 months), _Politecnico of Milan, Italy_
- Malik Al-Essa (Mar 2023, 6 months), _University of Bari, Italy_
- Giuseppina Andresini (2021), _University of Bari, Italy_
- Dr. Daniel Arp (Sep 2022, 6 months), _TU Berlin, Germany_
- Ilias Tsingenopoulos (Jan 2023, 3 months), _KU Leuven, Belgium_
- Shae McFadden, _King's College London, UK_

## Past Members: BSc Research Internships

- Jeevan Jutla (2023), _King's College London, UK_
- Shae McFadden (2023), _King's College London, UK_
- Adil Farooq (2022), _Georgia Tech, USA_
- Zhuo Ying Jiang Li (2022), _King's College London, UK_
- Harivallabha Rangarajan (2020--2021), _BITS Pilani, Hyderabad Campus, India_
- Federico Barbero (2018), _King's College London, UK_
- Zakir Singh (2019--2021), _King's College London, UK_
- Cliona Mulligan (2020), _King's College London, UK_
- Piotr Kurek (2021), _King's College London, UK_
- Emiliyana Tsanova (2021), _King's College London, UK_
- Priya Pillaipakkam Madapusi (2021), _King's College London, UK_
