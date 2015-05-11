---
title: Title Page
guide: title-page
add_header: no
...

{{ site.markdown }}
{% assign book = site.data.book %}
# {{ book.title }}
{% for author in book.authors %}
## {{ author.name }}
{% endfor%}
### {{ book.publisher.name }}
ISBN: {{ book.isbn }}

{{ book.copyright.first }}

[Full Copyright Information](copyright.html)
