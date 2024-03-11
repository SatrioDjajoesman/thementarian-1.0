---
title: Monthly Issues
permalink: "/monthly_issues/"
layout: main
---

<html>
<link rel="stylesheet" href="/assets/css/monthly_issues.css">

{% assign postsByYear = site.monthly_issues | reverse | group_by_exp:"monthly_issues", "monthly_issues.date | date: '%Y'"%}
{% for year in postsByYear %}
  <h2>{{ year.name }}</h2>
    <div class="grid-container">
        {% for post in year.items %}
          <div class="grid-items">
            {% assign folderpath = '/assets/images/monthly_issues/' | append: post.folder %}
            {% for image in site.static_files %}
              {% if image.path contains folderpath and image.path contains "0001" %}
                <a href="{{post.url}}"><img src="{{ image.path }}" alt=""></a>
              {% endif %}
            {% endfor %}
            <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
          </div>
      {% endfor %}
    </div>
{% endfor %}

</html>