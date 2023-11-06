---
layout: page
title: Monthly Issues
permalink: /monthly-issues/
---

<html>
<link rel="stylesheet" href="/testProject/assets/monthly_issues.css">
{% for post in site.posts %}
    {% if post.category != "monthly issue" %}
        {% continue %}
    {% else %}
        <li class="monthly-issue-list title"><a href="/testProject/{{ post.url }}">{{ post.title }}</a></li>
        <li class="monthly-issue-list"> VOLUME {{post.volume}} ISSUE {{post.issue}}</li>
    {% endif %}
{% endfor %}
</html>