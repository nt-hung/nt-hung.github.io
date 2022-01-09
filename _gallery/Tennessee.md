---
title: "Tennessee-USA-August-2018"
layout: single-portfolio
excerpt: "[<img src='/images/gallery/Tennessee/DSC03360.jpg' alt=''>](https://nt-hung.github.io/gallery/Tennessee)"
collection: gallery
order_number: 11
---
<p float="left">   
{% for image in site.static_files %}
{% if image.path contains 'images/gallery/Tennessee' %}
<a href='{{ site.baseurl }}{{ image.path }}'>
    <img 
        src='{{ site.baseurl }}{{ image.path }}'
        alt="Tennessee, USA" width="245" title="Tennessee, USA"
    >
</a>
{% endif %}
{% endfor %}
</p>
<!-- [Poster](/files/pdf/research/PolMeth 2019 Poster.pdf){: .btn--research} -->
