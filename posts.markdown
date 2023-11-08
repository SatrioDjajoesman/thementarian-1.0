---
layout: page
title: Posts
permalink: /article-posts/
---


{% for categorie in site.categories %}
  <h3>{{ categories[0] }}</h3>
  <ul>
    {% for post in categories[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}