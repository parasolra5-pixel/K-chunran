---
layout: default
title: "명명품"
permalink: /varieties/named/
---

# 명명품

현재 K-Chunran에 수록된 품종 가운데 명명·등록 정보가 기록된 품종을 모아보는 공간입니다.

{% for post in site.posts %}
  {% assign d = site.data.varieties[post.variety_id] %}
  {% if d and d.registration.status %}
  - [{{ d.name }}{% if d.hanja %} ({{ d.hanja }}){% endif %}]({{ post.url | relative_url }}) — {{ d.registration.status }}
  {% endif %}
{% endfor %}
