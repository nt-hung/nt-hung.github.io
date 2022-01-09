---
title: "Chicago-USA-August-2018"
layout: single-portfolio
excerpt: "[<img src='/images/gallery/Chicago/DSC00007.jpg' alt=''>](https://nt-hung.github.io/gallery/Chicago)"
collection: gallery
order_number: 11
---
<p float="left">   
{% for image in site.static_files %}
{% if image.path contains 'images/gallery/Chicago' %}
<a href='{{ site.baseurl }}{{ image.path }}'>
    <img 
        src='{{ site.baseurl }}{{ image.path }}'
        alt="Chicago, USA" width="245" title="Chicago, USA"
    >
</a>
{% endif %}
{% endfor %}
</p>
<!-- [Poster](/files/pdf/research/PolMeth 2019 Poster.pdf){: .btn--research} -->
