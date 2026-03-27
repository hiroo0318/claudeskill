# Claude Skills Library

17년차 모바일 서비스 기획자를 위한 Claude 스킬 라이브러리입니다.

## 구조

```
claude/
├── README.md
└── skill-factory/              ← 스킬 제조소 (마스터 스킬)
    ├── SKILL.md                ← 프로젝트 지침에 등록
    ├── references/
    │   └── library.md          ← 스킬 라이브러리 목록
    └── library/                ← 생성된 스킬들
        └── (스킬 추가될 예정)
```

## 사용 방법

### Claude.ai 프로젝트
`skill-factory/SKILL.md` 내용을 프로젝트 지침(Instructions)에 붙여넣기

### Claude Code
```bash
git clone https://github.com/hiroo0318/claude.git
```
각 스킬 폴더를 Claude Code 스킬 경로에 설치

### 새 스킬 추가
이 프로젝트 채팅방에서 "스킬 만들자" → 자동 설계 → `library/` 폴더에 저장 → GitHub push
