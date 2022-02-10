---
title: mp notes
layout: def
impMath: true
---

# {{ page.title }}

{% for category in site.categories %}
    {% capture category_name %}{{ category | first }}{% endcapture %}
  <details>
    <summary> {{ category_name }} </summary>
    <ul>
    {% for post in site.categories[category_name] %}
        <li><a href="{{ post.baseurl }}{{ post.url }}">→ {{ post.title }}</a></li>
    {% endfor %}
    </ul>
  </details>
{% endfor %}

test content 8
