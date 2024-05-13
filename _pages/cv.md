---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

[Download my full CV (PDF)](https://raw.githubusercontent.com/BernardoRaimundo/BernardoRaimundo.github.io/master/files/Curriculum%20Vitae.pdf)

Education
======
<div class="accordion" id="educationAccordion">
  <div class="accordion-item">
    <h2 class="accordion-header" id="headingOne">
      <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
        Ph.D. in Information Management specializing in Data Science (2024 - Present)
      </button>
    </h2>
    <div id="collapseOne" class="accordion-collapse collapse" aria-labelledby="headingOne" data-bs-parent="#educationAccordion">
      <div class="accordion-body">
        <strong>Nova IMS</strong>. Currently pursuing a Ph.D. in Information Management with a specialization in Data Science.
      </div>
    </div>
  </div>
  <div class="accordion-item">
    <h2 class="accordion-header" id="headingTwo">
      <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#collapseTwo" aria-expanded="false" aria-controls="collapseTwo">
        M.S. Statistics and Information Management specializing in Risk Analysis and Management (2021 - 2023)
      </button>
    </h2>
    <div id="collapseTwo" class="accordion-collapse collapse" aria-labelledby="headingTwo" data-bs-parent="#educationAccordion">
      <div class="accordion-body">
        <strong>Nova IMS</strong>. Completed a Master's degree in Statistics and Information Management, focusing on Risk Analysis and Management.
      </div>
    </div>
  </div>
  <!-- More accordion items can be added similarly for other degrees -->
</div>


<!--  
Work experience
======
* Spring 2024: Academic Pages Collaborator
  * Github University
  * Duties includes: Updates and improvements to template
  * Supervisor: The Users

* Fall 2015: Research Assistant
  * Github University
  * Duties included: Merging pull requests
  * Supervisor: Professor Hub

* Summer 2015: Research Assistant
  * Github University
  * Duties included: Tagging issues
  * Supervisor: Professor Git

Skills
======
* Skill 1
* Skill 2
  * Sub-skill 2.1
  * Sub-skill 2.2
  * Sub-skill 2.3
* Skill 3
-->

Publications
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>

<!--  
Talks
======
  <ul>{% for post in site.talks reversed %}
    {% include archive-single-talk-cv.html  %}
  {% endfor %}</ul>
  
-->

Teaching
======
  <ul>{% for post in site.teaching reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  

<!--    
Service and leadership
======
* Currently signed in to 43 different slack teams

-->

