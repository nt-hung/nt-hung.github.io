---
title: "Tromso-Norway-April-2016"
layout: single-portfolio
excerpt: "[<img src='/images/gallery/Tromso/DSC01189.JPG' alt=''>](https://nt-hung.github.io/gallery/Tromso)"
collection: gallery
order_number: 6
---
<p float="left">   
{% for image in site.static_files %}
{% if image.path contains 'images/gallery/Tromso' %}
<a href='{{ site.baseurl }}{{ image.path }}'>
    <img 
        src='{{ site.baseurl }}{{ image.path }}'
        alt="Tromso, Norway" width="280" title="Tromso, Norway"
    >
</a>
{% endif %}
{% endfor %}
</p>
<!-- [Poster](/files/pdf/research/PolMeth 2019 Poster.pdf){: .btn--research} -->
