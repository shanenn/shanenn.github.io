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
        {% if post.start == post.end %}
        <span style="float:right;">{{ post.start }}</span>
        {% else %}
        <span style="float:right;">{{ post.start }} - {{ post.end }}</span>
        {% endif %}
        {% endif %}
        </p>
    </h2>
    <h3 class = "post-subheading">
    <a href= "{{ post.extra.link }}" target = "_blank">Link: {{post.extra.display}}</a>
    </h3>
    <ul>
    {% for r in post.info %}
        <li> {{r | strip_html}} </li>
    {% endfor %}
    </ul>
    {% if post.image %}
    <img src="{{ site.url }}{{ site.baseurl }}/_images/{{ post.image }}" class="img-responsive" width="50%" />
    {% endif %}
      <a href= "{{ post.link }}" target = "_blank">GitHub Link</a>
  </section>
  {% endfor %}

</div>