---
title: About the Author
style: about
toc: back-matter
stories:
-
  title: Carrion Road
  slug: carrion-road
-
  title: Yantriel's Privy
  slug: yantriels-privy
-
  title: The Last Whiskey Bacon Cheddar Burger at Saint Florian's Abbey
  slug: saint-florians-abbey
...
{% assign author = site.data.author %}
Dale Hartley Emery
writes fiction in a variety of genres,
including fantasy, science fiction, and mystery.
His short stories include
{% for story in page.stories %}{% unless forloop.first %}, {% endunless %}{% if forloop.last %}and {% endif %}*[{{ story.title }}](http://DriscollBrookPress.com/title/{{ story.slug }}/)*{% endfor %}

Dale has worked as a failed shoemaker,
reluctant dairy farmer,
and ruthless ice cream man.
For several years he monitored the nuclear test ban treaty,
making sure those pesky commies didn’t blow up the planet.
(They didn’t.)

When he isn’t writing,
Dale advises software teams and leaders about how to play nice together.
Colleagues in Dale’s industry once created a special award for him for being reasonable.

Dale lives in California with his wife.

Visit [{{ author.site }}]({{ author.url }}) to learn more.
