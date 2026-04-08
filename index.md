---
layout: default
title: hello world
---

# hi

Just sharing my thoughts, reflections, and little moments that catch me—about life, space, people, and everything in between.

{% for post in site.posts %}
- [{{ post.title }}]({{ post.url }}) — {{ post.date | date: "%B %d, %Y" }}
{% endfor %}
