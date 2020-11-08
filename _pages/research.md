---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

My research tackles problems involving cooperative control and navigation of networked autonomous vehicles/mobile robots. Tools used to address these problem include : control, estimation, optimization and network theory.

<nbsp>

{% include base_path %}

{% assign ordered_pages = site.research | sort:"order_number" %}

{% for post in ordered_pages %}
  {% include archive-single.html type="grid" %}
{% endfor %}
