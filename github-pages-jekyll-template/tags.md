---
layout: page
title: ""
permalink: /tags/
---

{% assign tags = site.tags | sort %}

<ul class="tag-list">
  {% for tag in tags %}
    {% assign tag_name = tag[0] %}
    {% assign tag_posts = tag[1] %}
    <li class="tag-item">
      <div class="tag-title" id="{{ tag_name | slugify }}">{{ tag_name }}</div>
      <ul class="tag-posts">
        {% for post in tag_posts %}
          <li>
            <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
            <span class="post-meta">{{ post.date | date: "%Y-%m-%d" }}</span>
          </li>
        {% endfor %}
      </ul>
    </li>
  {% endfor %}
</ul>
