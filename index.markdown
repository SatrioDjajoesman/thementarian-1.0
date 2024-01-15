---
layout: page
---

<div class="flex-container">

  <div class="latest-posts">
    <h2>Latest posts</h2>
    <ul class="post-ul">
      {% for post in site.posts limit:5 %}
          <li class="title"><a href="{{ post.url }}">{{ post.title }}</a></li>
          <li>{{ post.date | date: "%d %B %Y"}}</li>
          <br>
      {% endfor %}
    </ul>
    <a href="{{ site.url }}/posts/">Click here to view more posts</a>
  </div>

  <div class="latest-issue">
  {%assign monthly_issue = site.monthly_issues | reverse%}
  {% for issue in monthly_issue limit: 1 %}
    <h2 class="monthly-issue">Latest issue: <a href="{{issue.url}}">{{issue.title}}</a></h2>
    <div class="monthly-issue-page">
    {% assign folderpath = '/assets/images/' | append: issue.folder %}
    {% for image in site.static_files %}
      {% if image.path contains folderpath and image.path contains "0001" %}
        <a href="{{issue.url}}"><img src="{{ image.path }}" alt=""></a>
      {% endif %}
    {% endfor %}
    </div>

  {% endfor %}



<!-- canva embed here -->