---
layout: default
title: "엽예품"
permalink: /varieties/leaf/
---

# 엽예품

현재 품종 데이터에서 잎 형질이 기록된 품종을 확인합니다. 이 페이지는 별도의 품종 분류값을 새로 만들지 않고 기존 `traits.leaf` 데이터를 기준으로 보여줍니다.

{% for post in site.posts %}
  {% assign d = site.data.varieties[post.variety_id] %}
  {% if d and d.traits.leaf %}
  - [{{ d.name }}{% if d.hanja %} ({{ d.hanja }}){% endif %}]({{ post.url | relative_url }}) — {{ d.traits.leaf.form | default: '잎 형질 기록 있음' }}
  {% endif %}
{% endfor %}
