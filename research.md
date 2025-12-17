---
title: Research
layout: default
---

## Papers

<div>
{% for paper in site.data.research["papers"]["items"] %}
  <p><strong>{{ paper.title }}</strong>
  {% if paper.pdf != null %}
    <a href="{{ paper.pdf }}" target="_blank">[pdf]</a>
  {% endif %}
  <br>
  {% for author in paper.author %}
    {{ author }}
  {% endfor %}</p>
  {% if paper.doi != null %}
    <p>DOI: {{ paper.doi }}</p>
  {% endif %}
  {% if paper.url != null %}
    <p>URL: <a href="{{ paper.url }}" target="_blank">{{ paper.url }}</a></p>
  {% endif %}
  <p><em>Abstract</em>: {{ paper.abstract }}</p>
{% endfor %}
</div>

## Projects

<div>
{% for project in site.data.research["projects"]["items"] %}
  <p><strong>{{ project.title }}</strong></p>
  <p>{{ project.description }}</p>
  {% if project.url != null %}
    <p>URL: <a href="{{ project.url }}" target="_blank">{{ project.url }}</a></p>
  {% endif %}
{% endfor %}
</div>