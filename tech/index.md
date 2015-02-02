---
layout: default
title: Tech
---

<div class="home">

  <ul class="posts">
    {% for post in site.categories.tech %}
      <li>
        <a class="post-link" href="{{ post.url }}">{{ post.title }}</a>
        <span class="post-date">{{ post.date | date: "%b %-d, %Y" }}</span>
        <section>{{ post.excerpt }}</section>
      </li>
    {% endfor %}
  </ul>

  <p class="rss-subscribe">subscribe <a href="/feed.xml">via RSS</a></p>

</div>
