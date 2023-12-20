---
title: November 2021
date: 2021-12-01 00:00:00 Z
categories:
- monthly issue
layout: page
folder: november2021issue
volume: 1
issue: 5
---

<html>
{% assign folderpath = 'assets/images/' | append: page.folder %}
{% for image in site.static_files %}
{% if image.path contains folderpath %}
    <img src="{{ image.path }}" alt="">
{% endif %}
{% endfor %}

</html>