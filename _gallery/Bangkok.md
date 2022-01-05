---
title: "Bangkok-Thailand-Jan-2016"
layout: single-portfolio
excerpt: "[<img src='/images/gallery/Bangkok/DSC00704.JPG' alt=''>](https://nt-hung.github.io/gallery/Bangkok)"
collection: gallery
order_number: 6
---
<p float="left">   
{% for image in site.static_files %}
{% if image.path contains 'images/gallery/Bangkok' %}
<a href='{{ site.baseurl }}{{ image.path }}'>
    <img 
        src='{{ site.baseurl }}{{ image.path }}'
        alt="Bangkok, Thailand" width="245" title="Bangkok, Thailand"
    >
</a>
{% endif %}
{% endfor %}
</p>
<!-- [Poster](/files/pdf/research/PolMeth 2019 Poster.pdf){: .btn--research} -->
