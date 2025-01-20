---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
title: Nico's Blog
description: >- # this means to ignore newlines until "baseurl:"
  A place for me to share things I come across with. And also original thoughts and ideas
  that come from my learning experiences.
---

{% for post in site.posts %}

  <article>
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
    <p>{{ post.excerpt }}</p>
    <p><a href="{{ post.url }}">Read more</a></p>
  </article>
{% endfor %}
