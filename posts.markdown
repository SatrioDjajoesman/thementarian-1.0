---
layout: page
title: Posts
permalink: /article-posts/
---

<html>
<ul class="post-ul">
    {% for post in site.posts %}
        {% if post.category == "monthly issue" %}
          {% continue %}
        {% else %}

        <li>{{ post.category }}</li>
        {% endif %}
    {% endfor %}
</ul>
</html>