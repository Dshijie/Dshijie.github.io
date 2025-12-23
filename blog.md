---
layout: page
title: ""
permalink: /blog/
---

{% assign posts = site.posts %}

<ul class="post-list">
  {% for post in posts %}
    <li>
      <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <span class="post-meta">{{ post.date | date: "%Y-%m-%d" }}</span>
    </li>
  {% endfor %}
</ul>
