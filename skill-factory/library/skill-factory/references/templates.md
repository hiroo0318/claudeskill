# templates.md
# 스킬 출력 템플릿 모음

CREATE 모드 Step 3에서 참조한다.
스킬 유형에 맞는 템플릿을 선택해 적용한다.

---

## §1. 기본 Claude Skill 템플릿

```md
---
name: skill-name
version: 1.0.0
description: Use when the user says "[트리거1]", "[트리거2]", "[한국어 트리거]", or asks to [specific task]. Also trigger when [추가 조건]. Always use this skill instead of [generic alternative]. Do not use for [제외1], [제외2], [제외3].
---

# [스킬 제목]

## 목적
[이 스킬이 하는 일 — 한 문장]

## 사용자 컨텍스트
- 직무: 20년차 모바일 서비스 기획자
- 환경: [업무 환경]

## 입력 방식
[어떤 형태의 입력을 받는지]

## 운영 모드 (해당 시)
| 모드 | 트리거 | 동작 |
|---|---|---|

## 출력 구조
[고정 출력 형식]

## 작성 규칙
- [해야 할 것]

## 금지 사항
- [하지 말아야 할 것]

## 단축 명령어 (해당 시)
| 명령어 | 동작 |
|---|---|

## 사용 예시
입력: [예시]
출력: [예시]
```

---

## §2. 프로젝트 지침 템플릿 (Lite)

Claude.ai 프로젝트 "지침" 탭에 바로 붙여넣는 압축형.
Full MD 대비 50% 이하 길이를 목표로 한다.

```md
# [프로젝트명] 운영 지침

## 역할
[한 줄 역할 정의]

## 기본 원칙
1. [핵심 원칙]
2. [핵심 원칙]

## 운영 모드
- [모드A]: [한 줄 설명]
- [모드B]: [한 줄 설명]

## 출력 형식
[대표 출력 구조]

## 금지
- [핵심 금지사항만]
```

---

## §3. 채팅 즉시 사용 템플릿

새 채팅방에서 첫 메시지로 붙여넣는 단일 블록.

```md
당신은 [역할]입니다.

[핵심 지시 2~4줄]

출력 형식:
- [형식]

하지 말아야 할 것:
- [금지사항]
```

---

## §4. Full MD 템플릿 (노션/파일 기준 원본)

상세 규칙과 예시를 모두 포함하는 완전한 문서.
프로젝트 지침이나 Claude Skill의 원본 기준 문서로 사용.

```md
# [스킬명] — Full 문서
버전: v[X.X.X] | 최종 수정: [날짜]

## 1. 목적
## 2. 역할
## 3. 사용자 컨텍스트
## 4. 입력 방식
## 5. 운영 모드 (상세)
## 6. 출력 구조 (상세)
## 7. 작성 규칙
## 8. 금지 사항
## 9. 단축 명령어
## 10. 사용 예시 (다수)
## 11. 버전 히스토리
```

---

## §5. Description 작성 패턴 (CSO)

### 좋은 예
```
Use when the user says "스킬 만들자", "프롬프트 만들어줘", "개선해줘", or asks to create, improve, merge, or convert Claude skills and prompts. Always use this skill instead of providing ad-hoc prompt drafts. Do not use for writing business documents, code, or emails.
```

### 나쁜 예 (워크플로우 요약 — 금지)
```
Use when creating skills. First ask about the purpose, then gather requirements, then design the structure, then output the result.
```
→ Claude가 description만 읽고 본문을 무시하게 됨.

### 나쁜 예 (약한 표현 — 금지)
```
This skill can help with prompt engineering tasks.
```
→ 발동률이 낮아짐.

---

## §6. 스킬 유형별 선택 가이드

| 목적 | 권장 형태 |
|---|---|
| 반복 업무 자동화 | Claude Skill (SKILL.md) |
| 장기 프로젝트 운영 | 프로젝트 지침 (Lite) |
| 기준 문서 보관 | Full MD |
| 새 채팅 즉시 실행 | 채팅 즉시 사용 버전 |
| 팀 공유 | Full MD + 프로젝트 지침 분리 |
