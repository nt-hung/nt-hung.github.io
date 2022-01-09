---
title: "Pompei-Italy-July-2018"
layout: single-portfolio
excerpt: "[<img src='/images/gallery/Pompei/DSC01292.JPG' alt=''>](https://nt-hung.github.io/gallery/Pompei)"
collection: gallery
order_number: 10
---
<p float="left">   
{% for image in site.static_files %}
{% if image.path contains 'images/gallery/Pompei' %}
<a href='{{ site.baseurl }}{{ image.path }}'>
    <img 
        src='{{ site.baseurl }}{{ image.path }}'
        alt="Pompei, Italy" width="245" title="Pompei, Italy"
    >
</a>
{% endif %}
{% endfor %}
</p>
<!-- [Poster](/files/pdf/research/PolMeth 2019 Poster.pdf){: .btn--research} -->
