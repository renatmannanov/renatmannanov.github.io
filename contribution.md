---
layout: default
title: "ray mann's contribution"
---

<div class="header">
{% include header-logo.html %}
</div>

<div>
    <div class=yearbox>
        <div class=yeartext>давайте поработаем</div>
        <hr class=yearline/>
    </div>

    <div class=cardbox>
    {% assign sorted_offers = site.offers | sort: "order"%}
    {% for offer in sorted_offers %}
        
        {% 
          include offer-cards.html
        %}

    {% endfor %}

    </div>
</div>