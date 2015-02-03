---
layout: default
title: Tech Talk
link: /tech
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

  <p class="rss-subscribe">subscribe <a href="/tech/feed.xml">via RSS</a></p>

</div>
