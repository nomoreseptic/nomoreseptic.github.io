---
layout: index
permalink: / 
title: Home
date: 2020-03-06
---

<h2>Latest Posts</h2>
  <ul>
    {% for post in site.posts %}
      {% assign date_format = site.cayman.date_format | default: "%b %-d, %Y" %}
      <h3>
          <a class="post-link" href="{{ site.baseurl }}{{ post.url}}" title="{{ post.title }}">{{ post.title | escape }}</a>
      </h3>
      <span class="post-meta">{{ post.date | date: date_format }}
      </span>
      {{ post.excerpt | markdownify | truncatewords: 30 }}
    {% endfor %}
  <ul>
