# 📊 Agentic Engineering v2.0 - WBS (Work Breakdown Structure)

> **최종 동기화 시각**: 2026-05-21T20:24:40.935Z
> **원격 저장소**: [Agentic-Engineering-v2.0](https://github.com/devowlscorp/Agentic-Engineering-v2.0)

---

# Project Roadmap & Work Breakdown Structure (WBS)

## 1. High-Level Status Dashboard

| Epic | Status | Progress | Notes |
| :---- | :---- | :---- | :---- |
| **[epic-0] Rebuild & Core Migration** | ✅ COMPLETED | 100% | Prisma, BetterAuth, S3 utils, and API handlers present. |
| **[epic-1] Feature Verification & Polish** | ✅ COMPLETED | 100% | Auditing individual flows for runtime stability. |
| **[epic-2] Pending Features** | 📅 TODO | 0% | New features and legacy functional ports awaiting restoration. |
| **[epic-3] Refinements** | 🚧 IN PROGRESS | 64% | Visual improvements, stability audits, and optimizations. |
| **[epic-4] Universal Mobile UX/UI Polish** | ✅ COMPLETED | 100% | Ergonomic scaling, typography & touch target optimization. |
| **[epic-5] Data Recovery & Supabase Migration** | ✅ COMPLETED | 100% | Syncing legacy Supabase DB, migrating S3 buckets & fixing local DB runtime. |
| **[epic-6] DevOps & DX Infrastructure** | ✅ COMPLETED | 100% | Automated verification workflow optimization & log consolidation. |
| **[epic-7] Emotional Weather Ecosystem** | ✅ COMPLETED | 100% | Real-time KMA integration & Watercolor Map UI. |
| **[epic-8] Profile & User System** | 📅 BACKLOG | 0% | Profile components, composables, collection store — pending migration. |
| **[epic-9] Admin Panel Expansion** | 📅 BACKLOG | 0% | Categories, i18n, menus, play/rps admin, storage, weather admin. |
| **[epic-10] Auth & Access Control Flows** | 📅 BACKLOG | 0% | Email modals, RBAC + locale global middleware, auth routes. |
| **[epic-11] Common UI Component Library** | 📅 BACKLOG | 0% | Form components, navigation UI, Jeju brand components, ambient sidebar. |
| **[epic-12] Play / Seasonal Mini-Games** | ✅ COMPLETED | 100% | Full RPS engine + NewYear, Reze, Santa seasonal games. |
| **[epic-13] Discovery & Social Engagement** | 📅 BACKLOG | 0% | Collections, trending, search modal, tags recommendation, chat DM routing. |
| **[epic-14] Content, FAQ & Utilities** | 📅 BACKLOG | 0% | FAQ pages, path/trail page, music API, webhooks, health/seed endpoints. |
| **[epic-15] Server API Gap Closure** | 📅 BACKLOG | 0% | AI APIs, common codes, Kakao composables, Prisma types, plugins. |
| **[epic-16] Orchestration Architecture** | ✅ COMPLETED | 100% | Token efficiency, tiered verify, plan cross-validation, HTTP-only Gemini boot. |
| **[epic-17] Project Management Migration** | ✅ COMPLETED | 100% | WBS standardization: decisions.md separation, backlog restructure, TODO 1:1 principle, Ref.File normalization. |
| **[epic-18] WBS Dashboard Vue 3 Migration & ESM Script Conversion** | ✅ COMPLETED | 100% | Vue 3 CDN dashboard migration & CJS→MJS ESM conversion. |

## 2. Per-Epic Detail Files

Each epic's full task table lives in `.plan/wbs/epic-XX.md`.
Load only the epic file relevant to your current REQ-ID.

| File | Epic |
| --- | --- |
| [epic-00.md](wbs/epic-00.md) | Rebuild & Core Migration |
| [epic-01.md](wbs/epic-01.md) | Feature Verification & Polish |
| [epic-02.md](wbs/epic-02.md) | Pending Features |
| [epic-03.md](wbs/epic-03.md) | Refinements |
| [epic-04.md](wbs/epic-04.md) | Universal Mobile UX/UI Polish |
| [epic-05.md](wbs/epic-05.md) | Data Recovery & Supabase Migration |
| [epic-06.md](wbs/epic-06.md) | DevOps & DX Infrastructure |
| [epic-07.md](wbs/epic-07.md) | Emotional Weather Ecosystem |
| [epic-08.md](wbs/epic-08.md) | Profile & User System |
| [epic-09.md](wbs/epic-09.md) | Admin Panel Expansion |
| [epic-10.md](wbs/epic-10.md) | Auth & Access Control Flows |
| [epic-11.md](wbs/epic-11.md) | Common UI Component Library |
| [epic-12.md](wbs/epic-12.md) | Play / Seasonal Mini-Games |
| [epic-13.md](wbs/epic-13.md) | Discovery & Social Engagement |
| [epic-14.md](wbs/epic-14.md) | Content, FAQ & Utilities |
| [epic-15.md](wbs/epic-15.md) | Server API Gap Closure |
| [epic-16.md](wbs/epic-16.md) | Orchestration Architecture |
| [epic-17.md](wbs/epic-17.md) | Project Management Migration |
| [epic-18.md](wbs/epic-18.md) | WBS Dashboard Vue 3 Migration & ESM Script Conversion |

---

## 3. Agent Protocol for WBS Interaction

1. **Contract First**: DO NOT begin coding without creating an `active-tasks/TODO_xxx.md` mapped to the current active **REQ-ID**.
2. **Evidence Driven**: Only mark tasks as DONE after terminal/browser validation logs are recorded in `.testing/`.
3. **Sync Ready**: Keep status accurate so the `/sync` workflow can publish up-to-the-minute project health.
4. **Epic-File Only**: When updating a task status, edit only the relevant `wbs/epic-XX.md` — not this index.

"Reality guides the WBS. Not assumptions."

---

> Decision Register: [`.plan/decisions.md`](decisions.md)
