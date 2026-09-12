---
layout: default
title: "품종 도감"
permalink: /varieties/
---

# 품종 도감

현재 K-Chunran에 수록된 전체 품종입니다.

{% for post in site.posts %}
  {% assign d = site.data.varieties[post.variety_id] %}
  {% if d %}
  - [{{ d.name }}{% if d.hanja %} ({{ d.hanja }}){% endif %}]({{ post.url | relative_url }})
  {% endif %}
{% endfor %}
