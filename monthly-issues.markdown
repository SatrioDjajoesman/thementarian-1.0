---
title: Monthly Issues
permalink: "/monthly-issues/"
layout: page
---

<html>
<link rel="stylesheet" href="/assets/monthly_issues.css">
{% assign postsByYear = site.posts | group_by_exp:"post", "post.date | date: '%Y'" %}
{% for year in postsByYear %}
  <h2>{{ year.name }}</h2>
    <ul>
      {% for post in year.items %}
        {% if post.category == "monthly issue" %}
        <li class="monthly-issue-list title"><a href="{{ post.url }}">{{ post.title }}</a></li>
        <li class="monthly-issue-list"> VOLUME {{post.volume}} ISSUE {{post.issue}}</li>
        <br>
        {% endif %}
      {% endfor %}
    </ul>
{% endfor %}
</html>