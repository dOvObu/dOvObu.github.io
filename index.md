---
title: mp notes
layout: def
impMath: true
mainPage: true
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
<br>
<br>
<iframe width="100%" height="300" scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/115435445&color=%23000000&auto_play=true&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true&visual=true"></iframe><div style="font-size: 10px; color: #cccccc;line-break: anywhere;word-break: normal;overflow: hidden;white-space: nowrap;text-overflow: ellipsis; font-family: Interstate,Lucida Grande,Lucida Sans Unicode,Lucida Sans,Garuda,Verdana,Tahoma,sans-serif;font-weight: 100;"><a href="https://soundcloud.com/anton-vosmoy-8th" title="Anton Vosmoy-8th" target="_blank" style="color: #cccccc; text-decoration: none;">Anton Vosmoy-8th</a> · <a href="https://soundcloud.com/anton-vosmoy-8th/bonus-track" title="VOSMOY (Чувствилище) - Конечности (bonus track)" target="_blank" style="color: #cccccc; text-decoration: none;">VOSMOY (Чувствилище) - Конечности (bonus track)</a></div>
