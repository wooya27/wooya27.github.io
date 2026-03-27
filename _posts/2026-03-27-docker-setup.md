---
title: "[DevOps] 윈도우 환경에서 Docker와 Python 분석 환경 구축하기"
excerpt: "Docker 실행 중 발생한 경로 에러와 가상환경 설정 트러블슈팅 기록"
categories:
  - DevOps
tags:
  - Docker
  - Python
  - Troubleshooting
---

## 1. 개요
토스(Toss) AI 엔지니어 로드맵의 첫걸음으로, 로컬 환경을 오염시키지 않는 Docker 기반 분석 환경을 구축했습니다.

## 2. 직면한 문제 (Troubleshooting)
- **에러 내용**: PowerShell에서 `%cd%` 인식 불가 및 가상환경 경로 꼬임.
- **원인 분석**: 쉘 환경에 따른 변수 차이 및 venv의 물리적 경로 의존성.
- **해결 방법**: `${PWD}` 사용 및 인터프리터 재지정을 통해 해결.

## 3. 결과
성공적으로 `psycopg2-binary`를 설치하고 도커 DB 연동을 확인했습니다.