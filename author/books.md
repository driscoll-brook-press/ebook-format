---
title: Books by the Author
style: books
toc: back-matter
categories:
- name: Fiction
  books:
  - title: The Donation
    slug: donation
  - title: Inventory
    slug: inventory
- name: Fantasy
  books:
  - title: Carrion Road
    slug: carrion-road
  - title: Funhouse
    slug: funhouse
  - title: Refund
    slug: refund
  - title: Tailor's Tears
    slug: tailors-tears
  - title: Winding Unwinding (Collection)
    slug: winding-unwinding
  - title: Yantriels Privy
    slug: yantriels-privy
- name: Crime Fiction
  books:
  - title: Double or Nothing
    slug: double-or-nothing
  - title: The Last Whiskey Bacon Cheddar Burger at Saint Florian's Abbey
    slug: saint-florians-abbey
---

{% for category in page.categories %}
## {{ category.name }}
{% for book in category.books %}
*[{{ book.title }}](http://DriscollBrookPress.com/title/{{ book.slug }}/)*
{% endfor %}
{% endfor %}
