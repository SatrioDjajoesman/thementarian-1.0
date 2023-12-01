---
layout: page
category: monthly issue
folder: octobernovember2023issue
title: October & November 2023
volume: 4
issue: 2
---
<html>
{% assign folderpath = '/assets/images/' | append: page.folder %}
{% for image in site.static_files %}
{% if image.path contains folderpath %}
    <img src="{{ image.path }}" alt="">
{% endif %}
{% endfor %}
</html>
