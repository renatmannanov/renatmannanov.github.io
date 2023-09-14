---
layout: default
title: "ray mann's blog"
---

<div class="header">
{% include header-logo.html %}
{% include header-panel.html %}
</div>

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

            {% include post-cards.html title=post.title url=post.url tags=post.tags type="blog" %}

        {% if forloop.last %}</div>{% endif %}

    {% endfor %}
</div>