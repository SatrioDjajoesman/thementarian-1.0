---
layout: page
title: Posts
permalink: /article-posts/
---


{% for categorie in site.categories %}
  <h3>{{ categorie[0] }}</h3>
  <ul>
    {% for post in categorie[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}