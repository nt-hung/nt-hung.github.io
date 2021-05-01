---
layout: archive
title: "Recent talks and presentations"
permalink: /talks/
author_profile: true
---
- European Marine Robotics Network, April 2021 (online).
    - **Title**: Cooperative Distributed Estimation and Control of Multiple Autonomous Vehicles for Range-Based Underwater Target Localization and Pursuit. [Slide](confidential) - [Web](https://www.eumarinerobots.eu/news/fifth-coffee-eumr-webinar)  
- Vietnamese Control System and Robotics, July 2020 (online).
    - **Title**: Cooperative Control of Multiple Autonomous Vehicles: A Gentle Introduction and Practical Applications. [Slide](/files/pdf/presentation/Hung_VNCR_2020.pdf) - [Video](https://www.facebook.com/groups/1240254362700264/permalink/3179867735405574/)  
- IFAC2020, Berlin, July 2020 (online).    
    - **Title**: Range-based Navigation and Target Localization: Observability Analysis and Guidelines for Motion Planning. [Slide](https://www.dropbox.com/s/qkwmucqrxvv0y83/Main_slide.pdf?dl=0) - [Video](https://www.youtube.com/watch?v=XS5U2FPjEXo&feature=youtu.be)
- European control conference, Naples, Italy, June 2019. 
    - **Title**: Event-Triggered Communications for the Synchronization of Nonlinear Multi Agent Systems on Weight-Balanced Digraphs. [Slide](https://www.dropbox.com/s/d8opr9mo3tkmxeg/Slide.pdf?dl=0)
- 6th IFAC Conference on Nonlinear Model Predictive Control, Wisconsin, USA, August 2018.
    - **Title**: Cooperative Path Following of Autonomous Vehicles with Model Predictive Control and Event Triggered Communications. [Slide](https://www.dropbox.com/s/4pnf9fr9e6a3mo5/Slide_NMPC2018.pdf?dl=0)
- The 11th IFAC Conference on Control Applications in Marine Systems, Robotics, and Vehicles– CAMS, Opatija, Croatia, September 2018.    
    - **Title**: Input-Constrained Path Following for Autonomous Marine Vehicles with a Global Region of Attraction. [Slide](https://www.dropbox.com/s/qotilch8e51yhvn/Hung_Presentation_CAMS2018.pdf?dl=0)     

{% if site.talkmap_link == true %}

<p style="text-decoration:underline;"><a href="/talkmap.html">See a map of all the places I've given a talk!</a></p>

{% endif %}

{% for post in site.talks reversed %}
  {% include archive-single-talk.html %}
{% endfor %}
