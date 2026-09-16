---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: Post
permalink: /
title: Last Thought
---
{% assign note_items = site.notes | sort: "date" | reverse %}
{% assign content = note_items[0].content %}
{% assign title = note_items[0].title %}
{%- include Content.html -%}
