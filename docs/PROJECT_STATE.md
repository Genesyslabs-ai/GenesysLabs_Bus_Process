# GenesysLabs Business Operating Blueprint — current project state

**Updated:** 2026-11-22. **Status:** M1 local V0.3 baseline integration and verification complete; awaiting review. No new commit, merge, push or deployment.

## Project purpose and hierarchy

- **Main objective:** accurate editable visualization of the GenesysLabs.ai customer-to-operations business process, including branching infra, software/KeyValue, consulting and combined offerings.
- **Technical learning objective:** Git, VS Code Codex, Docker, CI/CD and private hosting (secondary).
- **Company context source:** independent sibling `E:\Experiments\GenesysLabs\Shared-Context` Git clone, verified readable. Company knowledge is referenced there, not copied here; no shared-context files were modified.
- **Project-specific business source of truth:** `docs/OPERATING_MODEL.md`.
- **Technical handoff:** `docs/CODEX_HANDOFF.md` and repository `AGENTS.md`.
- **Decisions / history:** `docs/memory/DECISIONS.md`, `SESSION_LOG.md`.

## Repository and local source

- Canonical GitHub: `https://github.com/Genesyslabs-ai/GenesysLabs_Bus_Process`
- Canonical local Git clone: `E:\Experiments\GenesysLabs\Bus-Model`
- Existing V0.3 source extracted from ZIP: `E:\Experiments\GenesysLabs\Bus-Oper-Model`
- Shared-company local clone remote: `https://github.com/Genesyslabs-ai/GenesysLabs_Shared_Context.git` (verified from local Git configuration; its live remote metadata was not queried).

## Verified integration milestone

- Dedicated branch: `integration/v0.3-baseline`, created from local `main` at `209e7a97c78ccb241e45b5a5ea75f288e9877d70` (`Initial commit`). HEAD is unchanged; nothing is staged.
- Copied `index.html`, `assets/styles.css`, `src/app.js`, `src/blueprint-data.js`, `.editorconfig`, `.dockerignore`, `Dockerfile`, `compose.yaml` and `docs/preview-v03.png`. All nine match the original source byte-for-byte (SHA-256).
- Reconciled README and ignore rules; added a current local-development guide. Preserved the official operating specification, decision log and handoff rather than overwriting them with older prototype docs.
- Updated this state file and session log; added baseline verification and proposed follow-up tasks. `AGENTS.md` and the existing context/handoff docs were already untracked before integration and remain unstaged.
- Ran the same isolated headless Microsoft Edge suite against the original and integrated app using temporary Python loopback HTTP servers. All 22 grouped checks passed, including original-export import into the integrated copy. Details and limits: `BASELINE_VERIFICATION.md`.
- Browser tests covered five views, twelve stage inspectors, stage/subprocess editing, reload persistence, JSON roundtrip/rejection, reset, pan/zoom/focus and laptop rendering. No JavaScript runtime errors occurred; both copies logged an existing missing-resource 404 console warning.
- Hash manifests verified all 14 original prototype files and all 16 non-Git shared-context files remained untouched. The repositories remain independent; no submodule or nested repository was introduced.
- GitHub metadata for the exact `origin` repository reported **private** on 2026-11-22. Recheck immediately before any future authorized push; this observation does not authorize publishing.
- Docker was retained as optional source material and was not run. No CI, deployment, authentication or hosted service was configured. Test servers/browser contexts were closed; review artifacts are outside the application repository in `..\integration-review`.

## Active milestone

**M1 — Local integration and verification complete; review pending.**

| Field | Verified status |
|---|---|
| Branch and HEAD | `integration/v0.3-baseline` at `209e7a9`; no integration commit |
| Git working tree status | README and `.gitignore` modified; app/config/docs additions untracked; nothing staged |
| Prototype integrated | Verified byte-for-byte for all nine copied files; workflows, UI and data format unchanged |
| Local browser test | Original and integrated copies passed the same suite; Edge 157.0.4341.60 |
| Shared-Context clone present | Readable independent Git clone; original local modifications left untouched |
| Commit / merge / push / deploy | None performed; separate approval required |

## Next milestones

1. Review the local integration diff, including untracked additions and pre-existing project docs. Decide separately whether to authorize a commit; no merge or push is implied.
2. Validate an infrastructure path and a KeyValue-only path end-to-end with Joice/Jecko/Arshad. Preserve unresolved commercial/legal gates.
3. Review proposed improvements in `FOLLOW_UP_TASKS.md`, especially explicit exception/rework connections, consistency across views and import validation. No workflow change, UI redesign or schema migration occurred in M1.
4. Verify historical V0.2 JSON compatibility when a representative export is available; current V0.3 roundtrip and cross-copy import are verified.
5. Learn Docker/CI/private hosting only after business app review is reliable, with a separate scope and authorization. Shared-context versioning can be reviewed independently.

## Update protocol

After substantive work, record actual commit/branch, files changed, verified tests, open questions, next product milestone, next infrastructure-learning milestone, and whether changes are local or pushed. Add a concise dated entry to `docs/memory/SESSION_LOG.md`. Propose cross-project facts via `SHARED_CONTEXT_PROPOSALS.md` rather than mutating the company knowledge repository without approval.

## Re-entry prompt for ChatGPT

> Review the latest pushed `Genesyslabs-ai/GenesysLabs_Bus_Process` repository, especially `docs/PROJECT_STATE.md`, `docs/OPERATING_MODEL.md`, and `docs/memory/SESSION_LOG.md`. Summarize the last verified milestone, current business-process gaps, and next priority. Check the latest shared context repo too if installed/connected; do not assume the two repos are synchronized.
