# Database Migration Testing — QA Engineering

## Migration Chain Verification
- [ ] Run all migrations from empty database → no errors
- [ ] Migration order has no FK violations
- [ ] Every CREATE TABLE has matching IF NOT EXISTS (or handled)
- [ ] No duplicate migration filenames/timestamps
- [ ] Types generate cleanly after all migrations
- [ ] Seed data runs without constraint violations after migrations

## Rollback Testing
- [ ] Each migration can be rolled back (if framework supports)
- [ ] Rollback + re-migrate produces same schema
- [ ] Data is preserved during safe migrations (additive only)

## Schema Verification
- [ ] All tables referenced in code exist in schema
- [ ] All columns referenced in code exist in tables
- [ ] Column types match code expectations
- [ ] Indexes exist on frequently queried columns
- [ ] Foreign keys reference existing tables
- [ ] RLS policies exist on every table with user data
- [ ] Functions and triggers exist and execute correctly

## Seed Data Verification
- [ ] Seed creates expected number of records
- [ ] Seed data respects all constraints (FK, UNIQUE, CHECK, NOT NULL)
- [ ] Seed is idempotent (running twice doesn't duplicate)
- [ ] Test accounts have correct roles and org assignments
- [ ] Industry/feature-specific seed data present
