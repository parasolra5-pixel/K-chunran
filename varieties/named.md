---
layout: default
title: "명명품"
permalink: /varieties/named/
---

<section class="kc-leaf-hero kc-named-hero">
  <div>
    <p class="kc-page-kicker">VARIETY CATALOG · NAMED</p>
    <h1>명명품</h1>
    <p class="kc-page-lead">이름과 등록 정보가 확인된 한국춘란 품종을 한곳에서 살펴봅니다.</p>
    <p class="kc-page-copy">명명·등록 상태를 기준으로 품종을 모아 보고, 분류와 세부 형질을 확인한 뒤 각 품종의 상세 도감으로 이어집니다.</p>
  </div>
  <div class="kc-named-guide">
    <span>이름</span><i>→</i><span>등록</span><i>→</i><span>품종</span>
  </div>
</section>

<section class="kc-leaf-section kc-named-section">
  <div class="kc-section-heading">
    <div>
      <p class="kc-section-kicker">NAMED VARIETIES</p>
      <h2>명명·등록 품종</h2>
    </div>
    <p class="kc-section-note">현재 데이터에서 등록 정보가 확인된 품종입니다.</p>
  </div>

  <div class="kc-named-list">
    {% for post in site.posts %}
      {% assign d = site.data.varieties[post.variety_id] %}
      {% if d and d.registration.status %}
        {% assign class_key = d.cultivar_class %}
        {% assign class_label = site.data.categories.cultivar_class[class_key] %}
        {% assign pattern_key = d.classification.pattern | first %}
        {% assign pattern_label = site.data.categories.pattern[pattern_key] %}
        <a class="kc-named-row" href="{{ post.url | relative_url }}">
          <span class="kc-named-index">{{ forloop.index | prepend: "00" | slice: -2, 2 }}</span>
          <span class="kc-named-main">
            <strong>{{ d.name }}</strong>
            {% if d.hanja %}<small>{{ d.hanja }}</small>{% endif %}
          </span>
          <span class="kc-named-meta">
            <em>{{ d.registration.status }}</em>
            {% if class_label %}<small>{{ class_label }}</small>{% endif %}
            {% if pattern_label %}<small>{{ pattern_label }}</small>{% endif %}
          </span>
          <span class="kc-named-arrow" aria-hidden="true">→</span>
        </a>
      {% endif %}
    {% endfor %}
  </div>
</section>

<section class="kc-leaf-section kc-named-note">
  <div>
    <p class="kc-section-kicker">CATALOG PRINCIPLE</p>
    <h2>이름과 형질은 분리해서 기록합니다</h2>
    <p>명명품 페이지는 이름과 등록 상태를 시작점으로 삼고, 실제 품종의 잎·무늬·꽃 형질은 개별 도감과 AI 데이터에서 독립적으로 연결합니다.</p>
  </div>
  <a class="kc-hero-button" href="{{ '/varieties/classification/' | relative_url }}">분류 체계 보기</a>
</section>
