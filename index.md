---
layout: home
---

<div class="hero">
  <img src="/assets/images/hero.png" alt="">
  <div class="hero-content">
    <h1>{{ site.title }}</h1>
    <p>{{ site.description }}</p>
  </div>
</div>

<h2 class="centered_content">Institutions</h2>
<div class="logo-grid">
  {% for institution in site.data.institutions %}
    {% assign i = institution[1] %}
    <a href="{{ g.url }}" target="_blank" class="logo"><img src="{{ site.image_folder }}/institutions/{{ i.logo }}"><span class="logo-text">{{ i.name_en }}</span></a>
  {% endfor %}
</div>

<h2 class="centered_content">Partners</h2>
<div class="logo-grid">
  {% for partner in site.data.industry %}
    {% assign p = partner[1] %}
    <a href="{{ g.url }}" target="_blank" class="logo"><img src="{{ site.image_folder }}/institutions/{{ p.logo }}"><span class="logo-text">{{ p.name_en }}</span></a>
  {% endfor %}
</div>

<h2 class="centered_content">Groups</h2>
<div class="logo-grid">
  {% for group in site.data.groups %}
    {% assign g = group[1] %}
    <a href="{{ g.url }}" target="_blank" class="logo"><img src="{{ site.image_folder }}/institutions/{{ g.logo }}"><span class="logo-text">{{ g.name_en }}</span></a>
  {% endfor %}
</div>
