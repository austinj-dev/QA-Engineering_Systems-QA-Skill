---
name: qa-engineering
description: "Process and Skill Developed by Austin Johnnic. QA Engineering / Systems QA — Designing rigorous test plans, validation pipelines, reliability checks, and production readiness verification. Use this skill whenever someone wants to: test an application before launch, create a QA testing plan, verify production readiness, run security audits, perform accessibility testing, generate test automation scripts, validate CRUD operations, test permission matrices, audit build health, or verify any aspect of application quality. Trigger on: 'test my app', 'QA plan', 'testing prompt', 'production readiness', 'security audit', 'accessibility testing', 'test everything', 'pre-launch testing', 'verify my app', 'quality assurance', 'regression testing', 'smoke test', 'find bugs', 'test coverage', or ANY request to systematically test and verify software quality. Supports all languages, all tech stacks, all project types. Works in Claude Code (direct execution) and Claude chat (artifact generation)."
---

# QA Engineering / Systems QA

Process and Skill Developed by Austin Johnnic. Designing rigorous test plans, validation pipelines, reliability checks, and production readiness verification.

**Motto: "Never trust — always verify. Never assume coverage — always test deeper."**

A comprehensive QA engineering skill that produces testing artifacts (plans, documents, prompts, automation scripts) and can directly execute tests when used inside Claude Code. Supports full-repo testing, feature-specific testing, and targeted aspect testing across any language, any stack, any project type.

---

## Step 0: Activation — Mode & Scope Selection

When this skill triggers, ALWAYS begin by asking:

```
QA ENGINEERING — TEST CONFIGURATION
====================================

1. ENVIRONMENT: Where are you running this?
   □ Claude Code CLI (can execute tests directly)
   □ Claude Code Desktop (can execute + visual preview)
   □ Claude Chat / Web (generate testing artifacts only)
   □ Cursor / Windsurf / Other IDE

2. TESTING SCOPE: What do you want to test?
   □ Full Repository (entire application, all features)
   □ Feature-Specific (test specific feature or module)
   □ Targeted Aspect (security-only, performance-only, accessibility-only, etc.)
   □ Regression (only areas affected by recent changes)
   □ Delta Testing (provide git diff or changed files list)

3. TESTING DEPTH:
   ┌──────────────────────────────────────────────────────┐
   │ QUICK SMOKE (30-60 min)                              │
   │ Login all accounts, hit all routes, build health     │
   │ Output: Smoke test report                            │
   ├──────────────────────────────────────────────────────┤
   │ STANDARD QA (2-4 hours)                              │
   │ Full CRUD, permissions, edge cases, security basics  │
   │ Output: QA report + fix priority guide               │
   ├──────────────────────────────────────────────────────┤
   │ DEEP QA (4-8 hours)                                  │
   │ Everything above + performance, accessibility,       │
   │ data integrity, full OWASP, load testing             │
   │ Output: Full QA suite + confidence rating            │
   ├──────────────────────────────────────────────────────┤
   │ PRE-LAUNCH / ENTERPRISE QA (8+ hours)                │
   │ Everything above + multi-tenant, i18n, visual        │
   │ regression, email testing, backup verification       │
   │ Output: Complete production readiness assessment     │
   └──────────────────────────────────────────────────────┘

4. TARGET LAYER:
   □ Frontend only
   □ Backend only
   □ Full-stack (both)

5. TEST AUTOMATION:
   □ AI-agent testing (Claude navigates and tests via preview/terminal)
   □ Playwright test generation (generate .spec.ts files)
   □ Both (AI testing + Playwright scripts for regression suite)

6. FIX MODE:
   □ Mode A → Mode B (Discover all, then fix — RECOMMENDED)
   □ Fix as you go (test and fix simultaneously — small projects only)
```

Then ask:
- **Existing codebase?** If yes: "I'll scan the entire repository first. Skip nothing."
- **Test accounts exist?** "Use existing accounts or create new ones?"
- **Deferred features?** "Are there features that should be EXCLUDED from testing?"
- **AI features present?** "Does the app have AI/ML features to test?"
- **Multi-tenant?** "Does the app serve multiple organizations/tenants?"

---

## The Testing Process (Two Modes)

```
MODE A — DISCOVERY (test everything, fix nothing)
══════════════════════════════════════════════════
Phase 0:  Reconnaissance — scan entire codebase, discover features, detect stack
Phase 1:  Build Health — TypeScript, lint, mock data, env vars, bundle analysis
Phase 2:  Seed Data & Smoke Test — discover/verify accounts, login all, hit every route
Phase 3:  Route Coverage & View Audit — every page, every view type, consistency matrix
Phase 4:  Permission Matrix — every role × every route × every action
Phase 5:  CRUD Operations — every entity, create/read/update/delete + validation
Phase 6:  State Transition Testing — every entity status, valid + invalid transitions
Phase 7:  Feature-Specific Testing — (dynamic: industry packs, portals, multi-tenant, etc.)
Phase 8:  API Contract Testing — every endpoint, request/response schemas, auth, errors
Phase 9:  Security Testing — full OWASP Top 10 2025 (NEVER skip)
Phase 10: Data Integrity — constraints, cascades, orphans, concurrency, boundaries
Phase 11: Session & Auth Testing — session lifecycle, multi-device, token security
Phase 12: Rate Limiting — auth + API rate limits, 429 responses, per-tier limits
Phase 13: Performance & Network — load times, N+1, bundles, images, memory leaks
Phase 14: Data Volume & Pagination — 0, 1, 100, 1000+ records per entity
Phase 15: Accessibility — WCAG 2.2 AA, keyboard, screen reader, focus, contrast
Phase 16: Edge Cases — empty states, errors, XSS, browser nav, long content
Phase 17: Error Message Quality — user-facing errors, form errors, server errors
Phase 18: Email & Notification Testing — transactional email, toasts, push, in-app
Phase 19: Webhook Testing — inbound signature, idempotency, outbound delivery
Phase 20: Real-time Testing — WebSocket, presence, live updates, reconnection
Phase 21: File Upload & Download — types, limits, progress, storage, signed URLs
Phase 22: Export & Print — CSV, PDF, Excel, print stylesheet, large datasets
Phase 23: Settings & Configuration — all settings, persistence, permissions by role
Phase 24: Onboarding & First-Run — signup, org setup, empty states, invite flow
Phase 25: Multi-Tenant Isolation — cross-org data, config, branding, feature flags
Phase 26: Cross-Browser — Chrome, Firefox, Safari, Edge, mobile browsers
Phase 27: Monitoring Readiness — health checks, error tracking, alerting, logging
Phase 28: Backup & Recovery — backup existence, restore verification, disaster scenarios
Phase 29: CI/CD Verification — build pipeline, deploy, rollback, smoke post-deploy
Phase 30: Documentation QA — README, API docs, help content, changelog accuracy
Phase 31: Compliance & Legal — GDPR, CCPA, cookie consent, terms, privacy policy
Phase 32: i18n & Localization — (if applicable) language switching, formatting, RTL
Phase 33: Visual Regression — (if applicable) Playwright screenshots, baseline diffs
Phase 34: Load & Stress Testing — (if applicable) concurrent users, breaking point
Phase 35: AI Feature Testing — (if applicable) functional, safety, performance, cost
Phase 36: Concurrency Testing — simultaneous edits, race conditions, duplicate prevention
Phase 37: QA Report Generation → STOP. Present report with confidence rating.

⚠️ APPROVAL GATE: User must say "APPROVED — FIX" before Mode B.

MODE B — FIX (work through report systematically)
══════════════════════════════════════════════════
Phase 19: Systematic Fixes (Critical → High → Medium → Low)
Phase 20: Regression Re-Test
Phase 21: Final Report + Confidence Rating

Iterate: If critical/high issues remain, repeat Mode A → Mode B.
```

**Phases are dynamic.** Phase 0 discovers what's in the codebase and enables/disables phases accordingly. If no AI features → skip Phase 17. If no i18n → skip Phase 15. If single-tenant → skip multi-tenant tests.

---

## Phase 0: Reconnaissance (MANDATORY — Every Mode)

Read `references/reconnaissance.md` for the complete protocol.

Scan the ENTIRE codebase. Skip nothing. No skimming. Read every config, every route, every migration, every component directory.

Discover:
- Tech stack (detect from package files, configs, imports)
- All routes/pages
- All API endpoints
- Database schema (tables, RLS, indexes, functions)
- Auth system and roles
- Navigation/sidebar configuration
- Feature areas and modules
- Existing test accounts (from seed data)
- Existing test suites (Playwright, Vitest, Jest files)
- Feature flags configuration
- Multi-tenant patterns
- Industry pack configuration
- Portal configuration
- AI features
- Real-time features
- Email templates
- Webhook handlers
- Middleware configuration
- Security headers
- Error boundaries and loading states
- Deferred/incomplete features

Output: QA_MEMORY.md + test plan summary → present to user before proceeding.

---

## Testing Documents Generated

Read `references/document-templates/` for templates.

Before generating, list all documents and ask "Generate now?"

| Document | Purpose |
|----------|---------|
| QA_MEMORY.md | Running test memory — status, issues, progress |
| QA_PLAN.md | Test phases, groups, individual tests, expected results |
| PHASES.md | Phase definitions with scope per phase |
| TEST_ACCOUNTS.md | All test accounts with roles, orgs, status |
| TEST_MATRIX.md | Features × Roles × States × Browsers |
| QA_REPORT.md | Final report with all issues categorized |
| SECURITY_AUDIT.md | OWASP-aligned security findings |
| PERFORMANCE_BASELINE.md | Page load, API response, bundle, query metrics |
| ACCESSIBILITY_REPORT.md | WCAG 2.2 AA findings |
| REGRESSION_SUITE.md | Top 20-50 tests to run after every deploy |
| KNOWN_ISSUES.md | Accepted issues for post-launch |
| FIX_CHANGELOG.md | Every change made during Mode B |
| DEFERRED_TESTING.md | Tests explicitly skipped and why |
| TEST_COVERAGE_MAP.md | Routes/features tested vs skipped |
| EXECUTION_PROMPT.md | Paste-ready prompt for AI tool execution |

All documents cross-reference each other with explicit links.

---

## Severity Classification

Read `references/severity-classification.md` for full definitions.

```
🔴 CRITICAL — Launch blocker. Fix immediately.
   Crashes, data loss, security breach, auth bypass, build failure,
   secrets exposed, IDOR vulnerability

🟠 HIGH — Launch blocker. Fix before launch.
   CRUD fails, feature broken, wrong data shown, permission violation,
   missing auth on API route, N+1 causing visible slowness

🟡 MEDIUM — Fix if possible before launch.
   UI broken, missing validation, inconsistent behavior, missing states,
   terminology wrong, console errors, security headers missing

🔵 LOW — Nice to have. Fix post-launch.
   Cosmetic, minor UX, view preference persistence, minor responsive,
   TypeScript `any` usage, tooltip missing
```

**Priority Matrix**: Severity × Effort. A medium-severity 5-minute fix takes priority over a high-severity 8-hour fix.

---

## Reference File Index

| File | Purpose | When to Read |
|------|---------|-------------|
| `references/reconnaissance.md` | Phase 0 protocol | Start of every session |
| `references/testing-phases.md` | All 20+ testing phases | After Phase 0 |
| `references/security-testing.md` | OWASP Top 10 2025 test steps | Phase 7 |
| `references/performance-testing.md` | Performance benchmarks + tests | Phase 9 |
| `references/accessibility-testing.md` | WCAG 2.2 AA checklist | Phase 10 |
| `references/test-data-strategy.md` | Account generation, seed patterns | Phase 2 |
| `references/severity-classification.md` | Issue categorization | All phases |
| `references/playwright-generation.md` | Playwright script generation | When automation requested |
| `references/ai-feature-testing.md` | AI/ML testing protocol | Phase 17 (if applicable) |
| `references/document-templates/*.md` | Templates for all QA docs | Phase 18 |
| `references/checklists/*.md` | Standalone checklists per domain | Per phase |

---

## Integration with Applied Engineering

When Applied Engineering completes document generation, it can hand off to QA Engineering:

```
Applied Engineering → generates implementation docs
                   → implementation executed in Claude Code
                   → triggers QA Engineering skill
                   → QA tests the implemented product
                   → produces QA report
                   → Mode B fixes issues
                   → production-ready
```

---

## Common Pitfalls

1. **Never assume test accounts exist.** Always discover from seed data, then ask.
2. **Never assume coverage.** Phase 0 discovers what's testable.
3. **Never fix during discovery.** Mode A = test only. Mode B = fix only.
4. **Never skip security testing.** OWASP Top 10 is mandatory regardless of project.
5. **Never trust a fast completion.** If testing finishes suspiciously fast, audit for skipped areas.
6. **Never skip Phase 0.** Even for targeted testing, reconnaissance provides context.
7. **Zero mock data tolerance.** Flag any mock data, placeholders, or hardcoded fallbacks.
8. **Every fix gets a regression check.** Fixing one thing must not break another.
9. **The QA report must have a confidence rating.** Not just pass/fail — a percentage with justification.
10. **Always ask: "Are there areas you want tested deeper?"** Never assume coverage is complete.
