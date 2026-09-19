# Security & Privacy Requirements

1. TLS for all network traffic.
2. Secure password hashing; optional MFA/passkeys.
3. Backend authorization on every sensitive request.
4. Least-privilege RBAC: veterinarian, student, farm owner, administrator, technician, laboratory user, system administrator.
5. Organization/farm/animal/case-level access controls.
6. Encrypted local database and encrypted backups/sync.
7. Audit login, case access/edit, lab entry, treatment, exports and permission changes.
8. Finalized records read-only; corrections require amendments with reason and actor.
9. Controlled exports and revocable/expiring share links.
10. Data minimization and purpose limitation.
11. Do not send private clinical records to external AI by default.
12. Provide privacy policy, retention/deletion rules, consent where required, and clinical disclaimer.
