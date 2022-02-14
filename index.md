---
title: mp notes
layout: def
impMath: true
mainPage: true
---

# {{ page.title }}

![hello and wellcome](https://www.shadertoy.com/media/users/Mike_Permyakov/profile.jpeg)

<br>

<iframe width="396" height="100" scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/1065986050&color=%00000000&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true&visual=true"></iframe><div style="font-size: 10px; color: #cccccc;line-break: anywhere;word-break: normal;overflow: hidden;white-space: nowrap;text-overflow: ellipsis; font-family: Interstate,Lucida Grande,Lucida Sans Unicode,Lucida Sans,Garuda,Verdana,Tahoma,sans-serif;font-weight: 100;"><a href="https://soundcloud.com/bo-burnham" title="Bo Burnham" target="_blank" style="color: #cccccc; text-decoration: none;">Bo Burnham</a> · <a href="https://soundcloud.com/bo-burnham/shit" title="Shit" target="_blank" style="color: #cccccc; text-decoration: none;">Shit</a></div>

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
