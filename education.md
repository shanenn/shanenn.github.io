---
layout: page
permalink: /education/
title: Education
---

{% include home-header.html %}

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
        <span style="float:right;">{{ post.start }} - {{ post.end }}</span>
        {% else %}
        <span style="float:right;">{{ post.start }}</span>
        {% endif %}
        </p>
    </h2>

    <!-- <div class="post-meta">
      <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date_to_string }}</time>
      {%- if jekyll.environment == "production" and site.disqus -%}
        <span> • </span>
        <a class="comment-count" href="{{ post.url | relative_url }}#disqus_thread">
          <span class="disqus-comment-count" data-disqus-url="{{ post.url | absolute_url }}"></span>
        </a>
      {%- endif -%}
    </div> -->

    <p>{{ post.excerpt | strip_html }}</p>
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