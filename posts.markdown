---
layout: page
title: Posts
permalink: /article-posts/
---

<link rel="stylesheet" href="/assets/posts.css">
<!-- <html> -->
  {% capture get_items %}
{% for cat in site.categories %}
{{ cat | first | remove: "monthly issue" | replace: ' ', '_' }}
{% endfor %}
{% endcapture %}
{% capture num_words %}
{{ get_items | split:' ' | join:' ' | number_of_words }}
{% endcapture %}

{% for item in (1..num_words) %}

{% capture this_word %}{{ get_items | split:' ' | sort | join:' ' | truncatewords:item | remove:'...' | split:' ' | last | replace: '_', ' '  }}{% endcapture %}

<!-- <details>
<summary class="heading">{{ this_word }}</summary> -->
<ul class="related-posts">
{% for post in site.categories[this_word] %}
  <details>
  <summary class="heading">{{this_word}}</summary>
   {% if post.url %}
    <li class="post title"><a href="{{ post.url }}">{{ post.title }}</a></li>
    <li class="post">by {{ post.author | upcase }}, {{ post.date | date: "%d %b %Y"}}</li>
   {% endif %}
{% endfor %}
  </details>
</ul>
{% endfor %}
<!-- </details> -->

<!-- </html> -->