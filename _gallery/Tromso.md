---
title: "Tromso-Norway-April-2016"
layout: single-portfolio
excerpt: "<img src='/images/gallery/Tromso/DSC01189.JPG' alt=''>"
collection: gallery
order_number: 6
---
{% for image in site.static_files %}
    {% if image.path contains 'images/gallery/Tromso' %}
    <img src='{{ site.baseurl }}{{ image.path }}' 
         alt='image' />
    {% endif %}
{% endfor %}
