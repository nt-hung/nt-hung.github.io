---
title: "Evora-Portugal-March-2016"
layout: single-portfolio
excerpt: "[<img src='/images/gallery/Evora/DSC01070.JPG' alt=''>](https://nt-hung.github.io/gallery/Evora)"
collection: gallery
order_number: 6
---
<p float="left">   
{% for image in site.static_files %}
{% if image.path contains 'images/gallery/Evora' %}
<a href='{{ site.baseurl }}{{ image.path }}'>
    <img 
        src='{{ site.baseurl }}{{ image.path }}'
        alt="Evora, Portugal" width="245" title="Evora, Portugal"
    >
</a>
{% endif %}
{% endfor %}
</p>
<!-- [Poster](/files/pdf/research/PolMeth 2019 Poster.pdf){: .btn--research} -->
