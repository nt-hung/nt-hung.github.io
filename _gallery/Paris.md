---
title: "Paris-France-Sep-2016"
layout: single-portfolio
excerpt: "[<img src='/images/gallery/Paris/DSC_1242.JPG' alt=''>](https://nt-hung.github.io/gallery/Paris)"
collection: gallery
order_number: 7
---
<p float="left">   
{% for image in site.static_files %}
{% if image.path contains 'images/gallery/Paris' %}
<a href='{{ site.baseurl }}{{ image.path }}'>
    <img 
        src='{{ site.baseurl }}{{ image.path }}'
        alt="Paris, France" width="280" title="Paris, France"
    >
</a>
{% endif %}
{% endfor %}
</p>
<!-- [Poster](/files/pdf/research/PolMeth 2019 Poster.pdf){: .btn--research} -->
