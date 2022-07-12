---
title: mp notes
layout: def
impMath: true
mainPage: true
---

# {{ page.title }}

![hello and wellcome](https://user-images.githubusercontent.com/43134602/178615284-b989ba77-0a98-429e-b25b-94cbdca20e2d.png)
<href="https://www.shadertoy.com/media/users/Mike_Permyakov/profile.jpeg"></a>

<br>

<iframe width="100%" height="166" scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/196944001&color=%233a4448&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true"></iframe><div style="font-size: 10px; color: #cccccc;line-break: anywhere;word-break: normal;overflow: hidden;white-space: nowrap;text-overflow: ellipsis; font-family: Interstate,Lucida Grande,Lucida Sans Unicode,Lucida Sans,Garuda,Verdana,Tahoma,sans-serif;font-weight: 100;"><a href="https://soundcloud.com/workingclassheroes_skinheadzine" title="WorkingClassHeroes (SHZ)" target="_blank" style="color: #cccccc; text-decoration: none;">WorkingClassHeroes (SHZ)</a> · <a href="https://soundcloud.com/workingclassheroes_skinheadzine/the-animals-the-house-of-the" title="The Animals  - The House Of The Rising Sun  (La Casa Del Sol Naciente)" target="_blank" style="color: #cccccc; text-decoration: none;">The Animals  - The House Of The Rising Sun  (La Casa Del Sol Naciente)</a></div>

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
