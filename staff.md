---
layout: page
title: Team
description: Fall 2024 Academic Development
nav_order: 2
---

# Staff
Say HELLO to your Spring 2025 JamBase team
{: .no_toc .text-delta }

Hover over some of our icons to get a different side of our personalities!

<!--
<p style="font-size:30px">Note: This page is under construction.</p>


<p style="font-size:30px">Please check back soon for an updated staff roster!</p>

-->

<h2 style="text-align: center;">Point of Contact</h2>

{% assign instructors = site.staffers | where: 'role', 'POC' %}

<div class="role flex">
  {% for staffer in instructors %}
  {{ staffer }}
  {% endfor %}
</div>


<h2 style="text-align: center;">Leadership</h2>

{% assign leads = site.staffers | where: 'role', 'Leader' %}
{% assign sorted_director_by_order = leads | sort: 'order' %}

<div id = "staff-page" class="role flex">
{% for staffer in sorted_director_by_order %}
{{ staffer }}
{% endfor %}
</div>

## Consultants

{% assign tas = site.staffers | where: 'role', 'Consultant' %}
{% assign sorted_ta_by_order = tas | sort: 'order' %}

<div id="staff-page" class="role flex">
{% for staffer in sorted_ta_by_order %}
{{ staffer }}
{% endfor %}
</div>
