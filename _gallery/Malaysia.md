---
title: "Several places in Malaysia-2012-2014"
layout: single-portfolio
excerpt: "[<img src='/images/gallery/Malaysia/WP_001549.jpg' alt=''>](https://nt-hung.github.io/gallery/Malaysia)"
collection: gallery
order_number: 7
---
<p float="left">   
{% for image in site.static_files %}
{% if image.path contains 'images/gallery/Malaysia' %}
<a href='{{ site.baseurl }}{{ image.path }}'>
    <img 
        src='{{ site.baseurl }}{{ image.path }}'
        alt="Various places, Malaysia" width="245" title="Various places, Malaysia"
    >
</a>
{% endif %}
{% endfor %}
</p>
<!-- [Poster](/files/pdf/research/PolMeth 2019 Poster.pdf){: .btn--research} -->
