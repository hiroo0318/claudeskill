# Claude Skill Library

> 17년차 모바일 서비스 기획자를 위한 Claude 스킬 라이브러리
> 마지막 업데이트: 2026-03-29

---

## 스킬 목록

| No | 스킬명 | 버전 | 카테고리 | 설명 | 주요 트리거 |
|----|--------|------|---------|------|-----------|
| 01 | `skill-factory` | v1.0 | 시스템 | 스킬 제조 및 라이브러리 관리 마스터 스킬 | "스킬 만들자", "프롬프트 만들어줘", "라이브러리 보여줘" |
| 02 | `service-planner` | v1.1 | 기획 | 서비스 전략→정책→구조→UI/UX→운영 정책까지 10단계 기획 수행 | "서비스 기획", "기획 시작", "IA 설계", "/이관" |
| 03 | `rfp-proposal` | v1.2 | 제안 | RFP 분석→제안 전략→제안서 초안 생성. 4단계 출처 태깅 | "RFP 분석", "제안서 작성", "입찰 준비" |
| 04 | `dev-architect` | v1.3 | 개발설계 | 기획→개발 설계 연결. SHARE(팀 공유 문서) / CODE(직접 설계) | "개발 설계", "API 설계", "DB 설계", "ERD" |
| 05 | `vibe-coding` | v1.0 | 코딩 | 기획 의도를 실행 가능한 코드로 즉시 전환. React/Vue/HTML+Supabase | "바이브코딩", "코드 짜줘", "구현해줘" |
| 06 | `ui-publisher` | v1.0 | UI/퍼블 | 기획→화면설계→퍼블리싱 전 흐름. React/Vue/HTML 지원 | "화면 설계", "퍼블리싱", "UI 만들어줘", "/react", "/vue", "/html" |

---

## 스킬 관계도

```
서비스 기획 흐름:
service-planner → dev-architect → vibe-coding
     ↓                               ↓
  (기획서)                        (코드 구현)
     ↓
ui-publisher ← (화면 설계 · 퍼블리싱 특화)

제안 흐름:
rfp-proposal (독립 운영)

스킬 관리:
skill-factory (전체 관리)
```

---

## 스킬별 경계 정의

| 스킬 | 담당 영역 | 비담당 (다른 스킬로) |
|------|---------|------------------|
| `service-planner` | 서비스 전략, 정책, IA, 기능 정의 | DB 설계, API 설계, 코드 → `dev-architect` |
| `dev-architect` | API 설계, DB/ERD, 개발 Task, 시스템 아키텍처 | UI 코드 구현 → `vibe-coding` 또는 `ui-publisher` |
| `vibe-coding` | 빠른 프로토타이핑, Supabase 연동, 전체 앱 구현 | UI/UX 구조 설계 → `ui-publisher` |
| `ui-publisher` | 화면 설계, 컴포넌트 정의, 퍼블리싱 코드 | 백엔드 로직, DB 연동 → `dev-architect` / `vibe-coding` |
| `rfp-proposal` | RFP 분석, 제안서 작성 전 과정 | 실제 서비스 기획 → `service-planner` |

---

## 추가 예정 스킬 (백로그)

| 스킬명 | 용도 | 우선순위 |
|--------|------|---------|
| `data-analyst` | GA4 분석, SQL 쿼리, 운영 데이터 리포트 | 중 |
| `meeting-doc` | 회의록, 액션아이템, 보고서 자동화 | 중 |
| `api-spec-writer` | OpenAPI 스펙 문서화, API 명세서 작성 | 낮음 |
