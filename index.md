---
title: mp notes
layout: def
impMath: true
mainPage: true
---

# {{ page.title }}

![hello and wellcome](ava.jpg)

<br>

это просто моя записная книжка

она не должна быть красивой, или сложной

самое главное тут, это удобство поиска и заполнения

<br>
{% for category in site.categories %}
    {% capture category_name %}{{ category | first }}{% endcapture %}
  <details open>
    <summary> {{ category_name }} </summary>
    <ul>
    {% for post in site.categories[category_name] %}
        <li><a href="{{ post.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
    </ul>
  </details>
{% endfor %}
<br>
