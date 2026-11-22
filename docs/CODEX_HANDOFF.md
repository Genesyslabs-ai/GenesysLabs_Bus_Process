# GenesysLabs.ai — Codex project handoff v0.5

> **Business-first.** The customer-to-operations app is the deliverable. Git, Docker, CI/CD and hosting are parallel educational infrastructure.

## First: read the repository's root `AGENTS.md`

It defines our shared-company vs project-specific memory hierarchy and the required adjacent local `Shared-Context` clone. After reading it, load `docs/OPERATING_MODEL.md`, `docs/PROJECT_STATE.md` and `docs/memory/DECISIONS.md`. If shared context isn't installed yet, mention that clearly and use the docs in this repository without silently guessing.

## The business goal

Create an internal editable, drill-down visualization of GenesysLabs.ai's full European customer journey, from lead first contact through NDA/due diligence, Austria and India technical discovery, paid assessment where appropriate, proposal and legal/commercial gating, infrastructure build or KeyValue software execution, shipping/installation, acceptance, support, renewal or exit.

A customer may choose infrastructure, software, consulting-only, or combined delivery. There must be **separate views** for customer journey, participants/owners, contracts, money and goods. Decisions, exceptions and rework must be representable; unapproved legal/commercial steps should be visibly provisional.

For all functional details and the 12 lifecycle stages, use `docs/OPERATING_MODEL.md` as authoritative.

## Current project state / directories

- Git clone: `E:\Experiments\GenesysLabs\Bus-Model` — **modify code here**.
- V0.3 HTML prototype (ZIP extraction): `E:\Experiments\GenesysLabs\Bus-Oper-Model` — inspect and merge as source; preserve it as reference until integration is verified.
- Shared context (new/proposed clone): `E:\Experiments\GenesysLabs\Shared-Context` — company knowledge only, not where application code belongs.
- Remote: `https://github.com/Genesyslabs-ai/GenesysLabs_Bus_Process.git` (private at the last verified check; recheck if publishing).
- Do not claim prototype is already committed to remote until you inspect the actual `main` branch and verify.

## Immediate task, if V0.3 not yet integrated

1. Check `git status`, `git remote -v`, current branch and existing files.
2. Read V0.3 prototype from local extracted folder; request permission if outside your workspace; do not invent source if access is denied.
3. Give the user a short proposed integration plan, preserving remote history and any existing scaffold.
4. Merge files into the Git clone; preserve five views, click/zoom/pan, editing, local save and JSON import/export, and backward compatibility.
5. Test via a simple local server (`python -m http.server 8000`), report actual outcomes and limits.
6. Update project state and session log. Show `git diff`/`git status`; request approval before committing or pushing.

## Later product priorities

- P0: Partner validation of business stages and route/exception logic; clear distinction of assumptions from policies.
- P1: Premium intuitive visual app UX without changing unapproved business logic.
- P2: Structured, versioned business-process data model, linked documents/roles/approvals, reliable import/export.
- P3: Secondary developer learning path — Git branches/PRs, Docker, CI, authenticated hosting. No forced React migration or Kubernetes.

## How to keep ChatGPT in sync

After a meaningful milestone, update `docs/PROJECT_STATE.md` and `docs/memory/SESSION_LOG.md`, then commit/push when approved. GitHub tracks committed source; ChatGPT can inspect it via its connected GitHub integration. It **cannot** infer local edits or see private Codex session history automatically. Project-specific updates stay local to this repo; cross-project update proposals go into `docs/memory/SHARED_CONTEXT_PROPOSALS.md` for founder approval.
