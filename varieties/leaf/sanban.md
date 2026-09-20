---
layout: default
title: "산반"
permalink: /varieties/leaf/sanban/
---

<section class="kc-leaf-hero kc-jungtu-hero">
  <div>
    <p class="kc-page-kicker">VARIETY CATALOG · LEAF · SANBAN</p>
    <h1>산반</h1>
    <p class="kc-page-lead">잎에 흩어져 나타나는 무늬의 분포와 밀도를 살펴봅니다.</p>
    <p class="kc-page-copy">산반은 잎에 나타나는 무늬 형질의 하나입니다. K-Chunran에서는 무늬의 분포를 관찰하고 잎의 형태와 다른 형질을 별도의 축으로 기록합니다.</p>
  </div>
  <div class="kc-jungtu-guide">
    <span>무늬</span><i>→</i><span>형질</span><i>→</i><span>품종</span>
  </div>
</section>

<section class="kc-leaf-section">
  <div class="kc-section-heading">
    <div>
      <p class="kc-section-kicker">WHAT IS SANBAN?</p>
      <h2>산반을 어떻게 볼 것인가</h2>
    </div>
    <p class="kc-section-note">관찰 가능한 형질을 기준으로 살펴봅니다.</p>
  </div>

  <div class="kc-jungtu-observe">
    <div>
      <strong>무늬의 분포</strong>
      <span>잎 전체에서 무늬가 어느 부분에 나타나는지 살펴봅니다.</span>
    </div>
    <div>
      <strong>무늬의 밀도</strong>
      <span>무늬가 모여 있는 정도와 분포의 변화를 관찰합니다.</span>
    </div>
    <div>
      <strong>색과 대비</strong>
      <span>무늬와 녹색 바탕의 색 차이와 경계를 함께 기록합니다.</span>
    </div>
    <div>
      <strong>다른 잎 형질</strong>
      <span>잎의 폭·형태·자태 등은 별도의 형질 축으로 기록합니다.</span>
    </div>
  </div>
</section>

<section class="kc-leaf-section">
  <div class="kc-section-heading">
    <div>
      <p class="kc-section-kicker">LEAF TRAITS</p>
      <h2>함께 기록하는 잎의 형질</h2>
    </div>
    <a class="kc-text-link" href="{{ '/varieties/classification/' | relative_url }}">전체 분류 보기 →</a>
  </div>

  <div class="kc-jungtu-trait-grid">
    <a class="kc-jungtu-trait-card" href="{{ '/knowledge/leaf/form/' | relative_url }}">
      <strong>잎의 형태·자태</strong>
      <span>단엽 · 환엽 · 입엽 · 수엽 등</span>
      <i>지식 사전 →</i>
    </a>
    <a class="kc-jungtu-trait-card" href="{{ '/knowledge/leaf/width/' | relative_url }}">
      <strong>잎의 폭</strong>
      <span>광엽 · 세엽</span>
      <i>지식 사전 →</i>
    </a>
    <a class="kc-jungtu-trait-card" href="{{ '/varieties/leaf/' | relative_url }}">
      <strong>잎의 무늬</strong>
      <span>중투 · 복륜 · 산반 · 호 · 서반 등</span>
      <i>도감 보기 →</i>
    </a>
    <a class="kc-jungtu-trait-card" href="{{ '/knowledge/leaf/form/' | relative_url }}">
      <strong>잎끝</strong>
      <span>원두 · 둔두 · 예두</span>
      <i>지식 사전 →</i>
    </a>
  </div>
</section>

<section class="kc-leaf-section">
  <div class="kc-section-heading">
    <div>
      <p class="kc-section-kicker">SANBAN VARIETIES</p>
      <h2>산반과 연결된 품종</h2>
    </div>
    <p class="kc-section-note">현재 K-Chunran 데이터에 연결된 품종입니다.</p>
  </div>

  <div class="kc-jungtu-variety-list">
    {% for post in site.posts %}
      {% assign d = site.data.varieties[post.variety_id] %}
      {% if d %}
        {% assign patterns = d.classification.pattern %}
        {% if patterns contains "sanban" %}
          {% assign class_label = site.data.categories.cultivar_class[d.cultivar_class] %}
          <a class="kc-jungtu-variety" href="{{ post.url | relative_url }}">
            <strong>{{ d.name }}</strong>
            {% if d.hanja %}<span>{{ d.hanja }}</span>{% endif %}
            {% if class_label %}<em>{{ class_label }}</em>{% endif %}
            {% if d.traits.leaf.form %}<small>{{ d.traits.leaf.form }}</small>{% endif %}
            <i>→</i>
          </a>
        {% endif %}
      {% endif %}
    {% endfor %}
  </div>
</section>

<section class="kc-leaf-section kc-jungtu-data">
  <div>
    <p class="kc-section-kicker">AI DATA CONNECTION</p>
    <h2>산반을 AI 데이터로 연결하기</h2>
    <p>실제 이미지가 확보되면 무늬 또는 잎 형태의 위치, 범위, 색, 경계와 같은 관찰 형질을 이미지 데이터와 연결할 수 있습니다. 이 페이지는 그 데이터 구조의 출발점입니다.</p>
  </div>
  <a class="kc-hero-button" href="{{ '/ai/' | relative_url }}">AI 데이터 보기</a>
</section>
