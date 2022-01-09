---
layout: archive
title: "Collections"
permalink: /gallery/
author_profile: true
---

I love to visit new places to learn history, culture, and geography. Here are collections that I have taken over the years of "exploring the world". 

<nbsp>

{% include base_path %}

{% assign ordered_pages = site.gallery | sort:"order_number" %}

{% for post in ordered_pages %}
  {% include archive-single.html type="grid" %}
{% endfor %}
