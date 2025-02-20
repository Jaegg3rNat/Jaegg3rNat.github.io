---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---
    For a complete detailed CV click here

{% include base_path %}

Education
======
* Ph.D in Theoretical Physics, UERJ, Brazil, 2024 (Sandwich in CASUS-HZDR, Germany)
* M.S. in Physics, UERJ, Brazil, 2020
* B.S. in Physics, UERJ, Brazil, 2018

Work experience
======
* 2025- on going: Postdoctoral Reasercher
  * IFISC - Spain
  * Duties includes: Reasearch stochastic dynamics, pattern formation
  * Supervisor: Emilio Hernandez-Garcia
  
Skills
======
* Renormalization Group 
* Numerical Simulations
  * Python
  * Molecular Dynamics
  * Deterministic and Stochastic Integration of PDE's
* Languages
  * English
  * Portuguese
  * Spanish
  * German

Publications
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
Talks
======
  <ul>{% for post in site.talks reversed %}
    {% include archive-single-talk-cv.html  %}
  {% endfor %}</ul>
  
Teaching
======
  <ul>{% for post in site.teaching reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  