---
title: 독서 성향 분석
description: 읽은 책 데이터로 독서 취향과 성향을 분석하는 리포트.
tags: [Data Analysis, Python]
period: "2026.05"
category: AI in Daily Life
icon: "❉"
image: "/projects/book-analysis.png"
dashboard: "/dashboards/book-analysis.html"
---

## 문제 — 독서 기록엔 내가 담긴다

읽은 책 목록은 그냥 기록이 아니다. 그 안엔 관심사와 생각의 궤적이 은근히 담긴다. 주로 어떤 분야를 읽는지, 해가 갈수록 관심이 어떻게 변했는지, 막연히 느끼던 취향이 실제로 어떤지 — 데이터로 비춰보고 싶었다.

## 관점 — 권수가 아니라 '궤적'으로

몇 권 읽었나보다 어떤 분야로 어떻게 옮겨갔나가 사람을 더 말한다고 봤다. 목록을 분포와 흐름으로 펼치면 취향의 궤적이 드러난다.

## 어떻게 — 책 데이터를 리포트로

책 데이터(제목·분야·연도)를 정리해 독서 리포트로 만든다.

<div class="dg"><div class="dg-node"><b>책 목록</b></div><div class="dg-arr">→</div><div class="dg-node"><b>분야·연도 정리</b></div><div class="dg-arr">→</div><div class="dg-node"><b>분포·흐름 계산</b></div><div class="dg-arr">→</div><div class="dg-node"><b>성향 분석</b></div><div class="dg-arr">→</div><div class="dg-node key"><b>리포트</b></div></div>

## 만들어온 과정

처음엔 토스 스타일이었다. 단일 액센트·여백 중심의 미학으로 다시 칠했다.

### 토스 스타일
![토스 스타일](/projects/book-before.png)

### 지금
![ai-pick 미학](/projects/book-after.png)

## 기능

### 데이터가 그리는 독서 자화상
- **분야 분포** — 어떤 주제를 주로 읽는지
- **시기별 흐름** — 연도별 독서량과 관심 변화
- **성향 요약** — 데이터에서 드러나는 취향. 다만 해석엔 주관이 섞이니 하나의 관점으로 본다

## 성과

- 막연하던 취향이 분야 분포·시기 흐름으로 드러난다
- 책 데이터만 있으면 리포트가 자동으로 갱신된다
- 다만 책 목록이 사람의 전부는 아니니, 가벼운 자화상으로 본다
