---
layout: page
category: monthly issue
folder: september2021issue
title: September 2021
volume: 4
issue: 1
---

<html>
{% assign folderpath = 'assets/images/' | append: page.folder %}
{% for image in site.static_files %}
{% if image.path contains folderpath %}
    <img src="{{ image.path }}" alt="">
{% endif %}
{% endfor %}

</html>