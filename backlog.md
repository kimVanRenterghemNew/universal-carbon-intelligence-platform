# Product Backlog and Handoff — Universal Carbon Intelligence Platform

> Priority: **MVP** = Phase 1-2 delivery, **Later** = Phase 3-4

This backlog is intentionally written as a delivery handoff, not as a locked implementation spec. It should help a product, design, and engineering team pick up the work, challenge assumptions where needed, and turn the platform into a phased roadmap.

## Working Assumptions

- Proposal can stay as-is.
- The platform remains centered on carbon intelligence, integrity analysis, due diligence, pricing, and portfolio monitoring.
- Identity should be passwordless by default via FIDO or passkeys.
- Authorization should be claims-based rather than a simple hard-coded role matrix.
- A document-oriented store is a strong fit for ingested source material and extracted project dossiers.
- A graph model is still attractive for trading relationships, ownership links, counterparty exposure, and network-style market analysis.
- Mobile support should be deliberately designed, not treated as an automatic by-product of desktop screens.

## What Needs To Be Decided Early

These are the first handoff questions the next team should settle before building too much:

1. Do we want a hybrid persistence model:
	- document store for project dossiers, ingestion payloads, extracted summaries, and workflow state
	- relational sidecar for operational consistency and reporting
	- graph store for trading, ownership, linkage, and network analytics
2. Or do we deliberately go graph-first for almost everything and accept the extra modeling and query complexity?
3. Is the first release single workspace, multi-workspace, or full multi-tenant?
4. Do we want invite-only onboarding for MVP, or self-serve sign-up with approval?
5. Which claims are platform-global and which are workspace-scoped?
6. How much of the MVP must be genuinely mobile-friendly versus mobile-viewable?

## Recommended Direction For The Handoff

Use this as the default recommendation unless discovery proves otherwise:

- Identity: FIDO or passkeys first, no password lifecycle.
- Access control: claims-based access, with claims attached to workspace membership and business function.
- Core project data: document-first storage model for ingestion payloads, extraction results, project narratives, diligence bundles, and analyst annotations.
- Trading intelligence: graph-backed model for relationships between projects, issuers, brokers, buyers, holdings, transaction paths, and influence or exposure analysis.
- Operational consistency: keep a narrow operational store for jobs, audit events, workflow states, notifications, and reporting if needed.
- UI delivery: desktop-first for analyst workflows, plus a separate mobile wireframe and mobile backlog slice.

## Delivery Structure

### Phase 0 — Discovery and Architecture Alignment

Goal: remove the biggest product and platform risks before implementation starts.

#### Research Track R0.1 — Claims Model
Question: what claims exist, who grants them, and how are they evaluated?

Output expected:
- claims catalog
- claim naming convention
- scope model: platform, workspace, project, or transaction
- example access tokens or session claims payloads
- rules for temporary, delegated, and time-bound claims

Tasks:
- [ ] Define candidate claims for ingestion, AI review, integrity review, pricing, trading, portfolio, admin, and audit access
- [ ] Decide whether claims are role-derived, directly assigned, or both
- [ ] Model workspace membership plus claims inheritance
- [ ] Define approval flow for sensitive claims
- [ ] Define how claims appear in UI and audit history

#### Research Track R0.2 — Passwordless Identity
Question: how do invite, registration, recovery, and device management work without passwords?

Output expected:
- onboarding flow
- login flow
- step-up authentication flow for sensitive actions
- recovery policy
- device lifecycle policy

Tasks:
- [ ] Choose passkey and FIDO support strategy for web and mobile browsers
- [ ] Define invite-only onboarding versus open registration flow
- [ ] Define device enrollment and friendly device labels
- [ ] Define lost-device recovery with admin-assisted and backup-device options
- [ ] Define step-up auth for high-risk actions like claim approval or trading authorization

#### Research Track R0.3 — Persistence Topology
Question: where should graph, document, and operational data live?

Output expected:
- architecture decision record for graph-first versus hybrid
- query ownership map by module
- operational boundaries for each store
- migration and reporting implications

Tasks:
- [ ] Compare document store plus graph sidecar versus graph-first approach
- [ ] List the top 20 platform queries and assign their best-fit storage model
- [ ] Validate whether trading, ownership lineage, and counterparty exposure clearly justify a graph store
- [ ] Validate whether ingestion payloads, project dossiers, and extraction outputs are easier to manage in a document store
- [ ] Decide which events and audits must remain append-only and easy to export

#### Research Track R0.4 — Mobile Scope
Question: what must mobile users actually do in version one?

Output expected:
- mobile user personas
- must-have mobile tasks
- what remains desktop-only for MVP
- mobile design principles and navigation model

Tasks:
- [ ] Decide whether mobile users are reviewers, executives, operators, or all three
- [ ] Define the top mobile jobs to be done
- [ ] Identify desktop-only screens for MVP
- [ ] Define notification-driven entry points for mobile
- [ ] Set accessibility and performance constraints for mobile web

### Phase 1 — Identity, Onboarding, and Access Foundation

Goal: users can enter the system, join a workspace, and receive claims safely.

#### Epic 1.1 — Invite and Workspace Onboarding
Outcome: a user receives an invite, joins a workspace, sets context, and lands in the right workflow.

Stories:
- As an invited user, I want a clear onboarding flow so I understand what this platform does and what data I can access.
- As a workspace admin, I want to invite people into a workspace with an initial claim bundle.
- As a new analyst, I want my first session to explain ingestion, AI review, integrity flags, and due diligence workflows.

Tasks:
- [ ] Design invite flow and invite acceptance states
- [ ] Design onboarding sequence with workspace context, role explanation, and first-run guidance
- [ ] Add claim-aware landing rules so different users land in different starting modules
- [ ] Define audit events for invite, acceptance, claim grant, and claim denial

#### Epic 1.2 — Passkey or FIDO Authentication
Outcome: users authenticate without passwords and can manage enrolled devices.

Stories:
- As a user, I want passkey or FIDO login so I do not need a password.
- As an admin, I want strong authentication for privileged actions.
- As a user, I want to manage trusted devices and recovery options.

Tasks:
- [ ] Design passkey registration screen
- [ ] Design passwordless login and device selection flow
- [ ] Define device management UI and recovery journey
- [ ] Define re-authentication rules for sensitive admin or trading actions
- [ ] Define error states for unsupported browsers and failed ceremonies

#### Epic 1.3 — Claims-Based Authorization
Outcome: feature access is granted through claims, not only through static roles.

Stories:
- As an admin, I want to grant claims per workspace membership so access is explicit and reviewable.
- As a user, I want to request additional claims with a reason.
- As an auditor, I want a complete history of claim changes and access decisions.

Tasks:
- [ ] Define claim catalog and grouping
- [ ] Design claim request and approval workflow
- [ ] Design workspace member detail screen with effective claims, inherited claims, and pending requests
- [ ] Design access denied states that explain what claim is missing
- [ ] Define append-only audit model for claim lifecycle events

### Phase 2 — Data Foundation and Core Operations

Goal: ingest, normalize, and observe core data pipelines.

#### Epic 2.1 — Registry and Source Ingestion
Outcome: the platform can pull structured registry data and show operator health.

Tasks:
- [ ] Define connector contract per source
- [ ] Prioritize initial registries and source types
- [ ] Define normalized project dossier shape
- [ ] Define ingestion health dashboard requirements
- [ ] Define retry, quarantine, and manual review flows

#### Epic 2.2 — Document Dossier Pipeline
Outcome: unstructured reports become structured project records linked to evidence.

Tasks:
- [ ] Define document ingestion pipeline stages
- [ ] Define extraction schema and evidence references
- [ ] Define human validation workflow for high-impact fields
- [ ] Define how corrected extractions flow back into the dossier

#### Epic 2.3 — Geospatial Layer
Outcome: projects and flags can be visualized spatially with reliable geometry processing.

Tasks:
- [ ] Define geometry ingestion and CRS validation approach
- [ ] Define overlap and proximity detection rules
- [ ] Define project map interactions and saved views

### Phase 3 — Analyst Workflows

Goal: analysts can review integrity, score projects, and produce investment-ready outputs.

#### Epic 3.1 — AI Review and Evidence Validation
- [ ] Analyst extraction review screen
- [ ] Source trace and evidence viewer
- [ ] Finding, warning, and suggestion workflow
- [ ] Override and correction audit trail

#### Epic 3.2 — Integrity Detection
- [ ] Integrity queue
- [ ] Evidence-led investigation screen
- [ ] Resolution workflow with analyst commentary
- [ ] Alerting rules for overlap, dormancy, and issuance anomalies

#### Epic 3.3 — Dynamic Risk Scoring
- [ ] Score dimensions and methodology note
- [ ] Score breakdown and comparison screens
- [ ] Score history and explainability views

#### Epic 3.4 — Due Diligence
- [ ] One-screen diligence summary
- [ ] Missing data tracker
- [ ] PDF and shareable output definition

### Phase 4 — Market, Trading, and Relationship Intelligence

Goal: connect market activity and network analysis to the rest of the platform.

#### Epic 4.1 — Trading Relationship Graph
Outcome: the team can model linked entities and flow-based trading intelligence.

This is the strongest justification for introducing a graph store.

Suggested use cases:
- project to issuer relationships
- project to broker relationships
- buyer to portfolio relationships
- ownership transfer chains
- transaction path analysis
- concentration and exposure analysis
- suspicious circular flows or repeated counterparty patterns

Tasks:
- [ ] Define graph entities and relationship types for trading and ownership
- [ ] Define which market queries must run against the graph
- [ ] Define boundaries between graph data and document-backed project dossiers
- [ ] Define synchronization pattern between operational workflows and graph updates

#### Epic 4.2 — Liquidity and Pricing
- [ ] Market overview
- [ ] Liquidity signals
- [ ] Pricing engine
- [ ] SDG and biodiversity overlays
- [ ] Explainable premium or discount model

### Phase 5 — Portfolio and Executive Monitoring

Goal: surface risk, concentration, and change over time across holdings.

Tasks:
- [ ] Portfolio construction and watchlist rules
- [ ] Portfolio-level risk rollups
- [ ] Concentration and diversification logic
- [ ] Alerting and notification flows
- [ ] Executive summary views for low-frequency mobile usage

## UX and Design Backlog

### Desktop Wireframes To Keep
- [x] Dashboard overview
- [x] Data ingestion
- [x] Map analysis
- [x] AI extraction review
- [x] Market view
- [x] User settings
- [x] Registry ingestion health
- [x] AI interpretation results
- [x] Integrity detection
- [x] Risk scoring
- [x] Liquidity signals
- [x] Due diligence summary
- [x] Predictive failure
- [x] Pricing engine
- [x] Portfolio monitoring

### Missing Desktop Wireframes To Add
- [ ] Invite and accept invite flow
- [ ] Passkey or FIDO sign-in screen
- [ ] First-run onboarding flow
- [ ] Claims and workspace access management screen
- [ ] Claim request and approval flow
- [ ] Audit trail for authentication and authorization

### Mobile Wireframes To Add
- [ ] Mobile dashboard summary
- [ ] Mobile alerts and review inbox
- [ ] Mobile project detail snapshot
- [ ] Mobile due diligence summary
- [ ] Mobile onboarding and passkey login

## Suggested Claim Catalog For Discovery

These are starting points, not final names:

- claim.ingestion.view
- claim.ingestion.manage
- claim.documents.review
- claim.ai.validate
- claim.integrity.review
- claim.scoring.view
- claim.market.view
- claim.trading.execute
- claim.trading.approve
- claim.portfolio.view
- claim.portfolio.manage
- claim.workspace.invite
- claim.workspace.claims.manage
- claim.audit.view
- claim.admin.platform

## Suggested Handoff Deliverables

The next team should aim to produce these artifacts before heavy implementation starts:

- one architecture decision record for persistence topology
- one access control decision record for claims and workspace membership
- one onboarding journey map
- one passwordless authentication flow specification
- one mobile scope note
- one phased delivery plan mapping discovery to MVP and later phases

## Immediate Next Slice

If the next team wants the cleanest starting point, do these first:

1. Finalize the claims model.
2. Finalize the passkey or FIDO onboarding and recovery flow.
3. Decide hybrid persistence versus graph-first.
4. Add the missing onboarding and access-management wireframes.
5. Add a separate mobile wireframe source and mobile screenshots.
