---
layout: monthly_issue
category: monthly issue
folder: aprilmay2023issue
title: April & May 2023 Issue
volume: 4
issue: 1
---

<html>
{% assign folderpath = '/testProject/assets/images/' | append: page.folder %}
{% for image in site.static_files %}
{% if image.path contains folderpath %}
    <img src="{{ image.path }}" alt="">
{% endif %}
{% endfor %}

</html>