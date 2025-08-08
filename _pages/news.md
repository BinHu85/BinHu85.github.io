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
    <table class="table table-sm table-borderless compact-news">
    {%- assign news = site.news | reverse -%}
    {% for item in news %} 
      <tr>
        <th scope="row" style="min-width: 100px; width: 100px; font-size: 0.85rem; padding: 0.4rem 0.5rem;">{{ item.date | date: "%b %d, %y" }}</th>
        <td style="font-size: 0.9rem; padding: 0.4rem 0.5rem; line-height: 1.3;">
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
.compact-news th {
  font-weight: 500;
  color: var(--global-theme-color);
  border-right: 1px solid var(--global-divider-color);
  vertical-align: top;
}

.compact-news td {
  border-left: 1px solid var(--global-divider-color-light);
  padding-left: 0.8rem !important;
}

.compact-news tr {
  border-bottom: 1px solid rgba(0,0,0,0.05);
}

.compact-news tr:hover {
  background-color: var(--global-bg-color-light);
}

.compact-news tr:last-child {
  border-bottom: none;
}
</style>