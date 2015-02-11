---
layout: family
title: Santini Family
link: /family
---

<div class="home">
  <section class="post-header">
    <h2><a href='{{ page.link }}'>{{ page.title }}</a></h2>
  </section>

  <ul class="posts">
    {% for post in site.categories.family %}
      <li>
        <a class="post-link" href="{{ post.url }}">{{ post.title }}</a>
        <span class="post-date">{{ post.date | date: "%b %-d, %Y" }}</span>
        <section>{{ post.excerpt }}</section>
      </li>
    {% endfor %}
  </ul>

  <p class="rss-subscribe">subscribe <a href="/family/feed.xml">via RSS</a></p>

</div>
