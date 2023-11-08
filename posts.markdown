---
layout: page
title: Posts
permalink: /posts/
---

<html>
<ul class="post-ul">
    {% for post in site.posts limit:5 %}
        {% if post.category == "monthly issue" %}
          {% continue %}
        {% else %}
          <li><a href="{{ post.url }}">{{ post.title }}</a>
          <br>by {{ post.author | upcase }}, {{ post.date | date: "%d %b %Y"}}
          <br>{{ post.content | strip_html | truncatewords: 30 }}</li>
          <br>
        {% endif %}
    {% endfor %}
</ul>
</html>