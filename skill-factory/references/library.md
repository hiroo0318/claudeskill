# 스킬 라이브러리 (Skill Library)

> 마지막 업데이트: 2026-04-19
> 총 스킬 수: 11개

---

## 📋 전체 목록

| # | 스킬명 | 한줄 설명 | 버전 | 카테고리 | 최종 수정 |
|---|--------|---------|------|---------|---------|
| 1 | meeting-writer | 회의 STT/메모 → 실무 회의록 + Planner Insight 자동 정리 | 2.2.0 | 문서 작성 | 2026-04-14 |
| 2 | email-writer | 메모/요점 → 발송 가능한 완성형 업무 이메일 변환 | 1.0.0 | 문서 작성 | - |
| 3 | service-planner | 아이디어/RFP → 서비스 전략·정책·IA·기능 정의 전 과정 | 1.0.0 | 서비스 기획 | - |
| 4 | qa-sheet-writer | 기획서/기능 목록 → 실무 QA 테스트 시트 자동 생성 | 1.0.0 | 개발 협업 | - |
| 5 | dev-architect | 기획 결과물 → 개발 설계·아키텍처·협업 문서 + 코딩 | **2.1** | 개발 협업 | **2026-04-19** |
| 6 | tech-reviewer | 기술 개념/설정 → 기획자 관점 실무 설명 및 검토 | 1.0.0 | 개발 협업 | - |
| 7 | ui-publisher | IA/기능 정의 → Front/Admin 화면 설계 및 퍼블리싱 | 1.1.0 | UI/UX | - |
| 8 | vibe-coding | 기획 의도 → 즉시 실행 가능한 코드 빠른 구현 | 1.0.0 | 개발 협업 | - |
| 9 | rfp-proposal | RFP 분석 → 배점 최대화 제안 전략·제안서 초안 | 1.0.0 | 제안/사업 | - |
| 10 | legal-contract-assistant | 계약서/동의서/서비스 법무 설계 한국 법률 기준 지원 | 3.0 | 법무 | - |
| 11 | skill-factory | 스킬/프롬프트 설계·생성·라이브러리 관리 시스템 | 1.0.0 | 시스템 | - |

---

## 🗂️ 카테고리별 목록

### 📝 문서 작성
| 스킬명 | 설명 | 주요 트리거 |
|--------|------|-----------|
| meeting-writer | 회의록 + Planner Insight 자동 정리 | 회의록 정리, 미팅 정리, STT 정리, 회의 요약 |
| email-writer | 업무 이메일 작성 (외부/내부) | 이메일 써줘, 메일 작성, 보고 메일, 협업 메일 |

### 🗺️ 서비스 기획
| 스킬명 | 설명 | 주요 트리거 |
|--------|------|-----------|
| service-planner | 서비스 전략→정책→구조→UI/UX→운영 전 과정 | 서비스 기획, 기획서 작성, 기능 정의, IA 설계 |

### ⚙️ 개발 협업
| 스킬명 | 설명 | 주요 트리거 |
|--------|------|-----------|
| dev-architect | 기획 결과물 → 개발 설계·협업 문서 + 코딩 (v2.1) | 개발 설계, API 설계, DB 설계, ERD, 시스템 아키텍처, 구현해줘 |
| qa-sheet-writer | QA 테스트 시트 자동 생성 | QA 시트, TC 만들어줘, 테스트 케이스, QA 설계 |
| tech-reviewer | 기술 개념 설명 및 검토 | 기술 검토, 개발 설명해줘, Spring Boot, Docker, CI/CD |
| vibe-coding | 빠른 프로토타입 코드 구현 | 바이브코딩, 코드 짜줘, 프로토타입 만들자, 구현해줘 |

### 🖥️ UI/UX
| 스킬명 | 설명 | 주요 트리거 |
|--------|------|-----------|
| ui-publisher | Front/Admin 화면 설계 및 퍼블리싱 | 화면 설계, 퍼블리싱, UI 만들어줘, 컴포넌트, Admin 화면 |

### 📑 제안/사업
| 스킬명 | 설명 | 주요 트리거 |
|--------|------|-----------|
| rfp-proposal | RFP 분석 + 배점 최대화 제안서 작성 | RFP 분석, 제안서 작성, 제안 전략, 입찰 준비 |

### ⚖️ 법무
| 스킬명 | 설명 | 주요 트리거 |
|--------|------|-----------|
| legal-contract-assistant | 계약서·동의서·법무 설계 (한국 법률 기준) | 계약서 작성, 개인정보 동의, NDA, SLA, 법무 검토 |

### 🛠️ 시스템
| 스킬명 | 설명 | 주요 트리거 |
|--------|------|-----------|
| skill-factory | 스킬/프롬프트 설계·생성·라이브러리 관리 | 스킬 만들자, 프롬프트 만들어줘, 라이브러리 관리 |

---

## 🔗 스킬 경계 및 관계

```
서비스 기획 흐름:
  service-planner → dev-architect → qa-sheet-writer
                 ↘ ui-publisher

빠른 구현 흐름:
  service-planner → vibe-coding (개인 프로젝트 즉시 구현)
  dev-architect   → vibe-coding (BUILD 모드 연계)

문서 작업:
  meeting-writer → email-writer (회의 결과 → 후속 메일)

사업 제안:
  rfp-proposal → service-planner (수주 후 기획 전환)
```

### 스킬 선택 가이드
| 상황 | 사용 스킬 |
|------|---------|
| 서비스 아이디어 → 기획서 | service-planner |
| 기획서 → 개발팀 설계 문서 | dev-architect (REVIEW FULL) |
| 특정 기능 → 개발팀 협의 | dev-architect (REVIEW FOCUS) |
| 개인 프로젝트 → 즉시 코딩 | dev-architect (BUILD) 또는 vibe-coding |
| 화면 설계 → 퍼블리싱 | ui-publisher |
| 기능 정의 → QA 시트 | qa-sheet-writer |
| 기술 용어/구조 이해 | tech-reviewer |
| RFP 입찰 → 제안서 | rfp-proposal |
| 계약·동의서 작성 | legal-contract-assistant |
| 회의 내용 → 회의록 | meeting-writer |
| 업무 이메일 작성 | email-writer |

---

## 📝 버전 히스토리 (주요 변경)

| 스킬명 | 버전 | 주요 변경 내용 |
|--------|------|-------------|
| dev-architect | **v2.1** | 입력 유형 자동 감지(TYPE-A/B/C), 프로젝트 유형 자동 판별, REVIEW FOCUS 운영/QA 섹션 추가, BUILD 모드 📐선택 이유 필수화, 톤 전환("참조용 초안" → "기획자 설계안 + 검토 요청") |
| dev-architect | v2.0 | REVIEW FULL/FOCUS 분리, 정책→개발 매핑 구조화, 화면 처리 흐름 통합 |
| dev-architect | v1.x | SHARE/CODE 2모드 운영 (구버전) |
| meeting-writer | v2.2.0 | Planner Insight 섹션, 3단계 결론 상태, 회의 유형별 처리 |
| legal-contract-assistant | v3.0 | B2B 계약 + B2C 동의서 통합, 서비스 법무 설계 추가 |
| ui-publisher | v1.1.0 | React/Vue/HTML 멀티 프레임워크 지원 |
