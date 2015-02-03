---
layout: default
title: Becoming an Athlete
link: /sports
---

<div class="home">

  <ul class="posts">
    {% for post in site.categories.sports %}
      <li>
        <a class="post-link" href="{{ post.url }}">{{ post.title }}</a>
        <span class="post-date">{{ post.date | date: "%b %-d, %Y" }}</span>
        <section>{{ post.excerpt }}</section>
      </li>
    {% endfor %}
  </ul>

  <p class="rss-subscribe">subscribe <a href="/sports/feed.xml">via RSS</a></p>

</div>
