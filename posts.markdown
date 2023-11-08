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
        {% endif %}
    {% endfor %}
</ul>
</html>