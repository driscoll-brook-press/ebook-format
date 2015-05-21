---
title: Title Page
guide: title-page
add_header: no
---
{% assign publication = site.data.publication %}
{% assign author = site.data.author %}
{% assign publisher = site.data.publisher %}

# {{ publication.title }}

## {{ author.name }}

### {{ publisher.name }}

ISBN: {{ publication.isbn }}

&copy; {{ publication.copyright.text.date }} {{ publication.copyright.text.owner }}

[Full Copyright Information](copyright.html)
