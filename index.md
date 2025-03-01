---
layout: home
title: Home
nav_order: 1
nav_exclude: false
permalink: index.html
---


# Data Science Society 🤝 JamBase <img style = "width: 45px; margin-left: 15px; vertical-align: top;" src = "assets/site_images/dsslogopng.png"> <img style = "width: 45px; margin-left: 15px; vertical-align: top;" src = "assets/site_images/JB_logo.png">

## UC Berkeley, Spring 2025

[Jump to Current Week](#week-{{ site.current_week }}){: .btn .btn-currweek}

{% assign announcements = site.announcements | reverse %}
{% for announcement in announcements %}
{{ announcement }}
{% endfor %}


{% assign mods = site.modules | where: 'class', 'Berkeley' %}
{% assign active-mods = '' | split: '' %}

{% for mod in mods %}
  {% if mod.status == 'Active' %}
    {% assign active-mods = active-mods | push: mod %}
  {% endif %}
{% endfor %}

{% for module in active-mods %}
  {{ module }}
{% endfor %}