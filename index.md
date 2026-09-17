---
layout: default
title: "대한민국 춘란(K-Chunran) - 지식 도감 & AI 데이터베이스"
---

<div class="kc-hero">
  <p class="kc-hero-kicker">K-Chunran</p>
  <p class="kc-hero-title">한국춘란을 체계적으로 기록합니다.</p>
  <p class="kc-hero-copy">품종의 분류와 형질, 유통 정보, 이미지를 하나의 구조로 정리합니다.</p>
  <a class="kc-hero-link" href="{{ '/varieties/' | relative_url }}">품종 도감 보기</a>
</div>

<section class="kc-home-section">
  <h2>주요 분류</h2>
  <div class="kc-home-grid">
    <a class="kc-home-card" href="{{ '/varieties/' | relative_url }}">
      <strong>엽예품 (葉物)</strong>
      <span>중투호 · 복륜 · 단엽 · 서반 · 산반</span>
    </a>
    <a class="kc-home-card" href="{{ '/varieties/' | relative_url }}">
      <strong>화예품 (花物)</strong>
      <span>홍화 · 황화 · 소심 · 복색화 · 기화</span>
    </a>
    <a class="kc-home-card" href="{{ '/varieties/' | relative_url }}">
      <strong>분류체계</strong>
      <span>잎 형태 · 무늬 · 잎끝 형태 · 품종 분류</span>
    </a>
    <a class="kc-home-card" href="{{ '/varieties/' | relative_url }}">
      <strong>AI 데이터</strong>
      <span>이미지 데이터 · 데이터 구조 · 학습용 정보</span>
    </a>
  </div>
</section>

<section class="kc-home-section">
  <h2>대표 품종</h2>
  <div class="kc-home-varieties">
    {% assign featured_ids = "sebo,hojung,silla,cheonjong,agassi" | split: "," -%}
    {% for variety_id in featured_ids -%}
      {% assign d = site.data.varieties[variety_id] -%}
      {% if d -%}
        {% for post in site.posts -%}
          {% if post.variety_id == variety_id -%}
            <a class="kc-variety-link" href="{{ post.url | relative_url }}">
              {{ d.name }}{% if d.hanja %} <span>({{ d.hanja }})</span>{% endif %}
            </a>
          {%- endif %}
        {%- endfor %}
      {%- endif %}
    {%- endfor %}
  </div>
</section>

<section class="kc-home-section kc-home-final">
  <h2>유통 분류</h2>
  <p>명감 등록품 · 주거래 대중품 · 유전자 미발현품</p>
  <a class="kc-text-link" href="{{ '/varieties/' | relative_url }}">전체 품종 보기 →</a>
</section>
