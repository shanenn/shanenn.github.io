---
layout: page
permalink: /skills/
title: Skills
---

<div class="posts">
  {% for post in site.data.skills %}
  <section class="post-entry">
    <h2 class="post-title">
    <p style="text-align:left;">
        {{ post.category }}
        <!-- {% if post.current %}
        <span style="float:right;">{{ post.start }} - Current</span>
        {% else %}
        <span style="float:right;">{{ post.start }} - {{ post.end }}</span>
        {% endif %} -->
        </p>
    </h2>
    <ul>
    {% for r in post.content %}
        <li> {{r | strip_html}} </li>
    {% endfor %}
    </ul>
  </section>
  {% endfor %}

</div>