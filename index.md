---
title: df/dx
layout: post
---

## Math, Mines and Muffins

Recent Posts

<ul>
  {% for post in site.posts %}
    <li>
      {{ post.date || date_to_string }}&nbsp;<a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>