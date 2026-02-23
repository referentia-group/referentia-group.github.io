---
title: People
layout: default
---

<div>
  {% for group in site.data.people %}
    <h2 class="centered_content">{{ group[1].name }}</h2>
    <div class="people-grid">
      {% for person in group[1].people %}
        <div class="person-card">
          {% if person.photo != null %}
            <img src="{{ site.image_folder }}/people/{{ person.photo }}" alt="{{ person.name }}">
          {% endif %}
          <p>
            <strong>{{ person.name }}</strong><br>
            <em>{{ person.position }}</em>
          </p>
          <p>
            {% if person.institution_high != null %}
              {% for inst_id in person.institution_high %}
                {% assign inst = site.data.institutions[inst_id] %}
                {{ inst.name_short }}{% unless forloop.last %} - {% endunless %}
              {% endfor %}
              <br>
            {% endif %}
            {% if person.industry != null %}
              {% for ind_id in person.industry %}
                {% assign ind = site.data.industry[ind_id] %}
                {{ ind.name_short }}{% unless forloop.last %} - {% endunless %}
              {% endfor %}
              <br>
            {% endif %}
          </p>
          <p>
            {% if person.url != null %}
              <a href="{{ person.url }}" target="_blank">Personal Website</a>
            {% endif %}
          </p>
        </div>
      {% endfor %}
    </div>
  {% endfor %}
</div>
