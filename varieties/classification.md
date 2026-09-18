---
layout: default
title: "분류별 품종 찾기"
permalink: /varieties/classification/
---

<section class="kc-classification-hero">
  <div>
    <p class="kc-page-kicker">VARIETY CATALOG · CLASSIFICATION</p>
    <h1>분류별 품종 찾기</h1>
    <p class="kc-classification-lead">한국춘란의 대표 분류와 세부 형질을 나누어 살펴봅니다. 대표 분류와 잎의 형질은 서로 다른 탐색축으로 유지합니다.</p>
  </div>
  <div class="kc-classification-guide">
    <span>대표 분류</span><span>세부 형질</span><span>품종</span>
  </div>
</section>

<section class="kc-classification-section">
  <div class="kc-classification-heading">
    <div>
      <p class="kc-section-kicker">PRIMARY CLASSIFICATION</p>
      <h2>대표 분류</h2>
    </div>
    <p>도감에서 품종을 구분할 때 사용하는 대표 명칭입니다.</p>
  </div>

  <div class="kc-classification-grid">
    {% for item in site.data.categories.cultivar_class %}
      {% assign key = item[0] %}
      {% assign label = item[1] %}
      <div class="kc-classification-card is-featured">
        <strong>{{ label }}</strong>
        <code>{{ key }}</code>
      </div>
    {% endfor %}
  </div>
</section>

<section class="kc-classification-section">
  <div class="kc-classification-heading">
    <div>
      <p class="kc-section-kicker">LEAF TRAITS</p>
      <h2>잎의 세부 형질</h2>
    </div>
    <p>한 품종에 여러 형질이 연결될 수 있습니다.</p>
  </div>

  <div class="kc-classification-subgrid">
    <div class="kc-classification-subcard">
      <h3>잎의 형태</h3>
      <div class="kc-classification-items">
        {% for item in site.data.categories.leaf_form %}
          <span class="kc-classification-tag">{{ item[1] }}</span>
        {% endfor %}
      </div>
    </div>

    <div class="kc-classification-subcard">
      <h3>잎의 폭</h3>
      <div class="kc-classification-items">
        {% for item in site.data.categories.leaf_width %}
          <span class="kc-classification-tag">{{ item[1] }}</span>
        {% endfor %}
      </div>
    </div>

    <div class="kc-classification-subcard">
      <h3>잎의 자태</h3>
      <div class="kc-classification-items">
        {% for item in site.data.categories.leaf_attitude %}
          <span class="kc-classification-tag">{{ item[1] }}</span>
        {% endfor %}
      </div>
    </div>

    <div class="kc-classification-subcard">
      <h3>잎의 무늬</h3>
      <div class="kc-classification-items">
        {% for item in site.data.categories.pattern %}
          <span class="kc-classification-tag">{{ item[1] }}</span>
        {% endfor %}
      </div>
    </div>

    <div class="kc-classification-subcard">
      <h3>잎끝</h3>
      <div class="kc-classification-items">
        {% for item in site.data.categories.leaf_tip %}
          <span class="kc-classification-tag">{{ item[1] }}</span>
        {% endfor %}
      </div>
    </div>

    <div class="kc-classification-subcard">
      <h3>무늬 위치</h3>
      <div class="kc-classification-items">
        {% for item in site.data.categories.pattern_position %}
          <span class="kc-classification-tag">{{ item[1] }}</span>
        {% endfor %}
      </div>
    </div>
  </div>
</section>

<section class="kc-classification-section">
  <div class="kc-classification-heading">
    <div>
      <p class="kc-section-kicker">PATTERN BEHAVIOR</p>
      <h2>무늬의 발현</h2>
    </div>
    <p>AI 데이터셋에서 독립된 형질 축으로 보존합니다.</p>
  </div>

  <div class="kc-classification-grid">
    {% for item in site.data.categories.pattern_timing %}
      <div class="kc-classification-card">
        <strong>{{ item[1] }}</strong>
        <code>{{ item[0] }}</code>
      </div>
    {% endfor %}
  </div>
</section>

<div class="kc-classification-footer">
  <span class="kc-section-note">분류 체계는 실제 품종 데이터가 쌓이면서 계속 확장할 수 있습니다.</span>
  <a class="kc-text-link" href="{{ '/varieties/' | relative_url }}">전체 품종 보기 →</a>
</div>
