---
layout: page
category: monthly issue
folder: february2022issue
title: February 2022
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