---
layout: default
title: Home
---


### Education

<!-- <table style="width:100%;">
  <tr>
    <td>M.S. Computational Linguistics</td>
    <td>University of Washington, Seattle (in progress)</td>
  </tr>
  <tr>
    <td>B.S. Geological Sciences</td>
    <td>University of Washington, Seattle</td>
  </tr>
  <tr>
    <td>B.A. History</td>
    <td>University of Washington, Seattle</td>
  </tr>
</table> -->

- M.S. Computational Linguistics University of Washington, Seattle (in progress)
- B.S. Geological Sciences University of Washington, Seattle
- B.A. History University of Washington, Seattle

### Projects
<ul class="projects-list">
  {% for project in site.projects %}
    <li class="project-item">
      {% if project.image %}
        <img src="{{ project.image | relative_url }}" alt="{{ project.title }}">
      {% endif %}
      <h2><a href="{{ project.url | relative_url }}">{{ project.title }}</a></h2>
      <p>{{ project.description }}</p>
    </li>
  {% endfor %}
</ul>


