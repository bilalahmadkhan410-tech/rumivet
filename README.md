# RumiVet AI — Functional Offline Android Prototype v1.0

This version is a functional offline Android application rather than the previous UI-only prototype.

## Working features
- Clinical case entry with rule-based ruminant differential suggestions
- Emergency red-flag detection
- Laboratory interpretation for selected common analytes with clearly marked example/reference guidance
- Weight × dose/kg ÷ concentration dose-volume calculator
- Local animal registry saved on the device
- Local saved clinical cases
- Emergency guide
- Drug safety checklist that deliberately refuses to invent drug doses/withdrawal periods
- No internet or account required for the core prototype

## Important clinical limitation
This is clinical decision support, not a validated diagnostic or prescribing system. Reference ranges, drug monographs, withdrawal periods, treatment protocols, and disease rules must be reviewed against authoritative veterinary sources and local regulations before clinical deployment.

## Build
Open this folder in Android Studio and let it use Gradle/Android SDK. Then Build > Build APK(s). The debug APK will be under app/build/outputs/apk/debug/.

## Next production layer
A production release should add a validated ruminant disease/drug/lab database, citations, veterinarian confirmation workflow, encrypted database, authentication/RBAC, audit trail, cloud sync, offline conflict handling, and optional AI API integration.

## Build online for free with GitHub Actions

This package includes a GitHub Actions workflow at `.github/workflows/build-apk.yml`. Upload the project contents to a GitHub repository, open **Actions**, choose **Build RumiVet AI APK**, and run it. The finished `app-debug.apk` is uploaded as a workflow artifact.

See `GITHUB_BUILD.md` for step-by-step instructions.
