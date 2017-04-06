---
layout: page
title: Reading List
excerpt: "An archive of articles sorted by date."
search_omit: true
image:
  feature: reading_splash.jpg
---

## Currently reading

<ul class="post-list">
{% for post in site.categories.reading %}
  <img src="{{ site.url }}/images/{{ post.image.feature }}" width="80" height="100" style="float:left;">
  <li style="margin-left:100px"><article style="font-size:24px">{{ post.title }} <span class="entry-date"></span>{% if post.excerpt %} <span class="excerpt" style="font-size:18px;">{{ post.author | remove: '\[ ... \]' | remove: '\( ... \)' | markdownify | strip_html | strip_newlines | escape_once }}</span>{% endif %} <i style="color:grey;font-size:20px">{{ post.excerpt }}</i></article></li>
{% endfor %}
</ul>

## Recently read

<ul class="post-list">
{% for post in site.categories.read %}
  <img src="{{ site.url }}/images/{{ post.image.feature }}" width="80" height="100" style="float:left;">
  <li style="margin-left:100px"><article style="font-size:24px">{{ post.title }} <span class="entry-date"></span>{% if post.excerpt %} <span class="excerpt" style="font-size:18px;">{{ post.author | remove: '\[ ... \]' | remove: '\( ... \)' | markdownify | strip_html | strip_newlines | escape_once }}</span>{% endif %} <i style="color:grey;font-size:20px">{{ post.excerpt }}</i></article></li>
{% endfor %}
</ul>