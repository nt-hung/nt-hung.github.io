---
layout: archive
title: "Gallery"
permalink: /gallery/
author_profile: true
---

I love history, geography, and culture. This gallery records the beauty of the world where I had chances to visit.

<nbsp>

{% include base_path %}

{% assign ordered_pages = site.gallery | sort:"order_number" %}

{% for post in ordered_pages %}
  {% include archive-single.html type="grid" %}
{% endfor %}
