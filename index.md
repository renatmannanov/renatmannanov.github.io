---
layout: default
title: "raymann's story"
---

{% include header.html %}

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
    {% include short-read-card.html title=content.title %}
  {% endfor %}
</ul>
