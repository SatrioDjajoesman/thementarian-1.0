---
layout: page
category: monthly issue
folder: november2021issue
title: November 2021
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