---
layout: blog
title: Blog
permalink: /blog/
---

# Blog
Welcome to my blog! Here are my posts:
{% for post in site.posts %}
- [{{ post.title }}]({{ post.url }})
{% endfor %}
