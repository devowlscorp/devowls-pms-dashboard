# 📊 Agentic Engineering v3.0 - WBS (Work Breakdown Structure)

> **최종 동기화 시각**: 2026-05-29T20:31:13.621Z
> **원격 저장소**: [Agentic-Engineering-v3.0](https://github.com/devowlscorp/Agentic-Engineering-v3.0)

---

# WBS Master Index — DevOwls Gaze

> **SSOT**: Epic 상세는 `wbs/epic-xx.md`. REQ 명세는 `task-descriptions/req-xxxx-*.md`. Task Contract는 `tasks/todo-xxxx.md`.
> 이 파일은 Epic 인덱스 + 전체 상태 대시보드.

---

## 5-Layer Structure

```
EPIC (wbs/epic-xx.md)
  └── REQ — Feature (task-descriptions/req-[0-9]{4}-*.md)
        └── Micro REQ (task-descriptions/req-[0-9]{4}-[0-9]{2}-*.md)
              └── TODO — Task Contract (tasks/todo-[0-9]{4}(-[0-9]{2})?.md)
                    └── STEP — Implementation steps (todo 내부 섹션)
                          └── Acceptance Criteria & verify.mjs
```

---

## Epic Status

| Epic | Name | Status | REQs | Detail |
|---|---|---|---|---|
| _(No epics defined. Run /phase-planning to begin.)_ | | | | |

---

## REQ Master Register

| REQ ID | Epic | WBS Code | Feature Name | Status | Task Contracts |
|---|---|---|---|---|---|
| _(Empty. Epics and REQs will be registered here after /phase-planning.)_ | | | | | |

---

## Status Definitions

| Symbol | Meaning |
|---|---|
| 📅 TODO | Backlog / unclaimed |
| 🏗️ DOING | Claimed by active session |
| ✅ DONE | verify.mjs 통과 + synced |
| ⏸️ PAUSED | Blocked |

---

## Protocol
1. `/stage-i-define` 실행 → Epic/REQ 기반 todo-*.md 생성
2. 에이전트는 `tasks/todo-xxxx.md` CLAIMED 후 착수
3. Micro REQ는 `todo-xxxx-xx.md` 단위로 단일 세션 처리
4. verify.mjs 통과 전 DONE 금지

*Decision Register: [decisions.md](decisions.md)*
