---
layout: about
title: about
permalink: /
subtitle: "Researcher Fellow | e-mail: nathan@ifisc.uib-csic.es"

profile:
  align: right
  image: eu_.jpg
  image_circular: false # crops the image to make it circular
  more_info: 
    <p><strong>Complex Systems in Life and the Environment</strong></p>
    <p><a href='https://ifisc.uib-csic.es/en/people/nathan-silvano/'>IFISC - (CSIC-UIB)</a></p>
    <p>Palma de Mallorca, Spain</p>

selected_papers: false # includes a list of papers marked as "selected={true}"
social: true # includes social icons at the bottom of the page

announcements:
  enabled: false # includes a list of news items
  scrollable: true # adds a vertical scroll bar if there are more than 3 news items
  limit: 5 # leave blank to include all the news in the `_news` folder

latest_posts:
  enabled: false
  scrollable: true # adds a vertical scroll bar if there are more than 3 new posts items
  limit: 3 # leave blank to include all the blog posts

---

<div style="margin-left: 0rem;">
I am currently a Post-Doc Research Fellow at Institute for Cross-Disciplinary Physics and Complex Systems.

Some of my research interests are
  - Nonlinear Dynamics, Complex Systems, Statistical Physics,
  - Active Matter, Active Solids, Pattern Formation, Biological Modelling,
  - Condensed Matter, Quantum Field Theory, Renormalization Group.

</div>


{% assign about_sections = "work,education" | split: "," %}
<div class="cv">
{% for name in about_sections %}
{% for data in site.data.resume %}
{% if data[0] == name %}
<div class="card mt-3 p-3">
<h3 class="card-title font-weight-medium">{{ name | capitalize }}</h3>
<div>
{% include resume/{{ name }}.liquid %}
</div>
</div>
{% endif %}
{% endfor %}
{% endfor %}
</div>




