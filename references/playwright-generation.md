# Playwright Test Generation — QA Engineering

## When to Generate
When user selects "Playwright test generation" or "Both" in activation.

## What to Generate
- Smoke test suite: login all accounts, hit critical routes
- CRUD test suite: create/read/update/delete per entity
- Permission test suite: verify role-based access
- Security test suite: IDOR, XSS, injection checks
- Regression suite: top 20-50 critical paths

## Structure
```
tests/
├── smoke/
│   └── login.spec.ts
├── crud/
│   ├── [module].crud.spec.ts
├── permissions/
│   └── role-access.spec.ts
├── security/
│   └── owasp-checks.spec.ts
├── regression/
│   └── critical-paths.spec.ts
└── fixtures/
    ├── auth.ts
    └── test-data.ts
```

## Best Practices
- Use user-facing locators (role, text, label) not CSS/XPath
- Each test fully isolated (fresh context)
- Use fixtures for auth state reuse
- Parallel execution with isolated data
- Screenshots on failure
- Traces on first retry
