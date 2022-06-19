---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

My research tackles problems involving motion planing, control, and estimation of networked multi-agent systems. Each agent can be a mobile ground robot, an autonomous aerial/marine vehicle (AUV), or simply, a sensor node. Applications include formation control of multiple autonomous vehicles, cooperative target localization and pursuit, synchronization of networked multiple autonomous vehicles, etc. The solutions proposed possess the following properties:

- distributed, i.e. agents (e.g. robots, vehicles) only communicate with their neighbors. 
- event-triggered communications, i.e. agents only communicate with their neighbors when found necessary. 

Some algorithms developed have been tested succefully with real ground and marine autonomous vehicles, that can be seen in research pages.
<nbsp>

{% include base_path %}

{% assign ordered_pages = site.research | sort:"order_number" %}

{% for post in ordered_pages %}
  {% include archive-single.html type="grid" %}
{% endfor %}
