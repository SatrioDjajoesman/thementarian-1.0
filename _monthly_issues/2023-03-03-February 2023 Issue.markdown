---
title: February 2023
date: 2023-03-03 00:00:00
category: monthly issue
layout: page
folder: february2023issue
volume: 3
issue: 2
---

<html>
{% assign folderpath = 'assets/images/' | append: page.folder %}
{% for image in site.static_files %}
{% if image.path contains folderpath %}
    <img src="{{ image.path }}" alt="">
{% endif %}
{% endfor %}

</html>