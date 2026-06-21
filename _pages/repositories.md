---
layout: page
permalink: /software/
title: software
description: check out my open-source projects at the repos below
nav: true
nav_order: 4
---

<div class="sw-list">
  {% if site.data.software.projects %}
    {% assign projects = site.data.software.projects %}
    {% if site.data.software.config.max_display %}
      {% assign projects = projects | slice: 0, site.data.software.config.max_display %}
    {% endif %}
    {% for project in projects %}
      {% include software_card.liquid project=project %}
    {% endfor %}
  {% endif %}
</div>

{% if site.data.software.config.show_more_button and site.data.software.config.button_link %}
<div style="margin-top: 1rem;">
  <a href="{{ site.data.software.config.button_link }}" target="_blank" rel="noopener noreferrer"
     style="font-size: 0.82rem; color: var(--global-text-color-light); text-decoration: none;">
    {{ site.data.software.config.button_text | default: "More on GitHub" }} →
  </a>
</div>
{% endif %}

{%- comment -%}
Legacy GitHub users section - uncomment if you want to keep it
{% if site.data.repositories.github_users %}

<hr class="my-5">

## GitHub users

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for user in site.data.repositories.github_users %}
    {% include repository/repo_user.liquid username=user %}
  {% endfor %}
</div>

{% if site.repo_trophies.enabled %}
{% for user in site.data.repositories.github_users %}
{% if site.data.repositories.github_users.size > 1 %}
  <h4>{{ user }}</h4>
{% endif %}
  <div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% include repository/repo_trophies.liquid username=user %}
  </div>
{% endfor %}
{% endif %}
{% endif %}
{%- endcomment -%}
