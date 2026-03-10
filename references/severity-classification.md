# Severity Classification — QA Engineering

## 🔴 CRITICAL — Launch Blocker
App crashes, data loss, security breach, auth bypass, build failure, secrets exposed, IDOR vulnerability, SQL injection, XSS executing, login failure, DB constraint violations causing data corruption.

## 🟠 HIGH — Launch Blocker
CRUD fails, feature broken entirely, wrong data displayed, permission violation (wrong role can do/see wrong thing), missing auth on API route, N+1 query causing visible slowness, data isolation failure between tenants.

## 🟡 MEDIUM — Fix Before Launch If Possible
UI layout broken, missing validation, view type broken, terminology wrong, missing empty/loading/error states, inconsistent behavior between modules, console errors (non-fatal), security headers missing, excessive bundle size, console.log left in production code.

## 🔵 LOW — Post-Launch
Cosmetic issues, minor UX, view preference persistence, minor responsive issues, tooltip missing, TypeScript `any` usage, minor accessibility issues that don't block usage.

## Priority Matrix
| | Low Effort | Medium Effort | High Effort |
|---|-----------|--------------|------------|
| 🔴 Critical | FIX NOW | FIX NOW | FIX NOW |
| 🟠 High | FIX NOW | FIX BEFORE LAUNCH | FIX BEFORE LAUNCH |
| 🟡 Medium | FIX QUICK | PLAN FOR LAUNCH | DEFER IF NEEDED |
| 🔵 Low | QUICK WIN | BACKLOG | BACKLOG |
