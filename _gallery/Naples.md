---
title: "Naples-Italy-August-2019"
layout: single-portfolio
excerpt: "[<img src='/images/gallery/Naples/DSC_0437.jpg' alt=''>](https://nt-hung.github.io/gallery/Naples)"
collection: gallery
order_number: 3
---
<p float="left">   
{% for image in site.static_files %}
{% if image.path contains 'images/gallery/Naples' %}
<a href='{{ site.baseurl }}{{ image.path }}'>
    <img 
        src='{{ site.baseurl }}{{ image.path }}'
        alt="Naples, Italy" width="245" title="Naples, Italy"
    >
</a>
{% endif %}
{% endfor %}
</p>
<!-- [Poster](/files/pdf/research/PolMeth 2019 Poster.pdf){: .btn--research} -->
