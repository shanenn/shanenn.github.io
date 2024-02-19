---
layout: page
permalink: /education/
title: Education
---

<!-- {% include home-header.html %} -->

<div class="posts">
  {% for post in site.data.schools %}
  <section class="post-entry">
    <h2 class="post-title">
      <!-- <a>
        {{ post.title }}
      </a> -->
    <p style="text-align:left;">
        {{ post.major }} | {{ post.school}}
        {% if post.end ISEMPTY }
        <span style="float:right;">{{ post.start }}</span>
        {% else %}
        <span style="float:right;">{{ post.start }} - {{ post.end }}</span>
        {% endif %}
        </p>
    </h2>
    <h3 class = "post-subheading">
    <a>
        {{ post.gpa }}
    </a>
    </h3>
    <p>{{ post.honors | strip_html }}</p>
    <p>{{ post.summary | strip_html }}</p>
  </section>
  {% endfor %}
  <!-- {%- if jekyll.environment == "production" and site.disqus -%}
    <script id="dsq-count-scr" src="//{{ site.disqus }}.disqus.com/count.js" async></script>
  {%- endif -%} -->
</div>

<!-- <div class="pagination">
  {% if paginator.next_page %}
    <a class="pagination-item older" href="{{ paginator.next_page_path | relative_url }}">Older</a>
  {% else %}
    <span class="pagination-item older">Older</span>
  {% endif %}
  {% if paginator.previous_page %}
    <a class="pagination-item newer" href="{{ paginator.previous_page_path | prepend: relative_url }}">Newer</a>
  {% else %}
    <span class="pagination-item newer">Newer</span>
  {% endif %}
</div> -->
