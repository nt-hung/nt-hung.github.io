---
title: "Trondheim-Norway-April-2016"
layout: single-portfolio
excerpt: "[<img src='/images/gallery/Trondheim/DSC01292.JPG' alt=''>](https://nt-hung.github.io/gallery/Trondheim)"
collection: gallery
order_number: 6
---
<p float="left">   
{% for image in site.static_files %}
{% if image.path contains 'images/gallery/Trondheim' %}
<a href='{{ site.baseurl }}{{ image.path }}'>
    <img 
        src='{{ site.baseurl }}{{ image.path }}'
        alt="Trondheim, Norway" width="245" title="Trondheim, Norway"
    >
</a>
{% endif %}
{% endfor %}
</p>
<!-- [Poster](/files/pdf/research/PolMeth 2019 Poster.pdf){: .btn--research} -->
