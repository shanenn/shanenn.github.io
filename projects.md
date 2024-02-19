---
layout: page
permalink: /projects/
title: Projects/Supplemental
---

<div class="posts">
  {% for post in site.data.projects %}
  <section class="post-entry">
    <h2 class="post-title">
    <p style="text-align:left;">
        {{ post.name }}
        {% if post.current %}
        <span style="float:right;">{{ post.start }} - Ongoing</span>
        {% else %}
        <span style="float:right;">{{ post.start }} - {{ post.end }}</span>
        {% endif %}
        </p>
    </h2>
    <h3 class = "post-subheading">
        <a>
            {{ post.extra }}
        </a>
    </h3>
    <ul>
    {% for r in post.info %}
        <li> {{r | strip_html}} </li>
    {% endfor %}
    </ul>
    link = 
      <a href= "{{ post.link }}"download="ShaneNguyenResume.pdf">GitHub Link</a>
  </section>
  {% endfor %}

</div>