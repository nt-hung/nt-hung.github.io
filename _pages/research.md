---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

My research tackles problems involving the cooperative control and estimation of networked multi-agent systems under communication constraints. Each agent can be a mobile ground robot, an autonomous arial/marine vehicle (AUV), or simply, a sensor node. Applications include formation control of multiple autonomous vehicles, cooperative target localization and pursuit, synchronization of networked multiple robots, etc. The solutions proposed possess the following properties:

- distributed, i.e. agents (robots) only communicate with their neighbors. 
- event-triggered communications, i.e. agents only communicate with their neighbors when found necessary. 

<nbsp>

{% include base_path %}

{% assign ordered_pages = site.research | sort:"order_number" %}

{% for post in ordered_pages %}
  {% include archive-single.html type="grid" %}
{% endfor %}
