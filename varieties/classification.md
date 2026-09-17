---
layout: default
title: "분류별 품종 찾기"
permalink: /varieties/classification/
---

# 분류별 품종 찾기

현재 데이터에 저장된 대표 분류와 세부 형질을 기준으로 품종을 찾아볼 수 있는 공간입니다.

<h2>대표 분류</h2>
<ul>
{% for item in site.data.categories.cultivar_class %}
  {% assign key = item[0] %}
  {% assign label = item[1] %}
  <li><strong>{{ label }}</strong> <code>{{ key }}</code></li>
{% endfor %}
</ul>

<h2>세부 형질</h2>
<p>세부 형질은 품종 하나에 여러 값이 연결될 수 있으므로 대표 분류와 별도의 탐색축으로 유지합니다.</p>

<h3>잎의 형태·자세</h3>
<ul>
{% for item in site.data.categories.leaf_form %}
  <li>{{ item[1] }} <code>{{ item[0] }}</code></li>
{% endfor %}
</ul>

<h3>잎의 무늬</h3>
<ul>
{% for item in site.data.categories.pattern %}
  <li>{{ item[1] }} <code>{{ item[0] }}</code></li>
{% endfor %}
</ul>

<h3>잎끝</h3>
<ul>
{% for item in site.data.categories.leaf_tip %}
  <li>{{ item[1] }} <code>{{ item[0] }}</code></li>
{% endfor %}
</ul>

<p><a class="kc-text-link" href="{{ '/varieties/' | relative_url }}">전체 품종 보기 →</a></p>
