---
layout: post
title: בלוג
language: he
permalink: /he/blog/
---

בהקמה.
Example post:

<ul class="listing">
{% for post in site.posts %}
  {% if post.categories contains 'blogHE' %}
    {% capture y %}{{post.date | date:"%Y"}}{% endcapture %}
    {% if year != y %}
      {% assign year = y %}
      <li class="listing-seperator">{{ y }}</li>
    {% endif %}
    <li class="listing-item">
      <time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time>
      <a href="{{ site.baseurl }}{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
    </li>
  {% endif %}
{% endfor %}
</ul>
