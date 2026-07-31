---
layout: default
title: 江浙沪9日旅游计划
---

# 江浙沪9日旅游计划

欢迎来到我的行程合集。下面是收集的行程：

<ul>
{% for it in site.itineraries %}
  <li style="margin-bottom:1.25rem;">
    <a href="{{ it.url }}">{{ it.title }}</a> — {{ it.start_date }}{% if it.end_date %} — {{ it.end_date }}{% endif %}
    {% if it.photos and it.photos.size > 0 %}
      <br><img src="{{ it.photos[0] }}" alt="{{ it.title }}" style="max-width:240px; border-radius:6px; margin-top:6px;">
    {% endif %}
    <p>{{ it.excerpt }}</p>
    <p><a href="https://github.com/Cedric-01/9-day-travel-itinerary-for-JZH/new/main?_filename=_itineraries/{{ it.path | split: '/' | last }}">在 GitHub 新建/上传此行程（New）</a> · <a href="https://github.com/Cedric-01/9-day-travel-itinerary-for-JZH/edit/main/{{ it.path }}">编辑此行程</a></p>
  </li>
{% endfor %}
</ul>

<p>要添加新行程，点击上面的“在 GitHub 新建/上传此行程（New）”。如需帮助我可以为你创建模板文件。</p>
