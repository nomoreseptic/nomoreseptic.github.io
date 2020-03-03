---
#
# Here you can change the text shown in the Home page before the Latest Posts section.
#
# Edit cayman-blog's home layout in _layouts instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
#
layout: index
---
<h2>Latest Posts</h2>

<div>

    <ul>
      {% for post in site.posts %}
      {% assign date_format = site.cayman.date_format | default: "%b %-d, %Y" %}
        <!-- <li> -->
            <h3>
                <a class="post-link" href="{{ post.url}}" title="{{ post.title }}">{{ post.title | escape }}</a>
            </h3>
            <span class="post-meta">{{ post.date | date: date_format }}
                </span>
            {{ post.excerpt | markdownify | truncatewords: 30 }}
        <!-- </li> -->
      {% endfor %}
    <ul>
 
