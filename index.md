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

    {% for post in site.categories[category_name] %}

<a href="{{ post.baseurl }}{{ post.url }}">→ → {{ post.title }}</a>

    {% endfor %}
  </details>
{% endfor %}

test content 8
