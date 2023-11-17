---
layout: page
title: Posts
permalink: /article-posts/
---

<link rel="stylesheet" href="/assets/posts.css">
<html>
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

<a name="{{ this_word  }}"></a>
<h3>{{ this_word}}</h3>
<ul class="related-posts">
{% for post in site.categories[this_word] %}
   {% if post.url %}
    <li><a href="{{ post.url }}">{{ post.title }}</a>
          <br>by {{ post.author | upcase }}, {{ post.date | date: "%d %b %Y"}}
          <br><p class="post-excerpt">{{ post.content | strip_html | truncatewords: 30 }}</p>
    </li>
   {% endif %}
{% endfor %}
</ul>
{% endfor %}
</html>