# GenesysLabs.ai — Business Operating Model (working specification v0.5)

**Purpose:** This is the domain specification for the internal interactive **GenesysLabs Business Operating Blueprint**. It describes the customer-to-operations journey, not a generic supply-chain diagram. Treat it as a **working draft** for partner workshops, not a legally approved SOP.

**Project priority:** Accuracy and completeness of the business operating model come **before** technical sophistication, CI/CD, Docker, frameworks or deployment. Technology is a means to make the operating model easy to inspect, discuss, edit, version and eventually operate.

## A. Confirmed design decisions

1. **Genesys Austria** is the **default customer-facing contracting and invoicing entity**. This is a working default, not a claim that all hardware advances should be received there or that every transaction has been legally validated.
2. Two hardware logistics routes are in scope: **India → Austria staging → EU customer** AND **India → EU customer directly**, depending on the deal.
3. This application is **internal-only for Genesys partners/team** at this stage. Do not publicly host internal workflows or customer-sensitive details.
4. Prototype first: standalone offline-first HTML/CSS/JS, with editable workflow data, visual views and JSON import/export. A React/TypeScript migration, Docker, private hosting and CI/CD are optional later learning/evolution milestones, not today's primary work.
5. There may be distinct business routes for **infrastructure**, **software via KeyValue**, **consulting-only**, and **combined infrastructure + software**. A single opportunity may branch, rejoin or lead to cross-selling.
6. The company spelling in deliverables is **GenesysLabs.ai** (not Genesis Labs or Genesys when referring to the canonical brand).

## B. The company and relevant actors

- **European customer:** may be an enterprise, SME, research institute or other buyer; initiates opportunity, supplies information, decides, approves, pays and accepts delivery.
- **Genesys Austria / EU:** commercial customer interface; customer acquisition, lead qualification, workshops, offers, deal coordination and local relationship/support as agreed.
- **Joice — CCO / GTM and Commercial Lead:** lead qualification, commercial discovery, customer coordination, offers, partner/business communication, account management.
- **Jecko — CAIO / AI Strategy:** customer AI/workload discovery, architecture/solution strategy, technical evaluation, technical positioning.
- **Arshad — CTO / India Engineering:** feasibility, infrastructure solution architecture, BOM and engineering validation, sourcing/build/integration, FAT/QA, technical delivery planning.
- **Genesys India:** existing engineering/supplier/build ecosystem; actual legal seller/subcontractor and inter-entity responsibilities depend on the specific agreement.
- **KeyValue Systems:** prospective partner for software, AI products, agentic solutions/Nethra SDK, evaluation and development. *Commercial and contractual partner model is not yet final.*
- **Other parties:** component OEMs/distributors; courier/freight/insurance/customs brokers; Austrian installer/service organization; customer procurement/security/legal teams; tax/legal advisers; optional future solution partners.

## C. Top-level customer journey — 12 stages

| ID | Stage | Core outcome | Example subprocesses, decisions and documents |
|---|---|---|---|
| 01 | First contact and lead capture | Opportunity identified | Inbound/outbound, events, referrals, first pitch; lead record, consent/permission to follow up |
| 02 | Initial qualification | Fit, buyer and urgency understood | First customer call with commercial lead, needs/budget/timeline, go/nurture/no-go |
| 03 | NDA and due diligence (if needed) | Confidential exchange is authorized | NDA when appropriate, signer/entity, registration/VAT details, evidence/certifications, references, onboarding docs |
| 04 | Technical engagement | Technical problem and feasibility understood | Introduce Jecko/Arshad/India, workload and delivery discussions, initial feasibility and preliminary constraints |
| 05 | Engagement route selection | One or more business routes chosen | Infrastructure vs software vs consulting vs combined; commercial model and responsible entities |
| 06 | Assessment and design | Analysis and proposed solution produced | Scope paid consulting, questionnaires, customer answers, workload sizing/TCO/BOM/architecture, recommendation/report |
| 07 | Proposal, negotiation and contracting | Authorized order and terms | Offer, SoW/MSA if applicable, PO, SLA for service scope, taxes/payment milestones, deposits and credit policy |
| 08 | Procurement and execution | Solution built or developed | Supplier orders, engineering, assembly, integration; software PoC/dev/implementation; cost, quality and schedule checks |
| 09 | Logistics and fulfilment | Hardware reaches site where applicable | Factory QA/FAT, export documents, freight, insurance, customs, importer of record, Austria staging OR direct customer delivery |
| 10 | Deployment and customer acceptance | Customer signs off agreed solution | Installation/commissioning, configuration, site tests/SAT/UAT, benchmarks, documentation, handover, acceptance and final payments |
| 11 | Support and maintenance | Operate and resolve incidents | Warranty, SLAs where contracted, remote/local support, monitoring, preventive maintenance, spare parts, RMA, change management |
| 12 | Renewal, expansion or exit | Relationship intentionally continues or ends | GPU upgrades, platform/software add-ons, managed services, renewal, transition, offboarding or close-out |

The model **must** include failure and rework paths: customer declines, unclear needs, NDA not agreed, assessment fee declined, proposal rejected, revised scope, advance-payment failure, component delay, customs hold, transit damage, failed acceptance, incident escalation, warranty claims, cancellation and non-renewal.

## D. Business-route variation

### Route A — Infrastructure (AI/HPC physical systems)

Initial contact → qualification → (NDA) → Joice/Jecko/Arshad technical discovery → possible **paid workload/sizing assessment** → consultant's recommendation/architecture/TCO/BOM → quote/order/contract & payment gates → India sourcing/build/integration/QA → choose direct shipping or Austria staging → customs/logistics → installation and acceptance → warranty/service/expansion.

**Critical pricing design:** early exploratory calls may be free; deeper questionnaire/analysis can be a **paid consulting engagement**. Whether this fee is **credited against a later qualifying purchase**, by how much, on what timeframe, and by which contracting entity is an **open commercial policy**, not an automatic refund.

### Route B — Software (KeyValue Systems or future partner)

Initial contact → qualify software opportunity → partner intro → demonstration or PoC/technical discovery (as appropriate) → clarify **referral vs reseller vs prime contractor vs joint delivery** → agreed proposal/contract/IP/support → KeyValue software delivery → tests and customer acceptance → support/renewal or expansion.

**Important:** This route may **skip the paid infrastructure assessment** and has no default physical shipping subprocess. A separate paid discovery sprint is an option, not a mandatory gate.

### Route C — Consulting-only

Intro/discovery → scope deliverable and fee **before substantial billable work** → consulting offer/SoW → questionnaire and customer answers → analysis/assessment/blueprint → findings workshop and report → invoice/close, or conversion into infrastructure/software opportunity with explicit credit terms if offered.

### Route D — Combined (infra + software)

One shared customer opportunity with parallel infrastructure and application workstreams; clarify lead contractor, partner subcontracting, integration responsibilities, IP/licenses, commissioning/UAT, single or staged acceptance, integrated incident handling, and renewal/expansion.

## E. Four independent flows to model (do not conflate)

1. **Customer interaction / business process:** who speaks to whom, what decisions unlock the next step.
2. **Contractual / legal entity flow:** seller of record, who signs NDA/MSA/SoW/PO/SLA, warranty, indemnities, partner agreement, IP ownership.
3. **Financial flow:** who invoices whom, advances, consulting fees, hardware payments, currency, revenue share/referral fee, inter-entity settlements, payment milestones, credits; validate against actual seller-of-record model.
4. **Physical / operational supply chain:** supplier → India integration/QC → shipment → customs/importer → staging or direct-to-site → installation/acceptance → RMA/spares.

An Austrian customer contract **does not itself authorize directing advance payments to India**. The contracting, invoicing, VAT/customs and liability treatment must be checked with qualified professionals. Similarly, a direct ship-to-customer flow does not automatically establish importer-of-record or warranty ownership.

## F. Required views and interaction model

- **End-to-end lifecycle view:** 12-stage top-level clickable path, zoom/pan and clear decision/branch edges.
- **Business routes view:** infrastructure, KeyValue software, consulting and combined. Support branches, alternatives and rejoin points.
- **Swimlane / RACI-like responsibilities view:** customer, Austria commercial, AI strategy, India engineering, software partner, OEM/logistics and service/support.
- **Contracts and money view:** show separate signer, invoice issuer, payment recipient, commercial gate, fee/credit, and unresolved tax/legal review.
- **Physical supply-chain view:** BOTH shipment routes, transitions and exception routes.
- **Drilldown:** click stage → inspector → subprocess detail with owner, trigger, inputs, outputs, decisions, documents, lead time (only if sourced), financial/legal implications, questions and notes.
- **Editing:** edit node descriptions, substeps, status and notes; add links/branches in later versions; import/export versioned JSON; preserve existing exported JSON until a deliberate migration.
- **Clarity:** distinct visual states for `confirmed`, `proposed`, `open`, `needs_review`; avoid visually asserting proposals are implemented policy.

## G. Suggested process-node record

A stage/substage can carry:

- Stable `id`, `title`, `type` (`activity`, `decision`, `handoff`, `document`, `payment`, `exception`), `route(s)`.
- `owner_role`, `participants`, `legal_entity`, `country`, `trigger`, `inputs`, `actions`, `outputs`.
- `prerequisites`, `decision_conditions`, `outgoing_connections`, `rollback/rework/exit`.
- `required_documents`, `commercial_terms`, `payments`, `shipping_requirements`, `compliance_gates`.
- `status`, `reviewer`, `last_reviewed`, `notes`, `open_questions`, `source/decision_reference`.
- Separately store layout/presentation geometry so a diagram redesign does not rewrite business facts.

Do **not** treat this as a forced schema migration for V0.3. First preserve current app/data behavior, then propose backwards-compatible upgrades.

## H. Legal, financial and organizational matters deliberately OPEN

- Formal legal relationship India↔Austria and whether Austria is seller for every product type.
- Importer/exporter of record, Incoterms, EU product conformity, transit insurance, title and risk transfer, local stock/staging feasibility.
- Hardware advance payment recipient vs invoice issuer; VAT and customs; foreign exchange, intercompany settlements and applicable tax requirements.
- Warranty/RMA/local parts/installation obligations, support escalation, service credits, component substitutions.
- What corporate/certification documents can be used by the EU entity; signatory authority; customer onboarding/security requirements.
- Paid consulting package, pricing, partial/full purchase credit, expiration, termination and non-purchase treatment.
- KeyValue referral margin vs reseller margin vs prime contracting, software IP/licensing, PoC costs, maintenance and customer ownership.

**Never invent a final answer to these inside the app.** Represent them as unresolved checkpoints with proposed options, an owner, and a required confirmation.

## I. Product-development priority and acceptance criteria

**Priority 1 — Business-process quality:** validate the 12 stages and four routes with partner stakeholders; expose who does what, when, why, and under which commercial/legal condition. Present unresolved branches clearly.

**Priority 2 — Usable interactive visualization:** legible at laptop resolution; strong visual hierarchy; polished UI; intuitive drilldown/editing; reliable local save/export/import and backward compatibility.

**Priority 3 — Developer workflow:** private GitHub repo, clear README, local test instructions, reproducible commits, small reviewable changes. Python's `python -m http.server` is sufficient for the static prototype.

**Priority 4 — Optional infrastructure learning:** Docker, CI/checks, and authenticated hosting after the workflow is usable; avoid making these prerequisites or using Kubernetes for a static app.

**Business acceptance:** a partner can trace an infrastructure deal and a KeyValue-only software deal from lead through delivery/support; see alternate shipping/payment routes; click any stage to view responsible actors, artifacts and approvals; see what is assumed versus decided; and identify where the business needs a leadership/legal/accounting decision.

## J. Working agreement

- This document is the **project business-domain source of truth**; shared company facts are in the adjacent private `Shared-Context` clone. `docs/CODEX_HANDOFF.md` explains development tasks. `docs/PROJECT_STATE.md` records recent progress.
- When founders confirm a new operating decision, update this specification and the affected application nodes in the same development change.
- Do not silently transform the business logic while polishing the UI.
- Avoid committing customer names, contracts, pricing, secrets or private supplier data without deliberate review.
- Review this document with Joice/Jecko/Arshad before calling the model an approved SOP. External partner arrangements are exploratory unless formally confirmed.
