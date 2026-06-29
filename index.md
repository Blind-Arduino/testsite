---
layout: default
title: "Welcome to the Blind Arduino Project"
permalink: /
description: "A community of blind and sighted makers building accessible electronics together."
---

## The Blind Arduino Project is 10 years old!

In honor of the occasion, we're finally giving it a real web site. It's been a long time coming — and we're just getting started.

## What's coming

We're planning all kinds of cool resources and events — stay tuned! Think tutorials, accessible project designs, equipment reviews, community meetups, and more. Watch this space.

## Latest from the blog

<ul class="post-list" aria-label="Recent blog posts">
  {% for post in site.posts limit: 3 %}
  <li>
    <p class="post-meta"><a href="{{ post.url | relative_url }}">{{ post.title }}</a> &mdash; <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %-d, %Y" }}</time></p>
    <p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 40 }}</p>
  </li>
  {% else %}
  <li>No posts yet — check back soon!</li>
  {% endfor %}
</ul>

<p><a href="{{ "/blog/" | relative_url }}">All blog posts →</a></p>

## Upcoming events

<ul class="event-list" aria-label="Upcoming events">
  {% assign upcoming = site.events | where_exp: "event", "event.date >= site.time" | sort: "date" %}
  {% for event in upcoming limit: 3 %}
  <li>
    <strong><a href="{{ event.url | relative_url }}">{{ event.title }}</a></strong>
    <p class="event-meta"><time datetime="{{ event.date | date_to_xmlschema }}">{{ event.date | date: "%B %-d, %Y" }}</time>{% if event.time %} at {{ event.time }}{% endif %}{% if event.location %} &mdash; {{ event.location }}{% endif %}</p>
  </li>
  {% else %}
  <li>No upcoming events right now — check back soon!</li>
  {% endfor %}
</ul>

## Stay connected

Sign up for the Blind Arduino email list at groups.io by sending a blank email to [babamm+subscribe@groups.io](mailto:babamm+subscribe@groups.io). It's the best way to stay in the loop on everything we're up to.
