---
layout: default
title: "대한민국 춘란(K-Chunran) - 지식 도감 & AI 데이터베이스"
---

# 대한민국 춘란 (K-Chunran)

대한민국 난 등록협회 표준 체계 및 실제 유통 시장 데이터를 기반으로 구축된 **한국춘란 품종 도감 겸 AI 감정 학습용 데이터베이스**입니다.

## 카테고리

- **엽예품 (葉物):** 중투호, 복륜, 단엽, 서반, 산반
- **화예품 (花物):** 홍화, 황화, 소심, 복색화, 기화
- **유통 분류:** 명감 등록품 / 주거래 대중품 / 유전자 미발현품

## 품종 도감

현재 수록된 주요 품종입니다.

{% assign featured_ids = "sebo,hojung,silla,cheonjong,agassi" | split: "," %}
{% for variety_id in featured_ids %}
  {% assign d = site.data.varieties[variety_id] %}
  {% if d %}
  {% for post in site.posts %}
    {% if post.variety_id == variety_id %}
    - [{{ d.name }}{% if d.hanja %} ({{ d.hanja }}){% endif %}]({{ post.url | relative_url }})
    {% endif %}
  {% endfor %}
  {% endif %}
{% endfor %}

[전체 품종 보기]({{ '/varieties/' | relative_url }})
