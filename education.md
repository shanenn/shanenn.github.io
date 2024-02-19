---
layout: page
permalink: /education/
title: Education
---


<div class="posts">
  {% for post in site.data.schools %}
  <section class="post-entry">
    <h2 class="post-title">
    <p style="text-align:left;">
        {{ post.major }} | {{ post.school}}
        {% if post.end ISEMPTY %}
        <span style="float:right;">{{ post.start }}</span>
        {% else %}
        <span style="float:right;">{{ post.start }} - {{ post.end }}</span>
        {% endif %}
        </p>
    </h2>
    <h3 class = "post-subheading">
    <a>
        GPA: {{ post.gpa }}
    </a>
    </h3>
    <ul>
    <li>{{ post.honors | strip_html }}</li>
    <li>{{ post.summary | strip_html }}</li>
    </ul>
  </section>
  {% endfor %}

</div>
