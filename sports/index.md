---
layout: default
title: Sports
---

<div class="home">

  <ul class="posts">
    {% for post in site.posts %}
      {% if post.categories contains 'sports' %}
        <li>
          <a class="post-link" href="{{ post.url }}">{{ post.title }}</a>
          <span class="post-date">{{ post.date | date: "%b %-d, %Y" }}</span>
          <section>{{ post.excerpt }}</section>
        </li>
      {% endif %}
    {% endfor %}
  </ul>

  <p class="rss-subscribe">subscribe <a href="/feed.xml">via RSS</a></p>

</div>
