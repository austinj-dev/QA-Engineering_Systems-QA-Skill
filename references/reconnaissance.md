# Reconnaissance Protocol — QA Engineering

## MANDATORY for every testing mode. No exceptions.

Scan the ENTIRE codebase. Skip nothing. No skimming.

### Analysis Commands (adapt per stack)

```bash
# Project structure
find . -maxdepth 4 -type d | grep -v node_modules | sort

# All routes/pages
find . -name "page.tsx" -o -name "page.ts" -o -name "*.vue" -o -name "views.py" -o -name "*controller*" | sort

# All API routes
find . -path "*/api/*" -name "route.ts" -o -name "*.py" -o -name "*.rb" | sort

# Package/dependency files
cat package.json requirements.txt Cargo.toml go.mod Gemfile composer.json 2>/dev/null

# Database schema
find . -path "*/migrations/*" -type f | sort
grep -rh "CREATE TABLE" */migrations/ 2>/dev/null | wc -l
grep -rh "CREATE POLICY" */migrations/ 2>/dev/null | wc -l

# Auth system
grep -rl "auth\|session\|login\|permission\|role\|RBAC" src/ lib/ app/ 2>/dev/null | sort

# Navigation/sidebar
grep -rl "sidebar\|navigation\|navItems\|menuItems" src/ 2>/dev/null | sort

# Existing tests
find . -name "*.test.*" -o -name "*.spec.*" -o -name "*_test.*" | sort
find . -name "playwright.config.*" -o -name "vitest.config.*" -o -name "jest.config.*" 2>/dev/null

# Test accounts in seed
grep -i "@\|password\|user\|account\|seed" */seed* 2>/dev/null | head -40

# Middleware
cat src/middleware.ts middleware.ts middleware.py 2>/dev/null

# Security headers
grep -rl "Content-Security-Policy\|X-Frame-Options\|HSTS\|cors\|CORS" src/ 2>/dev/null

# Environment variables
grep -roh "process\.env\.[A-Z_]*\|import\.meta\.env\.[A-Z_]*\|os\.environ\[" src/ app/ lib/ 2>/dev/null | sort -u

# Feature flags
grep -rl "feature.flag\|featureFlag\|LaunchDarkly\|PostHog" src/ 2>/dev/null

# AI features
grep -rl "openai\|anthropic\|ai_\|gemini\|groq\|llm\|embedding\|vector" src/ app/ 2>/dev/null | sort

# Real-time
grep -rl "websocket\|realtime\|supabase.*realtime\|socket\.io\|pusher\|sse" src/ 2>/dev/null

# Email
grep -rl "resend\|sendgrid\|ses\|nodemailer\|email.*template" src/ 2>/dev/null

# Webhooks
grep -rl "webhook" src/ app/ 2>/dev/null

# Error handling
find . -name "error.tsx" -o -name "not-found.tsx" -o -name "loading.tsx" | sort

# Mock data audit
grep -rn "mock\|Mock\|placeholder\|lorem\|dummy\|TODO\|FIXME" src/ --include="*.ts" --include="*.tsx" --include="*.py" --include="*.rb" --include="*.go" | grep -v "node_modules\|test\|spec\|__mock__" | wc -l
```

### Discover and Document

For EACH discovery, record in QA_MEMORY.md:
- Tech stack detected
- Total routes/pages
- Total API endpoints
- Database tables + RLS policies
- Roles found
- Modules/features found
- Test accounts found
- Existing test suites found
- Feature areas to test
- Feature areas to DEFER
- Multi-tenant: yes/no
- AI features: yes/no
- Real-time: yes/no
- i18n: yes/no

### Present Test Plan Summary

Before proceeding, present:
```
RECONNAISSANCE COMPLETE
========================
Stack: [detected]
Routes: [count]
API endpoints: [count]
DB tables: [count] | RLS policies: [count]
Roles: [count] — [list]
Modules: [count] — [list]
Test accounts found: [count]
Existing tests: [count] files
Phases enabled: [list of applicable phases]
Phases skipped: [list with reasons]
Deferred features: [list]

Proceed with testing? (yes/no)
```
