---
title: "Lisbon-Portugal-2016-2022"
layout: single-portfolio
excerpt: "[<img src='/images/gallery/Lisbon/DSC02466.JPG' alt=''>](https://nt-hung.github.io/gallery/Lisbon)"
collection: gallery
order_number: 2
---
<p float="left">   
{% for image in site.static_files %}
{% if image.path contains 'images/gallery/Lisbon' %}
<a href='{{ site.baseurl }}{{ image.path }}'>
    <img 
        src='{{ site.baseurl }}{{ image.path }}'
        alt="Lisbon, Portugal" width="245" title="Lisbon, Portugal"
    >
</a>
{% endif %}
{% endfor %}
</p>
<!-- [Poster](/files/pdf/research/PolMeth 2019 Poster.pdf){: .btn--research} -->
