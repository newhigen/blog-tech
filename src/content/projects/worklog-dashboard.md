---
title: 근태 기록 분석
description: 근태 데이터로 야근 시기와 출퇴근 리듬을 시각화.
tags: [Dashboard, Data Visualization]
period: "2026.05.24"
category: AI in Daily Life
icon: "⌚"
image: "/projects/worklog-dashboard.png"
imageLight: "/projects/worklog-dashboard-light.png"
dashboard: "/dashboards/worklog.html#sec-heatmap"
---

## 문제 — 근태 엑셀은 그냥 묵힌다

회사에서 받은 근태 데이터는 대개 엑셀로 묵힌다. 숫자 나열만으론 안 보이는 게 많다. 언제 야근이 몰렸는지, 휴가 뒤 출근 리듬이 어떻게 바뀌는지, 지난달보다 빨라졌는지 — 표로는 잘 안 잡힌다.

## 관점 — 출근 시각이 아니라 '리듬'으로

근태를 '몇 시에 왔다'는 점이 아니라, 시기마다 달라지는 리듬으로 봤다. 야근이 몰리는 때, 휴가 뒤 회복, 계절별 변동 — 흩어진 점을 선으로 이으면 그제야 패턴이 보인다.

## 어떻게 — 근태를 지도로 그린다

복잡한 데이터를 정리해 근태 지도로 만든다.

<div class="dg"><div class="dg-node"><b>근태 엑셀</b></div><div class="dg-arr">→</div><div class="dg-node"><b>정리</b></div><div class="dg-arr">→</div><div class="dg-node"><b>통계 계산</b></div><div class="dg-arr">→</div><div class="dg-node"><b>차트</b></div><div class="dg-arr">→</div><div class="dg-node key"><b>대시보드</b></div></div>

800일 넘는 기록에서 13개 차트와 주요 지표를 자동으로 뽑는다.

## 만들어온 과정

다크 테마로 시작해 라이트로 바꾸고, 연간 히트맵을 더하고, 야근에 색 규칙을 입히며 지금 모습이 됐다. (실데이터라 화면은 흐리게 처리 — 디자인 변화만 본다)

### 다크로 시작
![다크 초기](/projects/worklog-v1.png)

### 히트맵 추가
![히트맵 추가](/projects/worklog-v2.png)

### 색 규칙 · 완성
![완성](/projects/worklog-v3.png)

## 기능

### 분석 지표
출근 시간만 보지 않는다.
- **진짜 일한 시간** — 점심·저녁을 빼고 실제 업무 시간만 계산
- **야근 등급** — 근무 강도에 따라 유연·일반·장야근으로 구분
- **출근 변곡점** — 한 달 전 대비 리듬이 크게 바뀐 시점을 자동 탐지

### 디자인
- 중요한 지표는 상단 카드에 모아 한눈에
- 자주 나타나는 패턴은 부드러운 색, 야근은 선명한 색
- 15분 단위 분포와 연간 히트맵

## 성과

- 800일 넘는 기록을 수작업 없이 자동 집계 — 전엔 엑셀로 묵혀뒀다
- 출근 변곡점·야근 등급을 자동 탐지해, 직접 세지 않아도 된다
- 숫자로는 안 느껴지던 근무 패턴이 한 화면 13개 차트로 드러난다
- 다만 내 데이터 한정의 이야기다
