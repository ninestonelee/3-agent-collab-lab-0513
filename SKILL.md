---
name: 3-agent-collab-lab
description: >-
  Antigravity, Claude Code, Codex 3개 에이전트의 협업 패턴을 구현하는 실험실.
  에이전트 간 컨텍스트 유지, 작업 인수인계, 상태 동기화를 자동화하는 프레임워크.
author:
  name: ninestonelee
  url: https://github.com/ninestonelee
license: MIT
version: "1.0.0"
tags:
  - agent-collaboration
  - multi-agent
  - workflow-automation
  - antigravity
  - claude-code
  - codex
---

# 3-Agent Collaboration Lab — Claude Code Skill

> **Antigravity × Claude Code × Codex** — 세 에이전트가 하나의 프로젝트를 함께 만드는 협업 프레임워크

## 🎯 스킬 목적

다중 에이전트 환경에서:
- **컨텍스트 손실 방지**: `progress.md` 중심으로 모든 에이전트가 동일한 상태 공유
- **작업 인수인계 자동화**: 에이전트 간 전환 시 체크리스트 기반 핸드오프
- **협업 패턴 정형화**: 반복 가능한 워크플로우 스크립트화

## 📦 설치

### 방법 1: Claude Code 스킬로 직접 사용

```bash
git clone https://github.com/ninestonelee/3-agent-collab-lab-0513.git \
  ~/.claude/skills/3-agent-collab-lab
```

### 방법 2: 프로젝트 템플릿으로 포크

```bash
gh repo clone ninestonelee/3-agent-collab-lab-0513 my-agent-project
cd my-agent-project
npm install
npm run dev
```

## 🚀 빠른 시작

### 1️⃣ 프로젝트 초기화
```bash
cd your-project
cat constitution.md      # 프로젝트 불변 규칙 읽기
cat progress.md          # 현재 상태 파악
```

### 2️⃣ 에이전트 역할 분담
```
🤖 Antigravity  → UI/기획 설계 + 에이전트 명령어 작성
🧠 Claude Code  → 구현 + 테스트 + 리팩토링
🔍 Codex        → 검증 + 최적화 + 문서화
```

### 3️⃣ 작업 진행
```bash
# 자신이 작업할 때
1. progress.md를 먼저 읽기
2. 작업 수행
3. progress.md 업데이트 (다음 에이전트를 위해)

# 다른 에이전트로 전환
1. progress.md 최신 상태 파악
2. 명시된 "다음 할 일" 확인
3. 작업 시작
```

## 📋 필수 파일 구조

```
3-agent-collab-lab/
├── constitution.md          ← 🔴 불변 규칙 (에이전트들의 계약)
├── progress.md              ← 🟡 현재 상태 + 작업 이력
├── .instructions/
│   └── common.md            ← 모든 에이전트가 따를 지침
├── SKILL.md                 ← 이 파일 (스킬 정의)
├── plugin.json              ← 메타데이터
├── src/                     ← 소스 코드
├── public/                  ← 정적 자산
└── reference/
    └── agent-collab-framework.md  ← 협업 프레임워크 상세
```

## 🔄 협업 프로토콜

### Phase 1: Antigravity (UI 설계)
```
INPUT:  사용자 요청 / constitution.md 읽음
OUTPUT: 와이어프레임 + 상호작용 정의 + 컴포넌트 목록
UPDATE: progress.md → "Claude Code로 구현 준비 완료"
```

### Phase 2: Claude Code (구현)
```
INPUT:  progress.md 최신 상태 + Antigravity의 설계
OUTPUT: 동작하는 컴포넌트 + 테스트 + 커밋
UPDATE: progress.md → "Codex로 검증 준비 완료"
```

### Phase 3: Codex (검증)
```
INPUT:  Claude Code의 구현 + 테스트 결과
OUTPUT: 성능 리포트 + 최적화 제안 + 문서
UPDATE: progress.md → 완성 상태 기록
```

## 🛠 사용 사례

### ✅ 추천
- 복수 에이전트가 참여해야 하는 중규모 프로젝트
- 웹 애플리케이션 (React + Node.js)
- API 서버 + 프론트엔드 분리 작업
- 정규적인 협업 핸드오프 필요

### ❌ 부적합
- 단일 에이전트 작업
- 1인 스크립트 / 유틸리티
- 즉흥적 프로토타입

## 📚 심화 학습

더 자세한 협업 프레임워크는 `reference/agent-collab-framework.md` 참고.

주요 주제:
- Prompt Engineering for Multi-Agent Systems
- State Management Patterns (`progress.md` 버전 관리)
- Context Preservation Checklist
- Agent Role Specialization Matrix

## 🙏 Credits

- **Original Architecture**: 3-Agent Collab Lab (2026-05-13)
- **Antigravity Integration**: Antigravity IDE MCP 연동
- **Claude Code Adaptation**: ninestonelee (2026-05-17)

## 📜 License

MIT License — 자유롭게 포크·수정·배포 가능. 원본 저작권 표시 필수.

---

## 🔗 관련 리소스

- [Antigravity GitHub MCP 가이드](https://github.com/ninestonelee/3-agent-collab-lab-0513/tree/main/.instructions)
- [constitution.md](./constitution.md) — 프로젝트 불변 규칙
- [progress.md](./progress.md) — 현재 작업 상태
- [공식 레포](https://github.com/ninestonelee/3-agent-collab-lab-0513)

