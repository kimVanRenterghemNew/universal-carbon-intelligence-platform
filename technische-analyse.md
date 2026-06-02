# Technische Analyse

## Doel van de architectuur

De platformarchitectuur moet vier dingen tegelijk goed doen:

- grote hoeveelheden heterogene carbon data binnenhalen
- ongestructureerde documenten omzetten naar bruikbare datasets
- integriteitsrisico's uitlegbaar detecteren
- inzichten snel en toegankelijk presenteren aan analisten en operators

## Voorgestelde architectuur

### Frontend
- Moderne SPA of hybride webapp voor dashboards, projectdetail, kaarten en reviewflows
- Goede keuze: React met Next.js of Vue 3 met Vite
- UI-laag met Tailwind CSS + daisyUI component patterns, duidelijke statusweergave en responsieve layouts

### Backend en services
- API-laag voor gebruikers, projecten, flags, scores en exports
- Identity- en accesslaag voor onboarding, FIDO of passkey login, sessies en claims-evaluatie
- Asynchrone workers voor ingestie, OCR, extractie, scoring en notificaties
- Eventgedreven koppeling tussen pipelines zodat nieuwe data automatisch vervolgstappen triggert

### Datalaag
- Document store voor projectdossiers, extractieresultaten, bronpayloads en analyst notes
- Graph store als sterke kandidaat voor tradingrelaties, ownership chains, counterparty links en exposure-analyse
- Beperkte operationele kern voor jobs, audit trails, notificaties en workflowstatus
- Object storage voor documenten, exports en bronbestanden
- Geospatiale opslag via PostGIS voor polygonen, overlaps en kaartqueries
- Zoek- of indexlaag voor full-text document retrieval en snelle filters

## Aanbevolen stack

### Applicatielaag
- Frontend: React + Next.js of Vue 3 + Vite, met Tailwind CSS en daisyUI voor de componentlaag
- Backend API: Node.js met NestJS of Python met FastAPI
- Background jobs: queue workers voor ingestie en AI-pijplijnen
- Authenticatie: FIDO of passkeys zonder traditioneel wachtwoordbeheer
- Autorisatie: claims-based access control in plaats van enkel coarse-grained roles

### Data en analyse
- Document store als primaire opslagkandidaat voor project- en extractiedossiers
- Graph database voor trading, ownership en relationship-heavy queries
- Kleine relationele of transactionele sidecar voor workflowconsistentie, auditability en reporting wanneer nodig
- PostGIS extensie voor geospatiale analyse
- S3-compatibele object storage voor documenten en snapshots
- Optionele zoeklaag zoals OpenSearch voor document- en projectfiltering

### AI en extractie
- OCR stap voor gescande documenten
- LLM-gebaseerde extractie per documenttype
- Strikte outputschema's zodat extracties valideerbaar en herhaalbaar blijven
- Feedbackloop voor menselijke correcties op high-impact velden

## Belangrijkste domeincomponenten

### 1. Registry Ingestion Engine
- Connector per registry of bron
- Normalisatielaag naar één intern projectmodel
- Sync-status, retries, rate limiting en foutregistratie

### 2. Document Extraction Pipeline
- Upload, classificatie, OCR, extractie, validatie en opslag
- Confidence score per veld
- Link tussen extracties en originele bronpassages

### 3. Geospatial Analysis Engine
- CRS-validatie en geometry cleanup
- Overlapdetectie, buffering, proximity checks en visualisatie-output
- Satelliet- of NDVI-koppeling per project of gebied

### 4. Integrity Detection Layer
- Regelgebaseerde flags voor monitoring delays, dormancy en issuance anomalies
- Later uitbreidbaar met ML of anomaliedetectie
- Altijd uitlegbaar: elke flag moet bewijs en brondata tonen

### 5. Scoring and Market Intelligence
- Herberekening van scores bij nieuwe data
- Opslag van scorehistorie voor trends
- Marktmodules voor prijs, volume, liquidity en comparables

## Architectuurprincipes

- Eerst een betrouwbare datafundering, daarna pas complexere AI-logica
- Explainability boven magische black-box output
- Idempotente pipelines zodat re-ingest veilig blijft
- Toegankelijkheid als standaard in plaats van laatste laag bovenop de UI
- Auditability voor datawijzigingen, overrides en modelcorrecties

## Open ontwerpkeuzes

1. Gaat de eerste versie multi-tenant zijn of starten we single-tenant?
2. Welke registries krijgen prioriteit in de MVP?
3. Hoeveel handmatige review is acceptabel bij documentextractie?
4. Is near-real-time marktdata nodig of volstaat batchverwerking?
5. Welke exports zijn commercieel het belangrijkst: PDF, CSV of API-first?
6. Gaan we hybrid document + graph werken of echt graph-first?
7. Welke claims zijn workspace-scoped en welke platform-breed?
8. Start onboarding invite-only of self-serve met approval?
9. Welke flows moeten echt mobile-first zijn in de MVP?

## Concrete aanbevelingen

- Gebruik een hybride richting als default: document-first voor dossiers en extracties, graph voor trading- en relatieanalyse, en een smalle operationele store waar transactiestabiliteit of rapportage dat vereist.
- Gebruik aparte async workers voor ingestie, OCR en scoring; houd de API request/response laag dun.
- Leg flags, scores en AI-extracties vast met herleidbare evidence references.
- Ontwerp de UI rond analistenflows en voeg expliciet onboarding, claimsbeheer en passwordless identity toe.
- Houd identity en permissions niet role-first maar claims-first, met audit log, recovery flow en workspace-context.