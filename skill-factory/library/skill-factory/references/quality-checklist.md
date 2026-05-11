# quality-checklist.md
# 스킬 품질 검증 기준

REVIEW 모드 및 CREATE 모드 Step 4 (Description)에서 참조한다.

---

## §1. CSO 5대 원칙 (Description 작성)

Description은 Claude가 스킬을 언제 사용할지 판단하는 기준이다.
잘못 쓰면 스킬이 발동되지 않거나, 잘못 발동된다.

### 원칙 1. "Use when..."으로 시작한다
```
좋음: "Use when the user says '스킬 만들자', or asks to create a skill..."
나쁨: "This skill helps with skill creation..."
```

### 원칙 2. 3인칭으로 작성한다
```
좋음: "Use when the user asks to..."
나쁨: "I help you create..."
나쁨: "You can use this to..."
```

### 원칙 3. 워크플로우를 요약하지 않는다 ⚠️ 가장 중요
Description에 "먼저 X하고, 그다음 Y한다" 같은 절차를 쓰면
Claude가 본문(SKILL.md)을 읽지 않고 description만으로 실행한다.
→ Description은 "언제 쓰는지"만. "어떻게 하는지"는 본문에.

```
나쁨: "Use when creating skills. First ask about purpose, then gather requirements."
좋음: "Use when the user says '스킬 만들자' or asks to design a new skill."
```

### 원칙 4. Pushy하게 쓴다
Claude는 스킬을 undertrigger하는 경향이 있다. 명시적으로 강조한다.
```
약함: "This skill can help with code reviews."
좋음: "Always use this skill instead of providing ad-hoc review comments."
```

### 원칙 5. 실제 사용자 표현을 포함한다
전문 용어보다 자연스러운 표현. 한국어·영어 혼합.
```
좋음: "스킬 만들자", "프롬프트 만들어줘", "개선해줘", "create a skill", "make a prompt"
나쁨: "prompt engineering", "skill design request"
```

---

## §2. 전체 품질 점검 기준 (REVIEW 모드)

### 구조 점검

| 항목 | 확인 내용 | 판정 |
|---|---|---|
| 목적 명확성 | 무엇을 하는 스킬인지 한 문장으로 설명 가능한가 | ✅/❌ |
| Description | CSO 5대 원칙 모두 충족하는가 | ✅/❌ |
| 역할 적합성 | 전문가 역할이 업무 목적과 일치하는가 | ✅/❌ |
| 입력 처리 | 다양한 입력 형태를 구분하는가 | ✅/❌ |
| 출력 구조 | 실제 업무 산출물로 바로 쓸 수 있는가 | ✅/❌ |
| 금지 사항 | 임의 확정·추론·과장 방지 규칙이 있는가 | ✅/❌ |
| 운영 모드 | 반복 사용에 적합한 모드 체계가 있는가 | ✅/❌ |

### 실용성 점검

| 항목 | 확인 내용 | 판정 |
|---|---|---|
| 길이 | 프로젝트 지침으로 사용 가능한 길이인가 | ✅/❌ |
| 실행 가능성 | 환경에서 실제로 실행 불가능한 기능이 포함되어 있지 않은가 | ✅/❌ |
| 중복 여부 | 기존 라이브러리 스킬과 역할이 중복되지 않는가 | ✅/❌ |
| 최신성 | 현재 업무 방식 및 Claude 동작 방식에 맞는가 | ✅/❌ |
| 소스 무결성 | 문서 기반/협의 기반/추론을 구분하는가 (필요 시) | ✅/❌ |

### 판정 기준
- **10개 중 9개 이상 ✅**: 바로 사용 가능
- **7~8개 ✅**: 경미한 개선 후 사용
- **6개 이하 ✅**: IMPROVE 모드로 전면 개선 필요

---

## §3. 스킬 길이 가이드

| 형태 | 적정 길이 | 초과 시 처리 |
|---|---|---|
| Claude Skill SKILL.md | 200~500줄 | references로 분리 |
| 프로젝트 지침 (Lite) | 50~150줄 | Full MD로 분리 |
| Full MD | 제한 없음 | 챕터 분리 권장 |
| 채팅 즉시 사용 | 20~50줄 | 핵심만 남기기 |

---

## §4. 흔한 품질 문제

| 문제 | 증상 | 해결 |
|---|---|---|
| Description 워크플로우 요약 | 스킬이 본문을 무시하고 description대로만 실행 | description에서 절차 제거 |
| 너무 긴 단일 파일 | Claude가 중요 규칙을 놓침 | references로 분리 |
| 운영 모드 없음 | 매번 동일한 방식으로만 실행 | 모드 체계 추가 |
| 금지 사항 없음 | 임의 추론/확정으로 오류 발생 | 금지 사항 섹션 추가 |
| 한국어 트리거 누락 | 한국어로 요청 시 스킬 미발동 | description에 한국어 표현 추가 |
