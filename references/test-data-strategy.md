# Test Data Strategy — QA Engineering

## Account Discovery (Always First)
1. Scan seed.sql / seed files for existing accounts
2. Present found accounts to user
3. Ask: "Use these accounts? Or create new ones?"
4. NEVER create accounts without asking

## Account Pattern (when creating)
```
Per role: [role]-test@domain.com
Per org:  [org-slug]-[role]@domain.com
Per feature: [feature]-[role]@domain.com
Password: TestPassword123! (or project-specific)
```

## Seed Data Requirements
- 5-10 records per major entity per org
- Edge case data: empty strings, max-length, special chars, unicode
- Relationship data: parent-child records for cascade testing
- Multi-state data: records in every status (draft, active, completed, archived)
- Date data: past, present, future dates
- Numeric data: zero, negative, max values

## Test Data Isolation
- Each test org has isolated data
- No cross-org data leakage
- Cleanup strategy after testing (or use disposable orgs)
