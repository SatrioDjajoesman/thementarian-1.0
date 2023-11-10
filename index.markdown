---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: page
---

<div class="flex-container">

  <div class="latest-posts">
    <h2>Latest posts</h2>
    <ul class="post-ul">
      {% for post in site.posts limit:5 %}
        {% if post.category == "monthly issue" %}
          {% continue %}
        {% else %}
          <li><a href="{{ post.url }}">{{ post.title }}</a>
          <br>by {{ post.author | upcase }}, {{ post.date | date: "%d %b %Y"}}
          <br><p class="post-excerpt">{{ post.content | strip_html | truncatewords: 30 }}</p></li>
          <br>
        {% endif %}
      {% endfor %}
    </ul>
    <a href="{{ site.url }}/article-posts/">Click here to view more posts</a>

  </div>

  <div class="latest-issue">
    <!-- <h2 class="monthly-issue">Latest issue: August & September Issue 2023</h2>
    <div style="position: relative; width: 100%; height: 0; padding-top: 141.4148%;
    padding-bottom: 0; box-shadow: 0 2px 8px 0 rgba(63,69,81,0.16); margin-top: 1.6em; margin-bottom: 0.9em; overflow: hidden;
    border-radius: 8px; will-change: transform;">
      <iframe loading="lazy" style="position: absolute; width: 100%; height: 100%; top: 0; left: 0; border: none; padding: 0;margin: 0;"
        src="https:&#x2F;&#x2F;www.canva.com&#x2F;design&#x2F;DAFvzj37a-g&#x2F;view?embed" allowfullscreen="allowfullscreen" allow="fullscreen">
      </iframe>
    </div>
    <a href="https:&#x2F;&#x2F;www.canva.com&#x2F;design&#x2F;DAFvzj37a-g&#x2F;view?utm_content=DAFvzj37a-g&amp;utm_campaign=designshare&amp;utm_medium=embeds&amp;utm_source=link" target="_blank" rel="noopener"></a>
  </div> -->

  {% assign this_word = "monthly issue" %}
  {% for post in site.categories[this_word] limit:1 %} 
    {% if post.url %}
      <h2 class="monthly-issue">Latest issue: <a href="{{post.url}}">{{post.title}}</a></h2>
    {% endif %}
  {% endfor %}
  <div style="position: relative; width: 100%; height: 0; padding-top: 141.4148%;
    padding-bottom: 0; box-shadow: 0 2px 8px 0 rgba(63,69,81,0.16); margin-top: 1.6em; margin-bottom: 0.9em; overflow: hidden;
    border-radius: 8px; will-change: transform;">
      <iframe loading="lazy" style="position: absolute; width: 100%; height: 100%; top: 0; left: 0; border: none; padding: 0;margin: 0;"
        src="https:&#x2F;&#x2F;www.canva.com&#x2F;design&#x2F;DAFvzj37a-g&#x2F;view?embed" allowfullscreen="allowfullscreen" allow="fullscreen">
      </iframe>
    </div>
    <a href="https:&#x2F;&#x2F;www.canva.com&#x2F;design&#x2F;DAFvzj37a-g&#x2F;view?utm_content=DAFvzj37a-g&amp;utm_campaign=designshare&amp;utm_medium=embeds&amp;utm_source=link" target="_blank" rel="noopener"></a>
</div>