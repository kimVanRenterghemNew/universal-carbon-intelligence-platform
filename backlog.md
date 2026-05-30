# Backlog

## Epic: Gebruikersbeheer & Authenticatie

### User Story 1: Als gebruiker wil ik kunnen registreren en inloggen met FIDO2/WebAuthn
- Task: Frontend registratie- en loginpagina (Vue + Pinia)
- Task: Backend endpoints voor registratie/login (Node.js)
- Task: Integratie WebAuthn/FIDO2 (frontend + backend)
- Task: Validatie en foutafhandeling flows
- Task: Testen met verschillende authenticators

### User Story 2: Als gebruiker wil ik mijn FIDO2 sleutel kunnen beheren (toevoegen/verwijderen)
- Task: UI voor sleutelbeheer
- Task: Backend API voor sleutelbeheer
- Task: Audit logging van sleutelwijzigingen

---

## Epic: Rechtenmatrix & Aanvragen

### User Story 3: Als gebruiker wil ik rechten kunnen aanvragen
- Task: UI voor rechtenaanvraag
- Task: Backend endpoint voor aanvraag indienen
- Task: Opslag aanvraag in Neo4j

### User Story 4: Als admin wil ik aanvragen kunnen goedkeuren of weigeren
- Task: Admin UI voor overzicht en acties
- Task: Backend endpoints voor goedkeuren/weigeren
- Task: Notificatie/feedback naar gebruiker

### User Story 5: Als admin wil ik een overzicht van alle rechtenwijzigingen (audit trail)
- Task: Audit logging implementeren
- Task: UI voor audit trail
- Task: Backend endpoint voor audit trail ophalen

---

## Epic: Toegankelijkheid & UX

### User Story 6: Als gebruiker wil ik dat de applicatie toegankelijk is (WCAG 2.1 AA)
- Task: Keyboard navigatie implementeren
- Task: Screen reader ondersteuning testen
- Task: Automatische accessibility tests (CI)

---

## Epic: Hosting & Deploy

### User Story 7: Als ontwikkelaar wil ik de app gratis kunnen hosten
- Task: Frontend deployen op Vercel/Netlify
- Task: Backend deployen op Cyclic/Render/Railway
- Task: Database opzetten op Neo4j Aura Free
- Task: Documentatie van deployment stappen
