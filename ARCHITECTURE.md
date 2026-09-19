# RumiVet AI — Production Architecture

## Mobile modules
- Clinical case intake and differential engine
- Disease knowledge browser
- Laboratory interpretation
- Treatment protocols
- Drug/product safety database
- Dose/volume calculator
- Animal registry and case history
- Emergency guide
- Follow-up/recheck workflow

## Production backend
Mobile/Web -> Auth -> API Gateway -> Authorization/RBAC -> Clinical Service / Lab Service / Drug Service / AI Service / Audit Service -> PostgreSQL + encrypted object storage.

## AI layer
Use an evidence-grounded retrieval layer. AI output must be labelled `AI_SUGGESTION`; veterinarian-confirmed diagnosis and lab-confirmed findings are separate immutable fields. Do not train external models on private clinical cases by default.

## Offline sync
Encrypted local database -> queued changes -> authenticated sync -> server conflict resolution. Finalized clinical records are append-only with amendments.
