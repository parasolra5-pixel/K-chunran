---
layout: default
title: "품종 도감"
permalink: /varieties/
---

# 품종 도감

현재 K-Chunran에 수록된 전체 품종입니다.

<div class="kc-home-grid">
  <a class="kc-home-card" href="{{ '/varieties/named/' | relative_url }}">
    <strong>명명품</strong>
    <span>현재 등록된 품종을 명명 정보 기준으로 살펴봅니다.</span>
  </a>
  <a class="kc-home-card" href="{{ '/varieties/classification/' | relative_url }}">
    <strong>분류별 품종 찾기</strong>
    <span>현재 데이터의 대표 분류와 세부 형질을 기준으로 찾습니다.</span>
  </a>
</div>

<h2>전체 품종</h2>

{% for post in site.posts %}
  {% assign d = site.data.varieties[post.variety_id] %}
  {% if d %}
  - [{{ d.name }}{% if d.hanja %} ({{ d.hanja }}){% endif %}]({{ post.url | relative_url }})
  {% endif %}
{% endfor %}
