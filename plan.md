# User Management & Authentication

## 1. User Registration & Login

- Users can register with name, email, and FIDO2/WebAuthn security key (up to 5 keys per user)
- Login via email + FIDO key (WebAuthn prompt)
- Users can add/remove keys in their profile (max 5)
- Show list of registered keys, allow setting default, and removing keys
- Error if user tries to add more than 5 keys

## 2. User Profile/Settings

- View/update profile info
- Manage FIDO keys (add, remove, set default)
- View assigned rights/roles
- Request additional rights (see below)

## 3. Admin User Management

- List/search users
- View user details (profile, registered keys, assigned rights)
- Assign or revoke rights/roles per user
- Disable/delete users
- See pending rights requests from users

## 4. Rights & Permissions System

- Define rights/roles (e.g. Viewer, Editor, Admin, Data Ingest, Integrity Reviewer, etc.)
- Admin can assign one or more rights to each user
- Users see their rights in profile
- Users can request additional rights (with reason)
- Admin sees and approves/denies requests
- UI: Rights matrix (users x rights), checkboxes for assignment
- Audit log for rights changes

## 5. UX/UI Notes

- Clear “Add Security Key” and “Remove” buttons
- Rights shown as badges or in a table
- Request rights: button opens dialog to select right and enter reason
- Admin: rights assignment via matrix or per-user detail page
- All actions accessible and WCAG AA compliant

---
**FIDO2/WebAuthn**: Use browser-native WebAuthn APIs for registration and authentication. Store public keys per user, max 5. Show friendly error messages for unsupported browsers or device issues.
# Platform Plan: Universal Carbon Intelligence

## Agent Roles Needed

1. **Registry Ingestion Agent**
   - Scrapes/ingests data from all major carbon registries, public documents, GIS, satellite, and transaction logs.
2. **Document Extraction Agent**
   - Extracts and parses data from PDFs, monitoring reports, verification docs, and project design documents.
3. **Geospatial Analysis Agent**
   - Detects land/parcel overlaps, polygon similarities, and conflicting claims using GIS and satellite data.
4. **Integrity Detection Agent**
   - Flags double counting, dormant projects, delayed monitoring, unrealistic claims, and inventory anomalies.
5. **AI Interpretation Agent**
   - Reads and standardizes project data, generates risk flags, project narratives, and comparable metrics.
6. **Risk Scoring Agent**
   - Assigns transparency, permanence, delivery, monitoring, financial, and registry consistency scores.
7. **Market Analytics Agent**
   - Tracks liquidity, pricing, sales activity, and generates market alerts and signals.
8. **Automated Due Diligence Agent**
   - Produces summaries, missing data alerts, and auditor flag predictions.
9. **Predictive Failure Agent**
   - Predicts project collapse, fire/drought/political risks, and underdelivery.
10. **User/Project Onboarding Agent**
    - Manages registry account linking, inventory exposure, and dynamic listing.

## Phased Plan

### Phase 1: Foundation
- Build Registry Ingestion Agent for major registries and public data
- Develop Document Extraction Agent for PDFs and reports
- Set up Geospatial Analysis Agent for overlap detection

### Phase 2: Intelligence Layer
- Implement AI Interpretation Agent for standardization and risk flagging
- Add Integrity Detection Agent for anomaly and risk detection
- Integrate Risk Scoring Agent for project ratings

### Phase 3: Market & User Layer
- Launch Market Analytics Agent for liquidity and pricing
- Enable User/Project Onboarding Agent for registry linking and listings
- Deploy Automated Due Diligence and Predictive Failure Agents

### Phase 4: Business Model & Expansion
- Integrate subscription, listing, and transaction fee models
- Expand to smallholder/agroforestry focus and advanced analytics

---
This plan matches the proposal and identifies the agent types needed for each layer. Each phase builds on the previous, ensuring a scalable and modular platform.