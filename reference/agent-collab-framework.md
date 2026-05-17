# 3-Agent Collaboration Framework — 심화 가이드

## 🎯 핵심 철학

> **"에이전트는 사람의 손을 잠깐 빌려쓰는 도구다."**

- 모든 에이전트는 **progress.md 하나의 진실공급원**을 신뢰한다
- 컨텍스트 손실 = 시간 낭비 → 설계, 구현, 검증의 악순환
- 따라서 **상태 동기화가 곧 생산성**

---

## 📊 에이전트 역할 행렬

| 역할 | Antigravity | Claude Code | Codex |
|------|-------------|-------------|-------|
| **UI/UX** | ✅ (와이어프레임) | △ (반영) | △ (검증) |
| **구현** | △ (가이드) | ✅ (핵심) | △ (최적화) |
| **테스트** | △ (사용성) | ✅ (단위) | ✅ (통합) |
| **문서** | △ (설계도) | △ (인라인) | ✅ (정식) |
| **배포** | △ (설정) | ✅ (스크립트) | ✅ (검증) |

---

## 🔄 7단계 협업 사이클

### 1️⃣ **Kickoff** (Antigravity)
```
목표: 사용자 요구사항을 구조화된 설계로 변환

⏱  소요시간: 30~60분
📋 체크리스트:
  ☐ constitution.md 검토 (규칙 이해)
  ☐ progress.md 최신 상태 파악
  ☐ 사용자 요청 분석
  ☐ 컴포넌트 목록 정의
  ☐ 상호작용 플로우 다이어그램
  ☐ 기술 제약사항 명시

📤 Output: design.md (또는 .instructions/design-phase.md)
📝 Update progress.md:
   - 현재 상태: "Phase 1 - Kickoff 완료"
   - 다음 단계: "Claude Code로 구현 시작"
   - 완료 항목 체크
```

### 2️⃣ **Scaffold** (Claude Code)
```
목표: 프로젝트 폴더 구조 + 핵심 라이브러리 설정

⏱  소요시간: 15~30분
📋 체크리스트:
  ☐ progress.md에서 설계 확인
  ☐ package.json 의존성 추가
  ☐ src/ 폴더 구조 생성
  ☐ 라우팅 설정
  ☐ 기본 레이아웃 컴포넌트
  ☐ 에러 핸들링 기초

📤 Output: 동작하는 스켈레톤
📝 Update progress.md:
   - 의존성 버전 명시
   - 구조 다이어그램 추가
   - "다음: Codex로 검증"
```

### 3️⃣ **Verify** (Codex)
```
목표: 스켈레톤이 설계와 맞는지 확인

⏱  소요시간: 10~20분
📋 체크리스트:
  ☐ 코드 스타일 검사 (lint)
  ☐ 보안 점검 (dependencies 취약성)
  ☐ 성능 베이스라인 (번들 크기)
  ☐ 호환성 확인 (브라우저)

📤 Output: 검증 리포트
📝 Update progress.md:
   - 검증 항목 + 결과
   - 이슈 있으면 Claude Code로 회귀
```

### 4️⃣ **Build** (Claude Code)
```
목표: 각 컴포넌트 + 로직 구현

⏱  소요시간: 2~8시간 (프로젝트 규모에 따라)
📋 체크리스트 (컴포넌트별):
  ☐ 컴포넌트 파일 생성
  ☐ Props 인터페이스 정의
  ☐ 스타일 (CSS/Tailwind)
  ☐ 상태 관리 (useState/context)
  ☐ 단위 테스트
  ☐ 인라인 문서

📤 Output: 구현된 컴포넌트들
📝 Update progress.md (체크포인트마다):
   - 완료된 컴포넌트 목록
   - 테스트 커버리지 %
   - 알려진 이슈 (TODO)
```

### 5️⃣ **Test** (Codex)
```
목표: 통합 테스트 + 성능 검증

⏱  소요시간: 1~3시간
📋 체크리스트:
  ☐ 통합 테스트 실행 (모든 기능)
  ☐ 성능 프로파일링 (lighthouse)
  ☐ 접근성 검사 (a11y)
  ☐ 크로스 브라우저 테스트
  ☐ 부하 테스트 (필요시)

📤 Output: 테스트 리포트 + 최적화 권장사항
📝 Update progress.md:
   - 테스트 통과율
   - 성능 메트릭 (LCP, FID, CLS 등)
   - 실패 항목 → Claude Code로 피드백
```

### 6️⃣ **Refactor** (Claude Code)
```
목표: 테스트 피드백 반영 + 코드 정리

⏱  소요시간: 1~2시간
📋 체크리스트:
  ☐ 실패한 테스트 수정
  ☐ 성능 최적화 (필요항목)
  ☐ 코드 중복 제거
  ☐ 주석 정리 + 문서 업데이트
  ☐ 빌드 확인

📤 Output: 최적화된 코드
📝 Update progress.md:
   - 수정사항 요약
   - 성능 개선율 (before/after)
```

### 7️⃣ **Deploy** (모든 에이전트)
```
목표: 프로덕션 배포 + 최종 검증

⏱  소요시간: 15~45분
📋 체크리스트:
  ☐ .env 설정 (시크릿 관리)
  ☐ 빌드 명령 검증
  ☐ 배포 스크립트 실행
  ☐ 스모크 테스트 (배포된 버전)
  ☐ 모니터링 설정

📤 Output: 배포된 애플리케이션
📝 Update progress.md:
   - 배포 날짜 + URL
   - 배포 버전
   - 다음 마일스톤 계획
```

---

## 📋 progress.md 템플릿

```markdown
# Progress — [프로젝트명]

## 현재 상태
- **단계**: Phase 4 - Build (50% 완료)
- **마지막 작업자**: Claude Code (2026-05-17 14:30)
- **다음 단계**: Codex로 테스트 검증
- **리뷰 필요**: 없음

## 마일스톤 (체크리스트)
- [x] Phase 1 - Kickoff
- [x] Phase 2 - Scaffold
- [x] Phase 3 - Verify
- [ ] Phase 4 - Build (50%)
  - [x] Header 컴포넌트
  - [x] Navigation
  - [ ] Main Content Area (진행 중)
  - [ ] Sidebar
  - [ ] Footer
- [ ] Phase 5 - Test
- [ ] Phase 6 - Refactor
- [ ] Phase 7 - Deploy

## 작업 이력
| 날짜 | 에이전트 | 작업 | 상태 |
|------|---------|------|------|
| 2026-05-13 | Antigravity | 설계 + constitution.md | ✅ |
| 2026-05-14 | Claude Code | 스켈레톤 생성 | ✅ |
| 2026-05-15 | Codex | 검증 리포트 | ✅ |
| 2026-05-16 | Claude Code | Header/Nav 구현 | ✅ |
| 2026-05-17 | Claude Code | Main Content 구현 (진행) | 🟡 |

## 알려진 이슈 (TODO)
- [ ] 모바일 반응형 미적용 (TODO: Antigravity 디자인 재검토)
- [ ] TypeScript strict mode 활성화 필요
- [ ] 성능: 이미지 최적화 필요 (Codex 리뷰 대기)

## 주요 의사결정
1. **React 18 선택** (2026-05-13)
   - 사유: 동시성 기능 + 에이전트 상태 관리 용이
   - 결과: 긍정적 (번들 크기 최적)

2. **Tailwind CSS** (2026-05-13)
   - 사유: 빠른 프로토타이핑 + 일관된 디자인
   - 결과: 개발 속도 40% 증가

## 다음 작업자를 위한 메모
- 현재 Header 컴포넌트까지 완료
- Main Content 구현 중인데, API 연결 부분에서 에러 발생 예상 (progress.md의 "알려진 이슈" 참고)
- Codex 성능 검증 후 Refactor 단계로 이동 예정
```

---

## 🔐 Context Preservation Checklist

### 에이전트 전환할 때 (A → B)

**출발 에이전트 (A) 체크리스트:**
- [ ] progress.md 마지막 상태 업데이트
- [ ] 구현 중단점 명확히 (줄 번호, 이유)
- [ ] 다음 에이전트가 할 일 명시 ("다음 단계: ...")
- [ ] 블로킹 이슈 있으면 "알려진 이슈"에 추가
- [ ] 코드 커밋 (메시지에 progress phase 포함)
- [ ] 예상 소요시간 메모

**도착 에이전트 (B) 체크리스트:**
- [ ] progress.md 읽음
- [ ] constitution.md 읽음 (처음이면)
- [ ] "마지막 작업자" 메모 확인
- [ ] "다음 단계" 확인
- [ ] "알려진 이슈" 검토
- [ ] 최신 코드 커밋 확인 (`git log --oneline -5`)
- [ ] 개발 환경 재설정 (npm install 등)

---

## 🚨 에러 시나리오

### 시나리오 1: 컨텍스트 손실
```
증상: Claude Code가 Antigravity의 설계를 몰라서 다른 방향으로 구현
원인: progress.md 미업데이트 + constitution.md 미확인
해결: 
  1. progress.md에서 설계 단계 재확인
  2. Antigravity에게 "다시 설명해줄 수 있나요?" 요청
  3. .instructions/common.md에 체크포인트 추가
```

### 시나리오 2: 작업 중복
```
증상: Claude Code와 Codex가 같은 컴포넌트 수정
원인: progress.md 미동기 (둘 다 "Phase 4"만 봤음)
해결:
  1. 최신 progress.md 한 줄: "마지막 작업자: Claude Code (14:30)"
  2. 작업 전 progress.md 타임스탬프 확인
```

### 시나리오 3: 마감 임박 협업 가속화
```
상황: 48시간 내 배포 필요, 에이전트 순차는 비효율
전략:
  1. 병렬 작업: Antigravity가 advanced features 설계 중, Claude Code는 Phase 4 진행
  2. Sync Point: 매 2시간 progress.md 강제 동기화
  3. Codex: 테스트 병렬화 (Phase 4 완료 컴포넌트부터 검증)
```

---

## 📈 성공 메트릭

각 Phase마다 KPI 측정:

| Phase | KPI | 목표 |
|-------|-----|------|
| Kickoff | 설계 완성도 (체크리스트 %) | 100% |
| Scaffold | 빌드 성공률 | 100% |
| Verify | 보안/성능 이슈 | 0개 Critical |
| Build | 테스트 커버리지 | >80% |
| Test | 테스트 통과율 | 100% |
| Refactor | 성능 개선율 | >10% |
| Deploy | Uptime | 99.9% |

---

## 🎓 학습 자료

- [Multi-Agent Collaboration Patterns](https://example.com/patterns)
- [Context Management in AI](https://example.com/context)
- [State Machines for Workflow](https://example.com/state-machines)
- [Prompt Engineering for Teams](https://example.com/prompting)

