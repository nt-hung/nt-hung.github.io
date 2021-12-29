---
layout: archive
title: "Photography"
permalink: /gallery/
author_profile: true
---

I love to go to new places, see how local people live and work, and learn their history, geography, and couture. Here is the collections of pictures that I have taken over the years of exploring the world. 

<nbsp>

{% include base_path %}

{% assign ordered_pages = site.gallery | sort:"order_number" %}

{% for post in ordered_pages %}
  {% include archive-single.html type="grid" %}
{% endfor %}
