---
layout: default
title: "대한민국 춘란(K-Chunran) - 지식 도감 & AI 데이터베이스"
---

<div class="kc-hero">
  <div class="kc-hero-copy-wrap">
    <p class="kc-hero-kicker">K-Chunran</p>
    <h1 class="kc-hero-title">대한민국 춘란</h1>
    <p class="kc-hero-lead">한국춘란을 기록하고, 이해하고, 연결합니다.</p>
    <p class="kc-hero-copy">품종의 분류와 형질, 유통 정보, 이미지를 하나의 구조로 정리합니다.</p>
    <div class="kc-hero-actions">
      <a class="kc-hero-button kc-hero-button-primary" href="{{ '/varieties/' | relative_url }}">품종 찾아보기</a>
      <a class="kc-hero-button" href="{{ '/ai/dataset/' | relative_url }}">AI 데이터 보기</a>
    </div>
  </div>
  <div class="kc-hero-visual" aria-label="대표 춘란 이미지 영역">
    <div class="kc-image-placeholder kc-hero-image-placeholder">
      <span>대표 춘란 이미지 영역</span>
      <small>실제 이미지 데이터 연결 예정</small>
    </div>
    <div class="kc-hero-structure" aria-label="K-Chunran 데이터 연결 구조">
      <span>사진</span><i aria-hidden="true">→</i><span>형질</span><i aria-hidden="true">→</i>
      <span>분류</span><i aria-hidden="true">→</i><span>품종</span><i aria-hidden="true">→</i><span>AI 데이터</span>
    </div>
  </div>
</div>

<section class="kc-home-section">
  <div class="kc-section-heading">
    <div><p class="kc-section-kicker">EXPLORE</p><h2>주요 분류</h2></div>
    <a class="kc-section-link" href="{{ '/varieties/' | relative_url }}">전체 품종 보기 →</a>
  </div>
  <div class="kc-home-grid">
    <a class="kc-home-card" href="{{ '/varieties/leaf/' | relative_url }}">
      <span class="kc-card-index">01</span><strong>엽예품 (葉物)</strong><span>중투호 · 복륜 · 단엽 · 서반 · 산반</span>
    </a>
    <a class="kc-home-card" href="{{ '/varieties/flower/' | relative_url }}">
      <span class="kc-card-index">02</span><strong>화예품 (花物)</strong><span>홍화 · 황화 · 소심 · 복색화 · 기화</span>
    </a>
    <a class="kc-home-card" href="{{ '/varieties/classification/' | relative_url }}">
      <span class="kc-card-index">03</span><strong>분류체계</strong><span>잎 형태 · 무늬 · 잎끝 형태 · 품종 분류</span>
    </a>
    <a class="kc-home-card" href="{{ '/ai/dataset/' | relative_url }}">
      <span class="kc-card-index">04</span><strong>AI 데이터</strong><span>이미지 데이터 · 데이터 구조 · 학습용 정보</span>
    </a>
  </div>
</section>

<section class="kc-home-section">
  <div class="kc-section-heading"><div><p class="kc-section-kicker">CULTIVARS</p><h2>대표 품종</h2></div></div>
  <div class="kc-variety-grid">
    {% assign featured_ids = "sebo,hojung,silla,cheonjong,agassi" | split: "," -%}
    {% for variety_id in featured_ids -%}
      {% assign d = site.data.varieties[variety_id] -%}
      {% if d -%}
        {% for post in site.posts -%}
          {% if post.variety_id == variety_id -%}
            <a class="kc-variety-card" href="{{ post.url | relative_url }}">
              <div class="kc-image-placeholder kc-variety-image-placeholder">
                <span>품종 이미지 영역</span><small>실제 이미지 연결 예정</small>
              </div>
              <span class="kc-variety-card-top">품종 도감</span>
              <strong>{{ d.name }}</strong>
              {% if d.hanja %}<span class="kc-variety-hanja">{{ d.hanja }}</span>{% endif %}
              <span class="kc-variety-arrow" aria-hidden="true">→</span>
            </a>
          {%- endif %}
        {%- endfor %}
      {%- endif %}
    {%- endfor %}
  </div>
</section>

<section class="kc-home-section kc-home-final">
  <div class="kc-section-heading"><div><p class="kc-section-kicker">DATA FLOW</p><h2>춘란 지식과 AI 데이터를 연결합니다</h2></div></div>
  <div class="kc-data-flow">
    <a href="{{ '/knowledge/leaf/' | relative_url }}"><strong>형질</strong><span>잎 · 무늬 · 꽃</span></a>
    <span class="kc-data-flow-arrow" aria-hidden="true">→</span>
    <a href="{{ '/varieties/classification/' | relative_url }}"><strong>분류</strong><span>체계와 기준</span></a>
    <span class="kc-data-flow-arrow" aria-hidden="true">→</span>
    <a href="{{ '/varieties/' | relative_url }}"><strong>품종</strong><span>실제 도감 페이지</span></a>
    <span class="kc-data-flow-arrow" aria-hidden="true">→</span>
    <a href="{{ '/ai/dataset/' | relative_url }}"><strong>AI 데이터</strong><span>이미지 · 학습 정보</span></a>
  </div>
</section>

<section class="kc-home-section kc-home-final">
  <h2>유통 분류</h2><p>명감 등록품 · 주거래 대중품 · 유전자 미발현품</p>
  <a class="kc-text-link" href="{{ '/varieties/' | relative_url }}">전체 품종 보기 →</a>
</section>
