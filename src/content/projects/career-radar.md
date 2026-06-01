---
title: 커리어 레이더
description: 한국 IT 채용 공고(JD)를 직군별 회사×스택 매트릭스 + 통합 직무기술서 + 학습 로드맵으로 정리하는 도구. 회사명은 익명화한 예시.
tags: [Data Analysis, Career]
period: "2026.05"
category: AI in Daily Life
icon: "📡"
image: "/projects/career-radar.png"
dashboard: "/dashboards/career-radar.html"
intro:
  summary: "한국 IT 채용 공고를 모아 직군별 회사×스택 매트릭스 + 통합 직무기술서 + 학습 로드맵으로 정리하는 Claude Code 도구. 공개용이라 회사명은 익명화했다."
  use:
    - "관심 직군의 채용 공고를 수집·구조화한다"
    - "회사×스택 매트릭스로 공통·차별 기술을 본다"
    - "통합 직무기술서와 학습 로드맵을 받는다"
---

## 문제 — 채용 JD는 흩어져 있고, '뭘 준비할지'가 안 보인다

직군 하나를 준비하려 해도 회사마다 요구가 제각각이다. 공고는 채용 사이트마다 흩어져 있고, 공통으로 요구하는 게 뭔지·이 회사만의 차별점이 뭔지는 결국 손으로 비교한다. 그러다 우선순위가 흐려진다.

## 관점 — 공고를 '데이터'로, 추정 없이

공고를 인상이 아니라 데이터로 봤다. 빈칸을 추정으로 채우지 않고, 공고 원문에 실제로 등장한 기술만 표시한다. 빈 칸은 "그 회사 JD에 명시되지 않았다"는 뜻이지 "없다"는 뜻이 아니다.

## 어떻게 — 수집 → 구조화 → 집계 → 통합

<div class="dg"><div class="dg-node"><b>채용 공고</b></div><div class="dg-arr">→</div><div class="dg-node"><b>본문 추출</b><span>Haiku</span></div><div class="dg-arr">→</div><div class="dg-node"><b>구조화</b><span>Sonnet/Opus</span></div><div class="dg-arr">→</div><div class="dg-node"><b>집계</b><span>deterministic</span></div><div class="dg-arr">→</div><div class="dg-node key"><b>매트릭스·JD·로드맵</b></div></div>

수집은 가벼운 모델로, 구조화는 큰 모델로, 집계는 결정적 스크립트로 나눠 비용과 신뢰도를 맞췄다.

## 기능

- **회사 × 스택 매트릭스** — 공고에 직접 등장한 기술만, 빈칸은 '미명시'로 구분
- **공통 스택** — 수집된 회사 절반 이상이 요구하는 기술 (우선 학습 후보)
- **회사별 차별점** — 그 회사 JD에만 등장한 기술
- **통합 직무기술서 · 로드맵** — 직군별로 묶은 JD와 학습 경로

## 성과

- 흩어진 채용 공고를 직군별 매트릭스 한 장으로
- 공통·차별 기술이 드러나 준비 우선순위가 잡힌다
- 추정 없이 공고 원문 기반 — 다만 수집 시점·범위에 따라 달라지고, 공개용이라 회사명은 익명화했다
