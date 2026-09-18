---
layout: default
title: "명명품"
permalink: /varieties/named/
---

<section class="kc-page-hero kc-named-hero">
  <div>
    <p class="kc-page-kicker">VARIETY CATALOG · NAMED</p>
    <h1>명명품</h1>
    <p class="kc-page-lead">이름과 등록 정보가 기록된 한국춘란 품종을 한곳에서 살펴봅니다.</p>
    <p class="kc-page-copy">품종의 이름을 시작점으로 도감 정보를 확인하고, 이후 형질·이미지·AI 데이터로 연결할 수 있도록 구성합니다.</p>
  </div>
  <div class="kc-page-summary">
    <span class="kc-page-summary-label">현재 수록</span>
    <strong>
      {% assign named_count = 0 %}
      {% for post in site.posts %}
        {% assign d = site.data.varieties[post.variety_id] %}
        {% if d and d.registration.status %}
          {% assign named_count = named_count | plus: 1 %}
        {% endif %}
      {% endfor %}
      {{ named_count }}
    </strong>
    <span>명명·등록 정보 기록 품종</span>
  </div>
</section>

<section class="kc-page-section">
  <div class="kc-section-heading">
    <div>
      <p class="kc-section-kicker">NAMED VARIETIES</p>
      <h2>품종 목록</h2>
    </div>
    <p class="kc-section-note">이름을 선택하면 해당 품종의 상세 도감으로 이동합니다.</p>
  </div>

  <div class="kc-named-grid">
    {% for post in site.posts %}
      {% assign d = site.data.varieties[post.variety_id] %}
      {% if d and d.registration.status %}
        <a class="kc-named-card" href="{{ post.url | relative_url }}">
          <div class="kc-named-card-image">
            <span>IMAGE</span>
            <small>품종 이미지</small>
          </div>
          <div class="kc-named-card-body">
            <p class="kc-named-status">{{ d.registration.status }}</p>
            <h3>{{ d.name }}{% if d.hanja %} <span>{{ d.hanja }}</span>{% endif %}</h3>
            <p class="kc-named-link">품종 상세 보기 <span aria-hidden="true">→</span></p>
          </div>
        </a>
      {% endif %}
    {% endfor %}
  </div>
</section>

<section class="kc-page-section kc-named-next">
  <div>
    <p class="kc-section-kicker">NEXT CONNECTION</p>
    <h2>명명품에서 AI 데이터로</h2>
    <p>현재는 이름과 등록 정보를 중심으로 정리하고, 이후 실제 품종 이미지와 형질 데이터를 연결해 품종별 데이터 구조를 확장합니다.</p>
  </div>
  <a class="kc-hero-button" href="{{ '/ai/' | relative_url }}">AI 데이터 보기</a>
</section>
