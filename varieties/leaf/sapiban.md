---
layout: default
title: "사피반"
permalink: /varieties/leaf/sapiban/
---

<section class="kc-leaf-hero kc-jungtu-hero">
  <div>
    <p class="kc-page-kicker">VARIETY CATALOG · LEAF · SAPIBAN</p>
    <h1>사피반</h1>
    <p class="kc-page-lead">잎에 나타나는 사피 계열의 반점 무늬와 그 분포를 살펴봅니다.</p>
    <p class="kc-page-copy">사피반은 잎에 나타나는 무늬 형질의 하나입니다. K-Chunran에서는 사피반의 무늬 자체와 잎의 형태·자태, 품종의 대표 분류를 서로 구분해 기록합니다.</p>
  </div>
  <div class="kc-jungtu-guide">
    <span>무늬</span><i>→</i><span>형질</span><i>→</i><span>품종</span>
  </div>
</section>

<section class="kc-leaf-section">
  <div class="kc-section-heading">
    <div>
      <p class="kc-section-kicker">WHAT IS SAPIBAN?</p>
      <h2>사피반을 어떻게 볼 것인가</h2>
    </div>
    <p class="kc-section-note">관찰 가능한 형질을 기준으로 살펴봅니다.</p>
  </div>

  <div class="kc-jungtu-observe">
    <div>
      <strong>무늬의 형태</strong>
      <span>잎에 나타나는 사피 계열 반점의 모양과 이어지는 양상을 관찰합니다.</span>
    </div>
    <div>
      <strong>반점의 분포</strong>
      <span>반점이 잎의 어느 부분에 나타나고 어떻게 분포하는지 살펴봅니다.</span>
    </div>
    <div>
      <strong>색과 대비</strong>
      <span>무늬의 색과 녹색 바탕의 대비, 경계와 농담을 함께 기록합니다.</span>
    </div>
    <div>
      <strong>다른 잎 형질</strong>
      <span>잎의 형태·자태와 폭 등은 사피반과 별도의 형질 축으로 기록합니다.</span>
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
      <span>중투 · 복륜 · 산반 · 호 · 사피반 · 호피반 등</span>
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
      <p class="kc-section-kicker">SAPIBAN VARIETIES</p>
      <h2>사피반과 연결된 품종</h2>
    </div>
    <p class="kc-section-note">현재 K-Chunran 데이터에 연결된 품종입니다.</p>
  </div>

  <div class="kc-jungtu-variety-list">
    {% for post in site.posts %}
      {% assign d = site.data.varieties[post.variety_id] %}
      {% if d %}
        {% assign patterns = d.classification.pattern %}
        {% if patterns contains "sapiban" %}
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
    <h2>사피반을 AI 데이터로 연결하기</h2>
    <p>실제 이미지가 확보되면 무늬 영역, 분포, 색, 경계와 같은 관찰 형질을 이미지 데이터와 연결할 수 있습니다. 이 페이지는 그 데이터 구조의 출발점입니다.</p>
  </div>
  <a class="kc-hero-button" href="{{ '/ai/' | relative_url }}">AI 데이터 보기</a>
</section>
