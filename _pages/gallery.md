---
layout: archive
title: "Photography"
permalink: /gallery/
author_profile: true
---

I love to explore new lands to learn how people there live and work, their history, geography, and culture. Here are collections that I have taken over the years of "exploring the world". 

<nbsp>

{% include base_path %}

{% assign ordered_pages = site.gallery | sort:"order_number" %}

{% for post in ordered_pages %}
  {% include archive-single.html type="grid" %}
{% endfor %}
