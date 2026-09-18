---
layout: default
title: "품종 도감"
permalink: /varieties/
---

<section class="kc-leaf-hero kc-varieties-hero">
  <div>
    <p class="kc-page-kicker">VARIETY CATALOG</p>
    <h1>품종 도감</h1>
    <p class="kc-page-lead">한국춘란의 품종을 분류와 형질을 기준으로 살펴봅니다.</p>
    <p class="kc-page-copy">엽예품·화예품의 주요 분류와 세부 형질을 따라가거나, 현재 수록된 전체 품종에서 바로 선택할 수 있습니다.</p>
  </div>
  <div class="kc-leaf-flow">
    <span>분류</span><i>→</i><span>형질</span><i>→</i><span>품종</span>
  </div>
</section>

<section class="kc-leaf-section kc-varieties-entry">
  <div class="kc-section-heading">
    <div>
      <p class="kc-section-kicker">CATALOG NAVIGATION</p>
      <h2>도감 둘러보기</h2>
    </div>
    <p class="kc-section-note">분류 또는 전체 품종에서 시작할 수 있습니다.</p>
  </div>

  <div class="kc-home-grid">
    <a class="kc-home-card" href="{{ '/varieties/leaf/' | relative_url }}">
      <span class="kc-card-index">01</span>
      <strong>엽예품</strong>
      <span>중투·복륜·산반·호·서반·단엽 등 잎의 형질을 기준으로 살펴봅니다.</span>
    </a>
    <a class="kc-home-card" href="{{ '/varieties/flower/' | relative_url }}">
      <span class="kc-card-index">02</span>
      <strong>화예품</strong>
      <span>홍화·황화·소심·복색화·기화 등 꽃의 형질을 기준으로 살펴봅니다.</span>
    </a>
    <a class="kc-home-card" href="{{ '/varieties/classification/' | relative_url }}">
      <span class="kc-card-index">03</span>
      <strong>분류별 품종 찾기</strong>
      <span>대표 분류와 잎의 세부 형질을 나누어 품종을 찾아봅니다.</span>
    </a>
  </div>
</section>

<section class="kc-leaf-section kc-varieties-list">
  <div class="kc-section-heading">
    <div>
      <p class="kc-section-kicker">ALL VARIETIES</p>
      <h2>전체 품종</h2>
    </div>
    <p class="kc-section-note">현재 데이터에 연결된 품종입니다.</p>
  </div>

  <div class="kc-variety-list">
    {% for post in site.posts %}
      {% assign d = site.data.varieties[post.variety_id] %}
      {% if d %}
      <a class="kc-variety-list-item" href="{{ post.url | relative_url }}">
        <strong>{{ d.name }}</strong>
        {% if d.hanja %}<span>{{ d.hanja }}</span>{% endif %}
        <i>→</i>
      </a>
      {% endif %}
    {% endfor %}
  </div>
</section>
