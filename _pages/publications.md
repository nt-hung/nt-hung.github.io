---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

## Journal
-  Nguyen T. Hung, Antonio M. Pascoal, "Consensus/synchronization of networked nonlinear
multiple agent systems with event-triggered communications", International Journal of Control,
2020
- Nguyen T. Hung, Antonio M. Pascoal, Tor A. Johansen, "Cooperative path following of constrained autonomous vehicles with model predictive control and event-triggered communications",
International Journal of Robust Nonlinear Control, 2020; 30: 2644– 2670
- Nguyen T. Hung, N. Crasta, David Moreno-Salinas, António M. Pascoal, Tor A. Johansen,
"Range-based target localization and pursuit with autonomous vehicles: An approach using
posterior CRLB and model predictive control", Robotics and Autonomous Systems, Volume 132,
2020, 103608, ISSN 0921-8890. [download](https://welcome.isr.tecnico.ulisboa.pt/author/antoniomanueldossantos/)
-  


{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}

<sup>*</sup> Equal authorship statement