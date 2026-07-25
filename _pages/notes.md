---
layout: page
permalink: /notes/
title: Notes
description: Essays, reading notes, and occasional thoughts on physics, philosophy, research, and life.
nav: true
nav_order: 3
---

{% include site-custom-style.html %}

<div class="notes-page">
  <ul class="notes-list">
    {% assign notes = site.posts | sort: "date" | reverse %}
    {% for post in notes %}
      <li class="notes-entry">
        <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
        <p>{{ post.description }}</p>
        <div class="notes-meta">
          <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %d, %Y" }}</time>
        </div>
      </li>
    {% endfor %}
  </ul>
</div>
