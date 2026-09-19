# RumiVet AI — Suggested Production Data Model

Core tables/entities:
- users(id, organization_id, role, status, auth_provider, created_at)
- organizations(id, name, country, created_at)
- farms(id, organization_id, name, location_text)
- animals(id, farm_id, tag, species, breed, sex, birth_date, status)
- cases(id, animal_id, clinician_id, status, opened_at, finalized_at)
- observations(id, case_id, type, value, unit, observed_at)
- diagnoses(id, case_id, diagnosis, certainty_type, source, confirmed_by)
- lab_results(id, case_id, analyte, value, unit, reference_low, reference_high, lab_source)
- treatments(id, case_id, drug_id, product_name, concentration, dose, dose_unit, route, frequency, duration, prescriber_id)
- drugs(id, generic_name, class, species, indication, source, country)
- withdrawal_rules(id, drug_id, product_id, species, milk_hours, meat_hours, jurisdiction, source, effective_date)
- protocols(id, condition, species, priority, diagnostics, stabilization, treatment_principles, monitoring, source)
- audit_events(id, actor_id, entity_type, entity_id, action, before_json, after_json, timestamp)

Use UUIDs, UTC timestamps, soft archive where legally appropriate, and append-only audit events.
