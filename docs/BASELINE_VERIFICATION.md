# V0.3 baseline integration verification

**Date:** 2026-11-22 (Europe/Vienna). **Result:** local integration and verification passed; review pending. No integration commit, merge, push or deployment.

## Method and scope

Branch `integration/v0.3-baseline` retains HEAD `209e7a97c78ccb241e45b5a5ea75f288e9877d70`. Application entry point, JavaScript, CSS and default process data were copied without edits from `..\Bus-Oper-Model`. Documentation/configuration reconciliation does not alter runtime behavior.

Playwright 1.65.2 drove the installed Microsoft Edge 157.0.4341.60 headlessly with fresh isolated contexts. Both source and integrated application were served by temporary Python HTTP servers bound to `127.0.0.1`. Test edits affected disposable browser storage only. Browser contexts and test servers were closed after verification. Existing personal browser sessions were not used.

The external review directory `E:\Experiments\GenesysLabs\integration-review` contains the test harness (`verify_baseline.py`), its separately installed Python test dependencies (`python-deps`), raw `test-results.json`, hash manifests and screenshots. These are local review material outside the application and shared-context repositories. Run the harness again with `python ..\integration-review\verify_baseline.py` on this workstation if verification is needed after a change.

## Results

The harness recorded **22 passed grouped checks**: one nine-file parity check, nine groups against the original, ten against the integrated copy (including cross-copy import), and two preservation checks.

| Area | Verified result |
| --- | --- |
| File parity | SHA-256 matches for `index.html`, both JS files, CSS, `.editorconfig`, `.dockerignore`, `Dockerfile`, `compose.yaml` and preview PNG |
| Initial load / stage navigation | HTTP 200, twelve expected stage IDs and all twelve clickable inspectors |
| Five views | Lifecycle, four route lanes, six responsibility lanes, four contracts/payment sections, and both shipping routes plus reverse logistics |
| Linked drilldowns | Stage links in each non-lifecycle view open the expected inspector |
| Inspector / stage editing | Three tabs, title/owner/status/notes editing and saved values after reload |
| Subprocess editing | Open/select/edit, add/remove a step, and retained changes after reload |
| JSON export | Download parsed as `genesyslabs-blueprint`, version `0.3`, twelve stages |
| Import / persistence | Exported edited stage data roundtrips exactly and remains after reload; reset restores template |
| Cross-copy compatibility | JSON exported from the original prototype imports into the integrated copy without losing stage data |
| Invalid imports | Malformed JSON and incompatible schema are rejected without replacing current stage data |
| Canvas controls | Zoom in/out, mouse-wheel zoom, drag pan, fit and focus-mode toggle |
| Help / keyboard | Help opens and Escape closes it |
| Laptop layout | Screenshots at 1440x900 (all five views) and 1366x768 (lifecycle); integrated laptop screenshot visually inspected and byte-identical to the original laptop screenshot |
| Runtime errors | No JavaScript page errors during either suite; both copies logged one existing missing-resource 404 console message |
| Reference preservation | All 14 files in `Bus-Oper-Model` match their pre-integration manifest |
| Shared-context preservation | All 16 non-Git files match their pre-integration manifest; independent repository retained |

## Limits and deferred work

- The importer was exercised through its file input; a native operating-system file picker was not part of the headless suite.
- The 404 console message is consistent with the prototype having no favicon; it was not a JavaScript runtime failure. No favicon or other runtime asset was added during this integration.
- Historical V0.2 exports were not available. The existing storage key, schema, importer and default data remain unchanged, but this is not evidence that every historical export is compatible.
- Invalid-import tests cover malformed JSON and wrong schema, not all missing fields or malicious inputs. Existing validation gaps are recorded in `FOLLOW_UP_TASKS.md`.
- Laptop screenshots preserve the existing dense overview; partner readability and full keyboard/accessibility review remain future UX work. No redesign was performed.
- No cross-browser matrix, Docker execution, CI, hosted authentication, shared persistence or business-policy validation was performed.

## GitHub and review state

The GitHub connector queried `Genesyslabs-ai/GenesysLabs_Bus_Process`, matching the configured `origin`, and returned `visibility: private` on 2026-11-22. Reverify current visibility immediately before a future authorized push. The shared-context remote was identified from local configuration only; its live visibility was not queried.

The initial repository tracks only README and `.gitignore`. The root instructions and domain/memory documents were already untracked at integration start. Review all untracked additions as well as the ordinary tracked-file diff. Nothing was staged, committed, merged, pushed or deployed.

`git diff --check` passed for tracked-file changes. The external review directory contains `full-working-tree.patch` (all 21 tracked/untracked files relative to HEAD, including the preview binary), `tracked-files.patch`, `milestone-doc-updates.patch` (state/log changes against their pre-integration local contents), `file-inventory.json` (distinguishes existing untracked files from integration additions), and `git-status.txt`.
