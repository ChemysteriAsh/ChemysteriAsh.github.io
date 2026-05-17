
---
layout: page
permalink: /publications/
title: publications
description: A collection of my research and publications.
nav: true
nav_order: 2
---

<div class="publications">

  <!-- _pages/publications.md -->

<!-- Bibsearch Feature -->

{% include bib_search.liquid %}

<div class="publications">

{% bibliography %}


{% if site.scholar.group_by == 'year' %}
  {% for y in page.years %}
    <h2 class="year">{{ y }}</h2>
    {% bibliography -q @*[year={{y}}]* %}
  {% endfor %}
{% else %}
  {% bibliography %}
{% endif %}

</div>
