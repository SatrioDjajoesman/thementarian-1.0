---
title: February 2022
date: 2022-03-03 00:00:00
category: monthly issue
layout: page
folder: february2022issue
volume: 2
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