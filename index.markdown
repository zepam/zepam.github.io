---
layout: default
title: Jen Wilson
---


### Education

- <b>M.S. Computational Linguistics <span class="vline">|</span> University of Washington, Seattle (in progress)
- Graduate Certificate in Software Design and Development	<span class="vline">|</span> University of Washington, Bothell, WA
- B.S. Geological Sciences <span class="vline">|</span> University of Washington, Seattle
- B.A. History <span class="vline">|</span> University of Washington, Seattle

---
## Current Projects

<ul class="projects-list">
  {% for project in site.projects %}
    {% if project.current %}
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
    {% endif %}
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
        {% assign paper_target = paper.link | default: paper.url %}

        {% if paper.thumbnail %}
          <a href="{{ paper_target | relative_url }}">
            <img src="{{ paper.thumbnail | relative_url }}" alt="{{ paper.title }} thumbnail" class="project-thumb-right">
          </a>
        {% endif %}

        <b><a href="{{ paper_target | relative_url }}" {% if paper.link %}target="_blank" rel="noopener"{% endif %}>{{ paper.title }}</a></b>
      <br>
        {{ paper.journal }}
        {% if paper.date %}

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
              <br>
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
          <h2><a href="{{ poster.link | relative_url }}">{{ poster.title }}</a></h2>
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

        {% if poster.thumbnail and poster.image %}
          <a href="{{ poster.image | relative_url }}" target="_blank">
            <img src="{{ poster.thumbnail | relative_url }}" alt="{{ poster.title }} poster" class="project-thumb-right">
          </a>
        {% endif %}

      {% if poster.description %}
        <p>{{ poster.description }}</p>
      {% endif %}

      {% if poster.image %}
        <p><a href="{{ poster.image | relative_url }}" target="_blank">View poster</a></p>
      {% endif %}
      </div>
    </li>
  {% endfor %}
</ul>



---
## Fun

<ul class="projects-list fun-list">
  {% assign fun_items = site.fun | sort: 'date' | reverse %}
  {% if fun_items.size > 0 %}
    {% for item in fun_items %}
      {% assign target_url = item.link | default: item.url %}
      <li class="project-item">
        {% if item.thumbnail %}
          <a href="{{ target_url | relative_url }}" {% if item.link %}target="_blank" rel="noopener"{% endif %}>
            <img src="{{ item.thumbnail | relative_url }}" alt="{{ item.title }} thumbnail" class="project-thumb-right">
          </a>
        {% endif %}

        <div class="project-info">
          <h2>
            <a href="{{ target_url | relative_url }}" {% if item.link %}target="_blank" rel="noopener"{% endif %}>{{ item.title }}</a>
          </h2>
          {% if item.description %}
            <p>{{ item.description }}</p>
          {% endif %}
        </div>
      </li>
    {% endfor %}
  {% else %}
    <li>No fun projects yet — check back later.</li>
  {% endif %}
</ul>

---
## Past Projects

<ul class="projects-list">
  {% for project in site.projects %}
    {% unless project.current %}
    <li class="project-item">
      {% if project.thumbnail %}
        <a href="{{ project.url | relative_url }}">
          <img src="{{ project.thumbnail | relative_url }}" alt="{{ project.title }} thumbnail" class="project-thumb-right">
        </a>
      {% endif %}

      <div class="project-info">
        {% if project.no_second_page %}
          <h2>{{ project.title }}</h2>
        {% else %}
          <h2><a href="{{ project.url | relative_url }}">{{ project.title }}</a></h2>
        {% endif %}
        <p>{{ project.description }}</p>
      </div>
    </li>
    {% endunless %}
  {% endfor %}
</ul>


