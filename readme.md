# Project Filip

Welkom bij het project! Dit document begeleidt je bij het opzetten, ontwikkelen en begrijpen van deze applicatie.

## Inhoud
- [Beschrijving](#beschrijving)
- [Technische Stack](#technische-stack)
- [Features](#features)
- [Backlog](#backlog)
- [Installatie & Ontwikkeling](#installatie--ontwikkeling)
- [Hosting](#hosting)
- [Toegankelijkheid](#toegankelijkheid)
- [Contact](#contact)

---

## Beschrijving
Een moderne webapplicatie voor rechtenbeheer met FIDO2/WebAuthn authenticatie, rechtenmatrix, audit trail en toegankelijke UX. Gebouwd met Vue 3, Vite, Tailwind CSS + daisyUI, Node.js backend en Neo4j database.

## Technische Stack
- **Frontend:** Vue 3 + Pinia, Vite, Tailwind CSS, daisyUI
- **Backend:** Node.js (Express/NestJS)
- **Database:** Neo4j (Aura Free)
- **Hosting:** Vercel/Netlify (frontend), Cyclic/Render/Railway (backend)

## Features
- FIDO2/WebAuthn login & registratie
- Rechten aanvragen en beheren
- Admin goedkeuring/afwijzing
- Audit trail van rechtenwijzigingen
- Toegankelijk (WCAG 2.1 AA)

## Backlog
Zie [backlog.md](backlog.md) voor alle user stories en taken.

## Installatie & Ontwikkeling
1. **Clone deze repo**
2. **Frontend installeren & starten:**
   ```bash
   cd frontend
   npm install
   npm run dev
   ```
3. **Backend installeren & starten:**
   ```bash
   cd backend
   npm install
   npm run dev
   ```
4. **Neo4j database:**
   - Maak een gratis AuraDB instance aan: https://neo4j.com/cloud/aura/
   - Zet connectiegegevens in een `.env` file in backend

## Hosting
- **Frontend:** Vercel of Netlify (gratis tier)
- **Backend:** Cyclic, Render of Railway (gratis tier, let op limieten)
- **Database:** Neo4j Aura Free (limiet: 200k nodes/relaties)

## Toegankelijkheid
- Keyboard navigatie en screen reader ondersteuning
- Automatische accessibility tests aanbevolen

## Contact
Voor vragen of bijdragen: open een issue of neem contact op met de projectbeheerder.
