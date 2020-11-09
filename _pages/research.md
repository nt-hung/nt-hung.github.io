---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

My research tackles problems involving cooperative control and estimation of networked multi agent system under communication constraints. Each agent can be a mobile ground robot, an underwater autonomous vehicle (UAV), or simply, a sensor node. 
Due to the communication constraints on the topology of the inter-agent communication network, where each agent is only capable of exchanging information with a subset of agents in the network, the problems must be addressed in a distributed manner. The main goal is to design efficiently distributed control/estimation algorithms to address problems involving in the operation of MAS that include:

<nbsp>

{% include base_path %}

{% assign ordered_pages = site.research | sort:"order_number" %}

{% for post in ordered_pages %}
  {% include archive-single.html type="grid" %}
{% endfor %}
