---
layout: page
title: Posts
permalink: /posts/
---

<html>
<ul class="post-ul">
    {% for post in site.posts %}
        {% if post.category == "monthly issue" %}
          {% continue %}
        {% else %}

        {{ post.category }}

        {% for s in post.category %}
            <li><a href="{{ s.url }}">{{ s.title }}</a>
            <br>by {{ s.author | upcase }}, {{ s.date | date: "%d %b %Y"}}
            <br>{{ s.content | strip_html | truncatewords: 30 }}</li>
            <br>
        {% endfor %}
        {% endif %}
    {% endfor %}
</ul>
</html>