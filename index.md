---
layout: default
title: "raymann's story"
---

{% include header.html %}

<div>
    {% for post in site.posts %}

        {% assign currentdate = post.date | date: "%Y" %}
            {% if currentdate != date %}
                {% unless forloop.first %}</div>{% endunless %}
                <div class=yearbox id="y{{post.date | date: "%Y"}}">
                <div class=yeartext>{{ currentdate }}</div>
                <hr class=yearline/>
                </div>
                <div class=cardbox>
                {% assign date = currentdate %}
            {% endif %}
        {% include short-read-card.html title=post.title url=post.url %}
        {% if forloop.last %}</div>{% endif %}

    {% endfor %}
</div>

