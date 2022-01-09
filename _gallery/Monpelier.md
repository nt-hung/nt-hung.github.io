---
title: "Montpellier-France-May-2019"
layout: single-portfolio
excerpt: "[<img src='/images/gallery/Monpelier/DSC03793 (1280x960).jpg' alt=''>](https://nt-hung.github.io/gallery/Monpelier)"
collection: gallery
order_number: 6
---
<p float="left">   
{% for image in site.static_files %}
{% if image.path contains 'images/gallery/Monpelier' %}
<a href='{{ site.baseurl }}{{ image.path }}'>
    <img 
        src='{{ site.baseurl }}{{ image.path }}'
        alt="Monpelier, France" width="245" title="Monpelier, France"
    >
</a>
{% endif %}
{% endfor %}
</p>
<!-- [Poster](/files/pdf/research/PolMeth 2019 Poster.pdf){: .btn--research} -->
