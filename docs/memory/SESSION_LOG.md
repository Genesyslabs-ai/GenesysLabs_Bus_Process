# Business Operating Blueprint — concise session log

## 2026-11-22 — M1 local V0.3 baseline integration

- **Scope:** user-approved baseline only; no business workflow, UI or data-format changes. No commit, merge, push or deployment authorized/performed.
- **Git:** `integration/v0.3-baseline` from `main` at `209e7a97c78ccb241e45b5a5ea75f288e9877d70`; HEAD unchanged, nothing staged. Existing untracked instructions/domain docs preserved.
- **Integration:** nine app/support files copied byte-for-byte; README/ignore rules reconciled, current development guide and follow-up list added.
- **Tests:** 22 grouped checks passed against original and integrated copies in isolated headless Edge 157.0.4341.60, including five views, editing, persistence, JSON roundtrip/cross-copy import, pan/zoom/focus and laptop render; no JavaScript runtime errors. Existing 404 console warning recorded.
- **Preservation:** all 14 reference files and 16 non-Git Shared-Context files unchanged by SHA-256 manifests; independent repos retained, no company-context copy.
- **Remote:** exact application `origin` reported private via GitHub metadata on 2026-11-22; recheck before any future authorized push.
- **Limits:** historical V0.2 export not supplied; Docker/CI/hosting not tested or configured. Existing importer and view-model gaps remain follow-up proposals.
- **Next:** review full local diff and evidence, then partner validation of infrastructure and software journeys. See `../PROJECT_STATE.md` and `../BASELINE_VERIFICATION.md`; raw results/screenshots/harness are in `..\integration-review` beside the repo.

## 2026-11-22 — Context architecture handoff (V0.5)

- **Business:** Preserve customer-to-operations alpha, 12-stage flow and four routes. Contracting entity vs payment vs logistics remain separate.
- **Technical:** V0.3 static prototype available in old extracted folder; official Git clone in `Bus-Model`. Git integration not yet verified.
- **Knowledge:** designed sibling private shared-context repo + root per-project `AGENTS.md`; files prepared but not installed/committed.
- **Next:** Verify repo and sibling folder, integrate V0.3 and project docs, local browser test, update state and request Git push approval.

Subsequent entries should be short (5–10 lines), dated, refer to commit SHA if available, distinguish tests from assumptions, and link to `PROJECT_STATE.md` for current status. Do not paste full chat transcripts.
