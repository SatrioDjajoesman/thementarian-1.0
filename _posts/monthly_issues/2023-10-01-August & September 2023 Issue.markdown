---
title: August & September 2023
date: 2023-10-01 00:00:00
category: monthly issue
layout: page
folder: augustseptember2023issue
volume: 4
issue: 1
---

<html>
{% assign folderpath = '/assets/images/' | append: page.folder %}
{% for image in site.static_files %}
{% if image.path contains folderpath %}
    <img src="{{ image.path }}" alt="">
{% endif %}
{% endfor %}
</html>
