---
layout: default
title: Jen Wilson
---


### Education

- M.S. Computational Linguistics <span class="vline">|</span> University of Washington, Seattle (in progress)
- B.S. Geological Sciences <span class="vline">|</span> University of Washington, Seattle
- B.A. History <span class="vline">|</span> University of Washington, Seattle

---
## Projects

<ul class="projects-list">
  {% for project in site.projects %}
    <li class="project-item">
      {% if project.thumbnail %}
        <a href="{{ project.url | relative_url }}">
          <img src="{{ project.thumbnail | relative_url }}" alt="{{ project.title }} thumbnail" class="project-thumb-right">
        </a>
      {% endif %}

      <div class="project-info">
        <h2><a href="{{ project.url | relative_url }}">{{ project.title }}</a></h2>
        <p>{{ project.description }}</p>
      </div>
    </li>
  {% endfor %}
</ul>

---
## Invited Talks and Presentations

<ul class="resume-list">
{% assign sorted_talks = site.talks | sort: 'date' | reverse %}
  {% for talk in sorted_talks %}
    <li class="resume-item">
      <div class="resume-info">
        <!-- {% if talk.link %}
          <h2><a href="{{ talk.link | relative_url }}">{{ talk.title }}</a></h2>
        {% else %}
          <h2>{{ talk.title }}</h2>
        {% endif %} -->
        <h2>{{talk.title}}</h2>

        <i>{{ talk.venue }}</i>

        {% if talk.date %}
          •
          {% assign parsed_date = talk.date | date: "%B %Y" %}
          {% if parsed_date contains "0001" or parsed_date == "" %}
            {{ talk.date }}
          {% else %}
            {{ parsed_date }}
          {% endif %}
        {% endif %}

      {%if talk.invited %}
        <br>{{talk.invited}}
      {% endif %}

      {% if talk.description %}
        <p class="resume-desc">{{ talk.description }}</p>
      {% endif %}

      {% if talk.link %}
        <span style="color: #007acc; font-weight: normal;">
          <a href="{{ talk.link | relative_url }}" 
            target="_blank" 
            style="color: #007acc; text-decoration: none; font-weight: normal;"
            onmouseover="this.style.textDecoration='none'; this.style.color='#007acc';"
            onmouseout="this.style.textDecoration='none'; this.style.color='#007acc';"
            >
            {{talk.link}}
          </a>
        </span>
    {% endif %}

      {% if talk.slides or talk.recording %}       
        {% if talk.slides %}
          <a href="{{ talk.slides | relative_url }}" target="_blank">Slides</a>
          {% if talk.recording %} | {% endif %}
        {% endif %}
      {% endif %}
        
      {% if talk.recording %}
        <a href="{{ talk.recording }}" target="_blank">Recording</a>
      {% endif %}

      </div>
    </li>
  {% endfor %}
</ul>

---
## Published Papers

<ul class="resume-list">
  {% for paper in site.papers %}
    <li class="resume-item">
      <div class="authors">
      {% if paper.authors %}
        <span class="authors">{{ paper.authors | join: ", " }} </span>
      {% endif %}
      </div>
      <div class="resume-info">
        <!-- {% if paper.link %}
          <h2><a href="{{ paper.link | relative_url }}">{{ paper.title }}</a></h2>
        {% else %}
          {{ paper.title }}
        {% endif %} -->
        <b>{{paper.title}}</b> •
      
        {{ paper.journal }}
        {% if paper.date %}
          •
          {% assign parsed_date = paper.date | date: "%B %Y" %}
          {% if parsed_date contains "0001" or parsed_date == "" %}
            {{ paper.date }}.
          {% else %}
            {{ parsed_date }}.
          {% endif %}
        {% endif %}
      

      {% if paper.description %}
        {{ paper.description }}
      {% endif %}
      {% if paper.link %}
        <span style="color: #007acc; font-weight: normal;">
          <a href="{{ paper.link | relative_url }}" 
            target="_blank" 
            style="color: #007acc; text-decoration: none; font-weight: normal;"
            onmouseover="this.style.textDecoration='none'; this.style.color='#007acc';"
            onmouseout="this.style.textDecoration='none'; this.style.color='#007acc';"
            >
            {{paper.link}}
          </a>
        </span>
    {% endif %}
    </div>
    </li>
  {% endfor %}
</ul>

---
## Posters

<ul class="resume-list">
  {% for poster in site.posters %}
    <li class="resume-item">
      <div class="resume-info">
        {% if poster.link %}
          <h2><a href="{{ poster.link | relative_url }}">{{ paper.title }}</a></h2>
        {% else %}
          <b>{{ poster.title }}</b> •
        {% endif %}
      
        <i>{{ poster.venue }}</i>
        {% if poster.date %}
          •
          {% assign parsed_date = poster.date | date: "%B %Y" %}
          {% if parsed_date contains "0001" or parsed_date == "" %}
            {{ poster.date }}
          {% else %}
            {{ parsed_date }}
          {% endif %}
        {% endif %}

      {% if poster.description %}
        <p>{{ poster.description }}</p>
      {% endif %}
      </div>
    </li>
  {% endfor %}
</ul>

