# GenesysLabs Business Operating Blueprint — Codex instructions

**Primary goal:** design and implement an accurate, richly interactive internal visualization of the GenesysLabs.ai customer-to-operations business model. **Secondary goals:** learn Git, Docker, CI/CD and secure hosting. Do not let tooling work displace business process quality.

## Context-loading protocol (at the start of each new session)

1. **Shared company context** is in the sibling private Git clone `..\Shared-Context` (expected on this Windows workstation at `E:\Experiments\GenesysLabs\Shared-Context`). Verify that it exists and is accessible. Read **`..\Shared-Context\context\COMPANY_CORE.md`**, then selectively `PARTNERS_ECOSYSTEM.md`, `COMMERCIAL_AND_DELIVERY.md`, or `PORTFOLIO_AND_TECHNOLOGY.md` if the task requires them. Don't load the 36KB historical master unless relevant.
2. **Project-specific requirements:** read `docs/OPERATING_MODEL.md` (business specification) and `docs/memory/DECISIONS.md` (domain decisions).
3. **Latest state:** read `docs/PROJECT_STATE.md` and check `git status`, current branch and recent commits before editing.
4. **Engineering handoff:** `docs/CODEX_HANDOFF.md` for app integration, tests, and secondary technology learning.
5. If sibling context cannot be read due to sandbox/workspace permission, **say so explicitly** and request permission for that folder. Never pretend to know the latest shared-context version.

## Scope rules

- Brand spelling: **GenesysLabs.ai**. India engineering and Austria commercial/relationship management are separate actors. KeyValue is a prospective software partner; contract model not finalized.
- Preserve distinctions among **confirmed / working assumption / proposed / exploratory / open question**.
- Keep process roles, contractual entities, payment recipients and logistics routes separate; no implied automatic payment redirect or legal compliance claim.
- Preserve V0.3 app behavior and JSON compatibility unless an approved migration is specified.
- Changes to business processes must update `docs/OPERATING_MODEL.md` and their decision records, not only UI labels.
- Keep PII, account numbers, credentials, confidential customer details, legal docs and secrets out of commits.
- Codex should propose a concise change plan; after approved work, report actual tests and update `docs/PROJECT_STATE.md` and `docs/memory/SESSION_LOG.md`.
- Suggest company-wide knowledge updates via `docs/memory/SHARED_CONTEXT_PROPOSALS.md` instead of directly editing `..\Shared-Context`.
- Do not push/deploy or claim a task was tested unless actually verified and authorized.

## Current paths

- This canonical Git clone: `E:\Experiments\GenesysLabs\Bus-Model`
- Earlier V0.3 prototype ZIP extraction: `E:\Experiments\GenesysLabs\Bus-Oper-Model` (reference, not Git clone)
- Shared knowledge clone (new/proposed): `E:\Experiments\GenesysLabs\Shared-Context`
- GitHub: `https://github.com/Genesyslabs-ai/GenesysLabs_Bus_Process.git` (private)

## Owner hierarchy

A founder's current explicit instruction supersedes older handoff docs. For content conflicts, use current confirmed owner decisions; project `OPERATING_MODEL.md` for process detail, shared context for general company facts, and `PROJECT_STATE.md` only for recent progress. Ask rather than silently resolve material legal/commercial conflicts.
