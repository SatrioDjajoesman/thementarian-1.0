---
title: Posts
permalink: "/posts/"
layout: page
---

<link rel="stylesheet" href="/assets/posts.css">

<ul class="post-ul">
{% for post in site.posts %}
    {% if post.category == "monthly issue" %}
        {% continue %}
    {% else %}
        <li class="title"><a href="{{ post.url }}">{{ post.title }}</a></li>
        <li>by {{post.author}} | {{ post.date | date: "%d %B %Y"}}</li>
        <br>
    {% endif %}
{% endfor %}
</ul>