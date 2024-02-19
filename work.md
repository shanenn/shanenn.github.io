---
layout: page
permalink: /work/
title: Work Experience
---



<div class="posts">
  {% for post in site.data.work %}
  <section class="post-entry">
    <h2 class="post-title">
    <p style="text-align:left;">
        {{ post.occupation }} | {{ post.company}}
        {% if post.end ISEMPTY }
        <span style="float:right;">{{ post.start }} - Current</span>
        {% else %}
        <span style="float:right;">{{ post.start }} - {{ post.end }}</span>
        {% endif %}
        </p>
    </h2>
    <h3 class = "post-subheading">
    <a>
        GPA: {{ post.city }}
    </a>
    </h3>
    <ul>
    {% for r in post.responsibilities}
    <li> {r | strip_html} </li>
    {% endfor %}
    </ul>
  </section>
  {% endfor %}

</div>
