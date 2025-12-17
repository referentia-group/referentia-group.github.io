---
layout: home
---
<h2 class="centered_content">Institutions</h2>
<div class="logo-grid">
  {% for institution in site.data.institutions %}
    {% assign i = institution[1] %}
    <a href="{{ i.url }}" target="_blank"><img src="{{ site.image_folder }}/institutions/{{ i.logo }}"></a>
  {% endfor %}
</div>

<h2 class="centered_content">Partners</h2>
<div class="logo-grid">
  {% for partner in site.data.industry %}
    {% assign p = partner[1] %}
    <a href="{{ p.url }}" target="_blank"><img src="{{ site.image_folder }}/institutions/{{ p.logo }}"></a>
  {% endfor %}
</div>

<h2 class="centered_content">Groups</h2>
<div class="logo-grid">
  {% for group in site.data.groups %}
    {% assign g = group[1] %}
    <a href="{{ g.url }}" target="_blank"><img src="{{ site.image_folder }}/institutions/{{ g.logo }}"></a>
  {% endfor %}
</div>