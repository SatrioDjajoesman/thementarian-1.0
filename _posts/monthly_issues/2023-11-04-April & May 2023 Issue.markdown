---
layout: monthly_issue
category: monthly issue
folder: aprilmay2023issue
title: April & May 2023 Issue
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
