---
title: test markdown gh pages
layout: home
---


<h1>{{ page.title }}</h1>


<ul>

{% for post in site.posts %}

<li><a href="{{ post.url }}">{{ post.title }}</li>

{% endfor %}

</ul>

test content 3
