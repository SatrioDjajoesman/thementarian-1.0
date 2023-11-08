---
layout: page
title: Posts
permalink: /article-posts/
---

<html>
{% for tag in site.categories %}
    {% if tag == "monthly issue"%}
        {% continue %}
    {% else %}
        <h3>{{ tag[0] }}</h3>
        <ul>
        {% for post in tag[1] %}
            <li><a href="{{ post.url }}">{{ post.title }}</a></li>
        {% endfor %}
        </ul>
    {% endif %}
{% endfor %}
</html>