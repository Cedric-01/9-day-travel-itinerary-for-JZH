---
layout: default
title: 江浙沪9日旅游计划
---

欢迎来到我的行程合集。下面是收集的行程：

<ul class="it-list">
{% for it in site.itineraries %}
  <li class="it-item">
    <a class="it-link" href="{{ it.url }}">{{ it.title }}</a>
    <div class="it-meta">{{ it.start_date }}{% if it.end_date %} — {{ it.end_date }}{% endif %}</div>
    {% if it.photos and it.photos.size > 0 %}
      <img class="it-thumb" src="{{ it.photos[0] }}" alt="{{ it.title }}">
    {% endif %}
    <p class="it-excerpt">{{ it.excerpt }}</p>
    <p class="it-actions">
      <a href="https://github.com/Cedric-01/9-day-travel-itinerary-for-JZH/new/main?_filename=_itineraries/{{ it.path | split: '/' | last }}">新建/上传此行程 (New)</a>
      · <a href="https://github.com/Cedric-01/9-day-travel-itinerary-for-JZH/edit/main/{{ it.path }}">编辑此行程</a>
    </p>
  </li>
{% endfor %}
</ul>

<p>要添加新行程，点击上面的“新建/上传此行程 (New)”。如需帮助我可以为你创建模板文件。</p>
