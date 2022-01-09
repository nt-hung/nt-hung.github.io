---
title: "Berlin-Germany-May-2017"
layout: single-portfolio
excerpt: "[<img src='/images/gallery/Berlin/DSC02686.JPG' alt=''>](https://nt-hung.github.io/gallery/Berlin)"
collection: gallery
order_number: 15
---
<p float="left">   
{% for image in site.static_files %}
{% if image.path contains 'images/gallery/Berlin' %}
<a href='{{ site.baseurl }}{{ image.path }}'>
    <img 
        src='{{ site.baseurl }}{{ image.path }}'
        alt="Berlin, Germany" width="245" title="Berlin, Germany"
    >
</a>
{% endif %}
{% endfor %}
</p>
<!-- [Poster](/files/pdf/research/PolMeth 2019 Poster.pdf){: .btn--research} -->
