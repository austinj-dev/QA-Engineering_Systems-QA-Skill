# Testing Phases — QA Engineering

## Dynamic Phase Selection

Phase 0 discovers what's in the codebase. Based on findings, phases are enabled or disabled:

| Phase | Always | Conditional On |
|-------|--------|---------------|
| 0 Reconnaissance | ✅ | — |
| 1 Build Health | ✅ | — |
| 2 Seed & Smoke | ✅ | — |
| 3 Route Coverage | ✅ | — |
| 4 Permission Matrix | ✅ | Roles exist |
| 5 CRUD Operations | ✅ | — |
| 6 Feature-Specific | ✅ | Features discovered |
| 7 Security (OWASP) | ✅ | — (NEVER skip) |
| 8 Data Integrity | ✅ | Database exists |
| 9 Performance | Standard+ | — |
| 10 Accessibility | Standard+ | Frontend exists |
| 11 Edge Cases | ✅ | — |
| 12 Cross-Cutting | Standard+ | Notifications/email/webhooks exist |
| 13 Settings | Standard+ | Settings pages exist |
| 14 Onboarding | Deep+ | Signup flow exists |
| 15 i18n | Deep+ | Multi-language detected |
| 16 Visual Regression | Deep+ | Playwright mode selected |
| 17 AI Features | Deep+ | AI features detected |
| 18 Report Generation | ✅ | — |

## Per-Phase Protocol

Every phase follows:
1. Read the phase description
2. Execute tests in order
3. Record every result in QA_MEMORY.md
4. DO NOT FIX issues (Mode A only)
5. Update QA_MEMORY.md issue counts
6. Verify phase GATE before proceeding

## Phase Recording Format

```
Phase [N]: [Name]
Started: [timestamp]
Account: [email]
Tests run: [count]
Issues found: [count] (🔴[n] 🟠[n] 🟡[n] 🔵[n])
Gate: ✅ PASSED / ❌ FAILED — [details]
```
