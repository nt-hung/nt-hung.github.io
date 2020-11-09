---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

My research tackles problems involving the cooperative control and estimation of networked multi agent systems under communication constraints. Each agent can be a mobile ground robot, an underwater autonomous vehicle (UAV), or simply, a sensor node. Applications include vehicle formation control, cooperative target localization, synchronization of networked multiple robots, ... etc. Due to the communication constraints on the topology of the inter-agent communication network, where each agent is only capable of exchanging information with a subset of agents in the network, the problems must be addressed in a distributed manner. In my research, event-triggered communication (ETC) mechanisms are introduced to reduce communications among the agents while theoretically, performance on the cooperative network is still preserved. These ETC mechanisms are of utmost importance for the networks that have limited bandwidth such as acoustic communication networks in underwater environment.  

<nbsp>

{% include base_path %}

{% assign ordered_pages = site.research | sort:"order_number" %}

{% for post in ordered_pages %}
  {% include archive-single.html type="grid" %}
{% endfor %}
