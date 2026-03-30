---
layout: page
title: Blog
permalink: /blog/
---

Articles techniques, retours d’expérience et notes autour de la data engineering.

{% if site.posts.size == 0 %}
*Aucun article pour le moment. Les billets publiés dans `_posts/` apparaîtront automatiquement ici.*
{% else %}
<ul class="post-list">
{% for post in site.posts %}
  <li>
    <span class="post-meta">{{ post.date | date: "%d/%m/%Y" }}</span>
    <h3>
      <a class="post-link" href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </h3>
    {% if post.excerpt %}
    <p>{{ post.excerpt | strip_html | truncatewords: 40 }}</p>
    {% endif %}
  </li>
{% endfor %}
</ul>
{% endif %}
