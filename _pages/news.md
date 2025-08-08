---
layout: page
permalink: /news/
title: News
description: All news and announcements from the NAIL Lab
nav: true
nav_order: 8
---

<div class="news">
  <h2>All News & Announcements</h2>
  {% if site.news != blank -%} 
  {%- assign news_size = site.news | size -%}
  <div class="table-responsive">
    <table class="table table-sm table-borderless">
    {%- assign news = site.news | reverse -%}
    {% for item in news %} 
      <tr>
        <th scope="row" style="min-width: 120px;">{{ item.date | date: "%b %-d, %Y" }}</th>
        <td>
          {% if item.inline -%} 
            {{ item.content | remove: '<p>' | remove: '</p>' | emojify }}
          {%- else -%} 
            <a class="news-title" href="{{ item.url | relative_url }}">{{ item.title }}</a>
          {%- endif %} 
        </td>
      </tr>
    {%- endfor %} 
    </table>
  </div>
  {%- else -%} 
    <p>No news so far...</p>
  {%- endif %} 
</div>

<style>
.news table th {
  font-weight: 500;
  color: var(--global-theme-color);
  border-right: 1px solid var(--global-divider-color);
  padding-right: 1rem;
}

.news table td {
  padding-left: 1rem;
  line-height: 1.5;
}

.news table tr {
  border-bottom: 1px solid var(--global-divider-color-light);
}

.news table tr:hover {
  background-color: var(--global-bg-color-light);
}
</style>