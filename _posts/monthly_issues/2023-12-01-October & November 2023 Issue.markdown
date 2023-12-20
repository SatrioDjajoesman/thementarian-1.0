---
title: October & November 2023
date: 2023-12-01 00:00:00 Z
categories:
- monthly issue
layout: page
folder: octobernovember2023issue
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
