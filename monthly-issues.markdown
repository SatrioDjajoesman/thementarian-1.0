---
title: Monthly Issues
permalink: "/monthly_issues/"
layout: page
---

<html>
<link rel="stylesheet" href="/assets/monthly_issues.css">
<!-- {% assign monthly_issues = site.monthly_issues | reverse %} -->

<!-- {% for issue in monthly_issues %}
    <ul>
      <li class="monthly-issue-list title"><a href="{{ issue.url }}">{{ issue.title }}</a></li>
      <li class="monthly-issue-list"> VOLUME {{issue.volume}} ISSUE {{issue.issue}}</li>
    </ul>
{% endfor %} -->

{% assign postsByYear = site.monthly_issues | reverse | group_by_exp:"monthly_issues", "monthly_issues.date | date: '%Y'"%}
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