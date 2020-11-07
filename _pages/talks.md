---
layout: archive
title: "Talks and presentations"
permalink: /talks/
author_profile: true
---
- VietNam Control and Robotics, July, 2020 (virtual)
    - Title: Cooperative control of MAS with event based communications: A gentle introduction and its applications in cooperative control of multiple autonomous vehicles. [Slide]()  
- European control conference 
    - Title: 

{% if site.talkmap_link == true %}

<p style="text-decoration:underline;"><a href="/talkmap.html">See a map of all the places I've given a talk!</a></p>

{% endif %}

{% for post in site.talks reversed %}
  {% include archive-single-talk.html %}
{% endfor %}
