# Project: 3-Agent Collaboration Lab (0513_class)

## Overview
- 목적: Antigravity, Claude Code, Codex 3개 에이전트의 협업 체계를 구축하고 최적화하는 실험실 프로젝트
- 기술스택: HTML / CSS (Vanilla) / JavaScript / Vite
- 패키지 매니저: npm

## Dev Commands
- 설치: `npm install`
- 실행: `npm run dev`
- 테스트: `npm test`
- 린트: `npm run lint`

## Code Rules
- **언어**: 모든 소통과 문서는 한국어 우선 (English only if necessary for code)
- **작업 계획**: 모든 코드 수정 전 `implementation_plan` 아티팩트를 통해 실행 계획 제시
- **안전**: 파일 삭제, 시스템 변경, 비용 발생 작업 전 반드시 사용자 승인 획득
- **보안**: API 키 및 보안 정보 하드코딩 절대 금지 (.env 사용)
- **커밋**: `type: description` 형식 준수 (feat, fix, refactor, docs, chore)

## 🤖 3-Agent Role Awareness
이 프로젝트는 아래 3개 에이전트가 각자의 강점을 발휘하여 협업합니다.

1. **Antigravity (Planning & Arch)**:
   - 역할: 전체 아키텍처 설계, 작업 분해(Decomposition), 브라우저 자동화 및 QA, UI/UX 디자인 가이드.
   - 특징: 'High-level' 시야를 유지하며 다른 에이전트에게 태스크를 할당하고 결과를 검증함.
2. **Claude Code (Logic & Refactor)**:
   - 역할: 복잡한 비즈니스 로직 구현, 대규모 리팩터링, 멀티 파일 수정, 테스트 코드 작성.
   - 특징: 'Precision'에 강점이 있으며, 복잡한 코드 베이스의 일관성을 유지함.
3. **Codex (Quick Proto & Module)**:
   - 역할: 단일 모듈 구현, 빠른 프로토타이핑, 스타일링(CSS) 작업, 단순 버그 수정.
   - 특징: 'Speed'와 'Single-focus' 작업에 최적화됨.

## Always Read
- `constitution.md`: 프로젝트의 헌법 (목표 및 불변 규칙)
- `progress.md`: 현재 진행 상황 및 태스크 보드

## Logging
- 작업 완료 시 반드시 로그 업데이트: `/Users/macbook15-platform/2026/L_2026_os/logs/`
- 파일명: `{YYYY-MM-DD}_{프로젝트명}_{작업요약}.md`
