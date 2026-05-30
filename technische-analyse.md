# Technische Analyse

## Architectuur & Componenten

- **Frontend**: Moderne SPA (Single Page Application) met component-based UI (bijv. React, Vue, of Svelte)
- **Backend**: Protobuf/gRPC API, met authenticatie endpoints (FIDO2/WebAuthn integratie)
- **Database**: Relationeel (PostgreSQL/MySQL) of document-based (MongoDB) afhankelijk van datamodel
- **User Management**: Eigen user store met FIDO2 key registratie, rechtenmatrix, en audit logging
- **Admin Panel**: Beheer van gebruikers, rechten, en verzoeken via een beveiligde admin interface
- **Security**: WebAuthn/FIDO2, HTTPS, RBAC (Role-Based Access Control), audit logs
- **Accessibility**: WCAG 2.1 AA, keyboard navigation, screen reader support

## Technologie Overwegingen

- **Frontend**:
    - **Vue 3 + Pinia** (https://pinia.vuejs.org/) als voorkeursstack.
    - **Vite** als bundler/build tool (snel, moderne DX, top integratie met Vue/Tailwind).
    - **Tailwind CSS** (https://tailwindcss.com/) als CSS framework, uitgebreid met **daisyUI** (https://daisyui.com/) voor kant-en-klare, aanpasbare componenten.

- **Backend**:
    - **Node.js** (Express/NestJS) als backend-platform.
    - Database: **Neo4j** (graph database, ideaal voor relaties en rechtenstructuren).
    - Alternatief: REST, GraphQL of gRPC API mogelijk.

- **Hosting/Infra**:
    - Voorlopig: gratis hosting vereist (bijv. Vercel, Netlify voor frontend; Cyclic, Render, Railway voor Node.js backend; Neo4j Aura Free voor database).
    - Let op limieten van gratis hosting (slaapstand, cold starts, beperkte resources).
- **Backend**:
    - Node.js (Express/NestJS) of Laravel (PHP) voor snelle API ontwikkeling
    - Alternatief: Python (FastAPI) of .NET Core voor grotere teams/enterprise
    - Protobuf/gRPC API: Overweeg Protobuf/gRPC als alternatief voor REST/GraphQL voor efficiënte, strongly-typed communicatie tussen services (vooral bij microservices of polyglot stacks). Voordelen: snellere serialisatie, contract-first, multi-language support. Nadeel: minder geschikt voor directe browser-consumptie zonder extra tooling (gRPC-web of REST gateway nodig).
- **Database**:
    - PostgreSQL voor relationele data en sterke integriteit
    - MongoDB voor flexibele document storage (bijv. rechtenmatrix als embedded docs)
- **Authentication**:
    - WebAuthn/FIDO2 via open source libraries (bijv. @simplewebauthn, webauthn.io)
- **Hosting/Infra**:
    - Cloud-native (Azure, AWS, Vercel) met CI/CD pipelines
- **Testing**:
    - Cypress/Playwright voor end-to-end tests, Jest/Vitest voor unit tests

## Vragen & Flow Issues

1. **User Flow**
    - Hoe verloopt de fallback als FIDO key niet werkt of verloren is?
    - Kunnen gebruikers meerdere rechten tegelijk aanvragen? ja. het zulle ntoegangen tot scremen zijn
    - Wat gebeurt er als een admin een recht weigert? Krijgt de gebruiker feedback? lijkt me ene goed idee
    - Is er een onboarding flow voor nieuwe gebruikers na registratie?
    - Hoe worden rechtenwijzigingen geaudit en getoond aan admins?
2. **Technologie**
    - Gaan we voor een monorepo (frontend+backend samen) of gescheiden repos? voorlopig mono
    - Welke WebAuthn library is het meest geschikt voor onze stack? die van bitwarden
    - Welke database past het beste bij het rechtenmodel? 
3. **Security & Privacy**
    - Hoe lang bewaren we audit logs en gebruikersdata? 
    - Hoe gaan we om met GDPR/AVG compliance? pii gevoelig inso word met een key op het user profiel beweaard
    - Is er een recovery flow voor verloren FIDO keys?

## Aanbevelingen

- Start met React (Next.js) + Node.js (Express/NestJS) + PostgreSQL voor maximale flexibiliteit en community support
- Gebruik @simplewebauthn voor FIDO2 integratie
- Bouw een eigen rechtenmatrix met audit logging
- Implementeer CI/CD en automatische accessibility testing vanaf het begin ! pervekt werk maar test driven en laat de testen door een andere afent schrijven
- Documenteer alle flows en edge cases in wireframes en user stories
