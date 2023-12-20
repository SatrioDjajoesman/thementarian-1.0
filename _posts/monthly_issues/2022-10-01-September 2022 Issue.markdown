---
title: September 2022
date: 2022-10-01 00:00:00 Z
categories:
- monthly issue
layout: page
folder: september2022issue
volume: 2
issue: 9
---

<html>
{% assign folderpath = 'assets/images/' | append: page.folder %}
{% for image in site.static_files %}
{% if image.path contains folderpath %}
    <img src="{{ image.path }}" alt="">
{% endif %}
{% endfor %}

</html>