---
layout: page
title: The archive
permalink: /the-archive/
sidebar_link: true
---

## <em> by category </em>
{% for category in site.categories %}
  <h3>{{ category[0] }}</h3>
  <ul>
    {% for post in category[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a>: {{ post.content | strip_html | truncatewords:50 }}</li>
    {% endfor %}
  </ul>
{% endfor %}

## <em> by tag </em>
{% for tag in site.tags %}
  <h3>{{ tag[0] }}</h3>
  <ul>
    {% for post in tag[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}
