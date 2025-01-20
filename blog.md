---
layout: page
title: Nico's Blog
description: >- # this means to ignore newlines until "baseurl:"
  A place for me to share things I come across with. And also original thoughts and ideas
  that come from my/
---

{% for post in site.posts %}

<article>
  <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
  <p>{{ post.excerpt }}</p>
  <p><a href="{{ post.url }}">Read more</a></p>
</article>
{% endfor %}
