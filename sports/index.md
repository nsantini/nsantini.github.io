---
layout: page
title: Sports
---

<div class="home">

  <h1>Sports Posts</h1>

  <ul class="posts">
    {% for post in site.posts %}
      {% if post.categories == 'sports' %}
        <li>
          <span class="post-date">{{ post.date | date: "%b %-d, %Y" }}</span>
          <a class="post-link" href="{{ post.url }}">{{ post.title }}</a>
          <p>{{ post.summary }}</p>
        </li>
      {% endif %}
    {% endfor %}
  </ul>

  <p class="rss-subscribe">subscribe <a href="/feed.xml">via RSS</a></p>

</div>
