# Claude Skills Library

17년차 모바일 서비스 기획자를 위한 Claude 스킬 라이브러리입니다.

## 구조

```
01 claudeskill/
├── README.md
└── skill-factory/                      ← 스킬 제조소 (마스터 스킬)
    ├── references/
    │   └── library.md                  ← 스킬 라이브러리 목록
    └── library/                        ← 생성된 스킬들
        ├── Meeting Writer/             ← 회의록 작성 (v2.2.1)
        ├── QA Sheet Writer/            ← QA 테스트 시트 생성 (v1.0.0)
        ├── email-writer/               ← 업무 이메일 작성 (v1.0.0)
        ├── legal-contract-assistant/   ← 계약서·동의서 법무 설계 (v3.0.0)
        ├── dev-architect/              ← 개발 설계·아키텍처 (v1.0.0)
        ├── rfp-proposal/               ← RFP 분석·제안서 작성 (v1.0.0)
        ├── service-planner/            ← 서비스 기획 전 과정 (v1.0.0)
        ├── skill-factory/              ← 스킬 설계·생성 시스템 (v1.0.0)
        ├── tech-reviewer/              ← 기술 검토·설명 (v1.0.0)
        ├── ui-publisher/               ← UI/UX 화면 설계·퍼블리싱 (v1.1.0)
        └── vibe-coding/                ← 빠른 코드 구현 (v1.0.0)
```

---

## 스킬 목록

| # | 스킬명 | 설명 | 버전 | 카테고리 | 수정일 |
|---|--------|------|------|---------|--------|
| 1 | Meeting Writer | 회의 STT/메모 → 실무 회의록 + Planner Insight | 2.2.1 | 문서 작성 | 2026-04-15 |
| 2 | email-writer | 메모/요점 → 발송 가능한 완성형 업무 이메일 | 1.0.0 | 문서 작성 | 2026-04-13 |
| 3 | service-planner | 아이디어/RFP → 서비스 전략·정책·IA·기능 정의 | 1.0.0 | 서비스 기획 | 2026-04-03 |
| 4 | QA Sheet Writer | 기획서/기능 목록 → 실무 QA 테스트 시트 | 1.0.0 | 개발 협업 | 2026-04-13 |
| 5 | dev-architect | 기획 결과물 → 개발 설계·아키텍처·코딩 연결 | 1.0.0 | 개발 협업 | 2026-04-03 |
| 6 | tech-reviewer | 기술 개념/설정 → 기획자 관점 실무 설명 및 검토 | 1.0.0 | 개발 협업 | 2026-04-08 |
| 7 | ui-publisher | IA/기능 정의 → Front/Admin 화면 설계·퍼블리싱 | 1.1.0 | UI/UX | 2026-04-03 |
| 8 | vibe-coding | 기획 의도 → 즉시 실행 가능한 코드 빠른 구현 | 1.0.0 | 개발 협업 | 2026-04-03 |
| 9 | rfp-proposal | RFP 분석 → 배점 최대화 제안 전략·제안서 초안 | 1.0.0 | 제안/사업 | 2026-04-03 |
| 10 | legal-contract-assistant | 계약서·동의서·서비스 법무 설계 한국 법률 기준 | 3.0.0 | 법무 | 2026-04-09 |
| 11 | skill-factory | 스킬/프롬프트 설계·생성·라이브러리 관리 시스템 | 1.0.0 | 시스템 | 2026-04-15 |

---

## 사용 방법

### Claude.ai 프로젝트
각 스킬 폴더의 `SKILL.md` 내용을 프로젝트 지침(Instructions)에 붙여넣기

### Claude Code
```bash
git clone https://github.com/hiroo0318/claude.git
```
각 스킬 폴더를 Claude Code 스킬 경로에 설치

### 새 스킬 추가
이 프로젝트 채팅방에서 `"스킬 만들자"` 입력
→ 자동 설계 → `skill-factory/library/` 폴더에 저장 → `library.md` 업데이트 → GitHub push

---

## 업데이트 히스토리

| 날짜 | 내용 |
|------|------|
| 2026-04-15 | Meeting Writer v2.2.1 — 회의명 자동 생성 규칙 추가 |
| 2026-04-15 | Meeting Writer v2.2.0 — 회의 유형별 처리, 의사결정 근거, 일정 영향, Action 상태 코드 추가 |
| 2026-04-15 | library.md 전체 스킬 정보 업데이트 |
| 2026-04-14 | Meeting Writer v2.1.0 — 절대규칙 + 신규 섹션 통합 |
| 2026-04-14 | Meeting Writer v1.1.0 — 추론 금지 규칙 강화 |
| 2026-04-14 | Meeting Writer v1.0.0 — 최초 생성 |
| 2026-04-13 | email-writer, QA Sheet Writer 추가 |
| 2026-04-09 | legal-contract-assistant v3.0.0 업데이트 |
| 2026-04-08 | tech-reviewer 추가 |
| 2026-04-03 | dev-architect, service-planner, ui-publisher, vibe-coding, rfp-proposal 추가 |
| 2026-03-26 | skill-factory 최초 생성 |