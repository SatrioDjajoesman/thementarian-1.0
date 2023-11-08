---
layout: page
title: Posts
permalink: /posts/
---

<html>
{% for kategori in post.categories %}
    {% if kategori == "monthly issue"%}
        {% continue %}
    {% else %}
        {% for post in kategori %}
            <li>{{ post.title}}</li>
        {% endfor %}
    {% endif %}
{% endfor %}


</html>