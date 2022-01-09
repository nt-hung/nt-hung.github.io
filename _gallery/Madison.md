---
title: "Madison-USA-August-2018"
layout: single-portfolio
excerpt: "[<img src='/images/gallery/Madison/DSC03242.jpg' alt=''>](https://nt-hung.github.io/gallery/Madison)"
collection: gallery
order_number: 5
---
<p float="left">   
{% for image in site.static_files %}
{% if image.path contains 'images/gallery/Madison' %}
<a href='{{ site.baseurl }}{{ image.path }}'>
    <img 
        src='{{ site.baseurl }}{{ image.path }}'
        alt="Madison, USA" width="245" title="Madison, USA"
    >
</a>
{% endif %}
{% endfor %}
</p>
<!-- [Poster](/files/pdf/research/PolMeth 2019 Poster.pdf){: .btn--research} -->
