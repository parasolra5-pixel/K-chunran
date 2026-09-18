---
layout: default
title: "중투"
permalink: /varieties/leaf/jungtu/
---

<section class="kc-leaf-hero kc-jungtu-hero">
  <div>
    <p class="kc-page-kicker">VARIETY CATALOG · LEAF · JUNGTU</p>
    <h1>중투</h1>
    <p class="kc-page-lead">잎의 중앙을 중심으로 밝은 무늬가 나타나는 대표적인 한국춘란 엽예 형질입니다.</p>
    <p class="kc-page-copy">중투는 하나의 품종명이 아니라 여러 품종에서 관찰할 수 있는 형질입니다. K-Chunran에서는 대표 분류와 잎의 세부 형질을 분리해 기록합니다.</p>
  </div>
  <div class="kc-jungtu-guide">
    <span>무늬</span><i>→</i><span>형질</span><i>→</i><span>품종</span>
  </div>
</section>

<section class="kc-leaf-section">
  <div class="kc-section-heading">
    <div>
      <p class="kc-section-kicker">WHAT IS JUNGTU?</p>
      <h2>중투를 어떻게 볼 것인가</h2>
    </div>
    <p class="kc-section-note">무늬의 위치와 형태를 먼저 보고 품종으로 연결합니다.</p>
  </div>

  <div class="kc-jungtu-observe">
    <div>
      <strong>중앙 무늬</strong>
      <span>잎의 중앙을 따라 밝은 색의 무늬가 나타나는지 관찰합니다.</span>
    </div>
    <div>
      <strong>색 대비</strong>
      <span>녹색 바탕과 무늬의 색, 명도와 경계를 함께 기록합니다.</span>
    </div>
    <div>
      <strong>무늬의 폭과 경계</strong>
      <span>무늬가 잎의 어느 범위까지 이어지고 경계가 어떻게 형성되는지 살펴봅니다.</span>
    </div>
    <div>
      <strong>잎의 자태</strong>
      <span>입엽·수엽·광엽·세엽·단엽 등 잎 자체의 형질은 별도의 축으로 보존합니다.</span>
    </div>
  </div>
</section>

<section class="kc-leaf-section">
  <div class="kc-section-heading">
    <div>
      <p class="kc-section-kicker">RELATED CLASSIFICATIONS</p>
      <h2>중투와 연결되는 대표 분류</h2>
    </div>
    <p class="kc-section-note">대표 분류와 세부 형질을 섞지 않습니다.</p>
  </div>

  <div class="kc-jungtu-class-grid">
    {% assign jungtu_classes = "jungtuho|중투호,danyeopseong_jungtu|단엽성중투,danyeop_jungtu|단엽중투" | split: "," %}
    {% for item in jungtu_classes %}
      {% assign pair = item | split: "|" %}
      <div class="kc-jungtu-class">
        <strong>{{ pair[1] }}</strong>
        <code>{{ pair[0] }}</code>
      </div>
    {% endfor %}
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

  <div class="kc-jungtu-tags">
    <span>단엽</span>
    <span>환엽</span>
    <span>입엽</span>
    <span>수엽</span>
    <span>광엽</span>
    <span>세엽</span>
    <span>원두</span>
    <span>둔두</span>
    <span>예두</span>
  </div>
</section>

<section class="kc-leaf-section">
  <div class="kc-section-heading">
    <div>
      <p class="kc-section-kicker">JUNGTU VARIETIES</p>
      <h2>중투와 연결된 품종</h2>
    </div>
    <p class="kc-section-note">현재 K-Chunran 데이터에 연결된 품종입니다.</p>
  </div>

  <div class="kc-jungtu-variety-list">
    {% for post in site.posts %}
      {% assign d = site.data.varieties[post.variety_id] %}
      {% if d %}
        {% assign patterns = d.classification.pattern %}
        {% if patterns contains "jungtu" %}
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
    <h2>중투를 AI 데이터로 연결하기</h2>
    <p>실제 이미지가 확보되면 무늬 영역, 색, 경계, 잎 형태와 같은 관찰 형질을 이미지 데이터와 연결할 수 있습니다. 이 페이지는 그 데이터 구조의 출발점입니다.</p>
  </div>
  <a class="kc-hero-button" href="{{ '/ai/' | relative_url }}">AI 데이터 보기</a>
</section>
