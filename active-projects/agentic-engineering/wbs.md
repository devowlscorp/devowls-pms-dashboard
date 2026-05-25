# 📊 Agentic Engineering v3.0 - WBS (Work Breakdown Structure)

> **최종 동기화 시각**: 2026-05-25T20:21:35.367Z
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
| **EPIC-01** | Foundation Setup | ✅ DONE | REQ-0101~0004 | [epic-01.md](wbs/epic-01.md) |
| **EPIC-02** | Public UI — 3 Layer | 📅 TODO | REQ-0201~0009 | [epic-02.md](wbs/epic-02.md) |
| **EPIC-03** | Admin Panel | 📅 TODO | REQ-0301~0013 | [epic-03.md](wbs/epic-03.md) |

---

## REQ Master Register

| REQ ID | Epic | WBS Code | Feature Name | Status | Task Contracts |
|---|---|---|---|---|---|
| **REQ-0101** | EPIC-01 | 1.1.1 | Nuxt 4 Init + Dockerfile | ✅ DONE | — |
| **REQ-0102** | EPIC-01 | 1.1.2 | DB Schema + Prisma Migrate | ✅ DONE | ✅ DONE |
| **REQ-0103** | EPIC-01 | 1.1.3 | Better-Auth Setup | ✅ DONE | ✅ DONE |
| **REQ-0104** | EPIC-01 | 1.1.4 | MinIO S3 Wrapper | ✅ DONE | ✅ DONE |
| **REQ-0201** | EPIC-02 | 2.1.1 | Game Map Engine (Canvas 2D) | 📅 TODO | ✅ DONE |
| **REQ-0202** | EPIC-02 | 2.1.2 | Main Page Layer 1 | 📅 TODO | ✅ DONE |
| **REQ-0203** | EPIC-02 | 2.1.3 | Card Roller Layer 2 | 📅 TODO | ✅ DONE |
| **REQ-0204** | EPIC-02 | 2.1.4 | Project Detail Layer 3 | 📅 TODO | ✅ DONE |
| **REQ-0205** | EPIC-02 | 2.1.5 | Public Read API | 📅 TODO | — |
| **REQ-0301** | EPIC-03 | 3.1.1 | Admin Login | 📅 TODO | — |
| **REQ-0302** | EPIC-03 | 3.1.2 | Admin Dashboard CRUD | 📅 TODO | — |
| **REQ-0303** | EPIC-03 | 3.1.3 | Screenshot Upload + Reorder | 📅 TODO | — |
| **REQ-0304** | EPIC-03 | 3.1.4 | Admin Write API | 📅 TODO | — |

---

## Execution Order

```
EPIC-01 (blocking)
  → [병렬] REQ-0101
         → [병렬] REQ-0102 + REQ-0103 + REQ-0104

EPIC-01 완료 후 EPIC-02 + EPIC-03 병렬 착수

EPIC-02:
  [병렬] REQ-0205 (depends: REQ-0102, REQ-0104) + REQ-0201 (depends: REQ-0101)
       → REQ-0202 (depends: REQ-0201)
             → REQ-0203 (depends: REQ-0202, REQ-0205)
                   → REQ-0204 (depends: REQ-0203, REQ-0205)

EPIC-03:
  [병렬] REQ-0301 + REQ-0304
       → REQ-0302
             → REQ-0303
```

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
1. `/stage-define` 실행 → Epic/REQ 기반 todo-*.md 생성
2. 에이전트는 `tasks/todo-xxxx.md` CLAIMED 후 착수
3. Micro REQ는 `todo-xxxx-xx.md` 단위로 단일 세션 처리
4. verify.mjs 통과 전 DONE 금지

*Decision Register: [decisions.md](decisions.md)*
