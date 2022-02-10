---
title: mp notes
layout: def
impMath: true
postPage: false
---

# {{ page.title }}

![hello and wellcome](https://www.shadertoy.com/media/users/Mike_Permyakov/profile.jpeg)

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
