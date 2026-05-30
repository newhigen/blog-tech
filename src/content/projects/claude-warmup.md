---
title: Claude 워밍업
description: 출근 전 Claude quota 윈도우를 미리 깨워 하루 토큰을 고르게 분산.
tags: [Claude Code, CLI]
period: "2026.05"
category: Better Claude Code
icon: "☀"
github: https://github.com/newhigen/claude-warmup
image: "/projects/claude-warmup.png"
dashboard: "/dashboards/claude-warmup.html"
---

## 소개

출근 후 Claude를 처음 쓰면 quota 윈도우가 그 시각부터 시작된다. 그러면 9시간 근무에 윈도우가 두 개밖에 안 들어와 토큰이 한 시간대에 몰린다. 출근 전에 자동으로 미리 깨워두면 출근 직후·점심 사이·퇴근 전 세 번에 새 quota가 들어와 하루 동안 고르게 쓸 수 있다.

## 주요 기능

- **예약 워밍업** — 출근 전 자동으로 quota 윈도우 시작
- **윈도우 시각화** — 문제(몰림)와 해결(분산)을 한눈에

## 배경

quota는 "언제 처음 쓰느냐"가 하루 전체 가용량을 좌우한다. 시작점만 앞당겨도 근무 시간 토큰이 크게 늘어난다.
