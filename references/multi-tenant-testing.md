# Multi-Tenant Isolation Testing — QA Engineering

## Data Isolation
- [ ] Tenant A cannot see Tenant B data via UI
- [ ] Tenant A cannot see Tenant B data via API (change org_id in request)
- [ ] Tenant A cannot see Tenant B data via direct URL manipulation
- [ ] RLS policies enforce isolation at database level
- [ ] Switching orgs shows only that org's data
- [ ] Search results scoped to current org only
- [ ] File/media access scoped to current org
- [ ] Export only includes current org data

## Configuration Isolation
- [ ] Org-specific settings don't leak between tenants
- [ ] Org-specific branding doesn't leak
- [ ] Org-specific feature flags isolated
- [ ] Industry pack configuration isolated per org

## Lifecycle
- [ ] New org gets clean default state
- [ ] Org deletion cascades correctly
- [ ] User multi-org membership works correctly
- [ ] Role scoping per org works