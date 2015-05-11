---
title: Books by the Author
style: books
categories:
-
  name: Fantasy
  books:
  -
    title: Carrion Road
    slug: carrion-road
  -
    title: Funhouse
    slug: funhouse
  -
    title: Refund
    slug: refund
  -
    title: Tailor's Tears
    slug: tailors-tears
  -
    title: Yantriels Privy
    slug: yantriels-privy
-
  name: Crime Fiction
  books:
  -
    title: Double or Nothing
    slug: double-or-nothing
  -
    title: The Last Whiskey Bacon Cheddar Burger at Saint Florian's Abbey
    slug: saint-florians-abbey
-
  name: Collections
  books:
  -
    title: Winding Unwinding
    slug: winding-unwinding
---

{% for category in page.categories %}
## {{ category.name }}
{% for book in category.books %}
*[{{ book.title }}](http://DriscollBrookPress.com/title/{{ book.slug }}/)*
{% endfor %}
{% endfor %}
