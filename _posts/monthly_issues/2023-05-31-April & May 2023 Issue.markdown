---
title: April & May 2023
date: 2023-05-31 00:00:00 Z
categories:
- monthly issue
layout: page
folder: aprilmay2023issue
volume: 3
issue: 4/5
---

<html>
{% assign folderpath = '/assets/images/' | append: page.folder %}
{% for image in site.static_files %}
{% if image.path contains folderpath %}
    <img src="{{ image.path }}" alt="">
{% endif %}
{% endfor %}
</html>
