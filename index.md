---
title: mp notes
layout: def
impMath: true
mainPage: true
---

# {{ page.title }}

Привет, путник 👋

![hello and wellcome](https://dovobu.github.io/ava.jpg)

Меня зовут Михаил, я технический художник и программист.

<p style="text-align:center"><i>Добро пожаловать на мою страницу!</i></p>

Выкладываю тут что по-кайфу, и в идеале собираю полезный для тебя ресурс.

Распологайся, будь как дома, вон тут совсем рядом записи отсортированные по категориям)

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

Ну чё, заинтересовало что-нибудь?)

Если чего-то не хватает, или хочешь обсудить что-нибудь подробнее с реальным живым мной, то вот, <a href="https://t.me/d0c_0b_p">держи мой контакт в tg)</a>

Будем на связи) 🤙

