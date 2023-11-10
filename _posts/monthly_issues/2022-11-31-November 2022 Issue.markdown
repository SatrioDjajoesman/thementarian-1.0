---
layout: page
category: monthly issue
folder: november2022issue
title: November 2022
volume: 2
issue: 11
---

<html>
{% assign folderpath = 'assets/images/' | append: page.folder %}
{% for image in site.static_files %}
{% if image.path contains folderpath %}
    <img src="{{ image.path }}" alt="">
{% endif %}
{% endfor %}

</html>