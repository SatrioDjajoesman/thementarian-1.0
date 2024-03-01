---
title: December-February 2024
date: 2024-02-01 00:00:00 
category: monthly issue
layout: page
folder: decemberfeb2024issue
volume: 4
issue: 3
---

<html>
{% assign folderpath = '/assets/images/' | append: page.folder %}
{% for image in site.static_files %}
{% if image.path contains folderpath %}
    <img src="{{ image.path }}" alt="">
{% endif %}
{% endfor %}
</html>
