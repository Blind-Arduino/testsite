---
layout: default
title: "Blog"
permalink: /blog/
description: "News, updates, and thoughts from the Blind Arduino community."
---

## All Posts

<ul class="post-list" aria-label="Blog posts">
  {% for post in site.posts %}
  <li>
    <p class="post-meta"><a href="{{ post.url | relative_url }}">{{ post.title }}</a> &mdash; <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %-d, %Y" }}</time></p>
    <p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 50 }}</p>
  </li>
  {% else %}
  <li>No posts yet — check back soon!</li>
  {% endfor %}
</ul>
