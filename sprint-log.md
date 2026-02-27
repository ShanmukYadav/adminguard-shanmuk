# AdmitGuard Development Sprint Log

### Sprint 1: Foundation (Zero-Tolerance)
- **Goal**: Implement primary institutional blocks.
- **Outcome**: Created 11-field form with strict validation for Phone, Aadhaar, and Name.

### Sprint 2: Logic Layer (Soft Rules & Exceptions)
- **Goal**: Handle "borderline" candidates without manual bottlenecks.
- **Outcome**: Implemented warning triggers for Age/Scores and the keyword-validated rationale system.

### Sprint 3: Enterprise Polish (Config & Audit)
- **Goal**: Ensure institutional accountability.
- **Outcome**: Refactored logic into JSON config and added the persistent LocalStorage Audit Log.