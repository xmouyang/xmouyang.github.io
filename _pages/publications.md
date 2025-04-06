---
layout: page
permalink: /publications/
title: Publications
description: 
years: [2025, 2024, 2023, 2022, 2021]
nav: true
nav_order: 1
---

<div class="publications">

{% bibliography -f papers -q @*[publisher=arXiv]* %}

{% for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}} && publisher!=arXiv]* %}
{% endfor %}

</div>
