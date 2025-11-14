---
layout: page
permalink: /publications/
title: Publications
description:
years: [2026, 2025, 2024, 2023, 2022, 2021, 2020, 2019, 2018, 2017, 2016, 2015, 2014, 2013, 2012, 2011]
nav: true
nav_order: 2  
---
<!-- _pages/publications.md -->
<div class="publications">

<p style="margin-bottom: 2rem; padding: 1rem; background-color: var(--global-card-bg-color); border-left: 4px solid var(--global-theme-color); border-radius: 4px;">
<strong>Note:</strong> Names marked with ★ indicate my PhD students and ♦ indicate my Master's students.
</p>

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f hu -q @*[year={{y}}]* %}
{% endfor %}

</div>
