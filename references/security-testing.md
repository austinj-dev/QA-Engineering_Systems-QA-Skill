# Security Testing — QA Engineering (OWASP Top 10 2025)

## NEVER SKIP THIS PHASE. Security testing is mandatory for every project.

### A01:2025 — Broken Access Control

Tests:
- [ ] IDOR: Change entity IDs in URLs to access other users/orgs data
- [ ] Horizontal escalation: User A accesses User B's data
- [ ] Vertical escalation: Low-privilege user accesses admin functions
- [ ] Force browsing: Access admin URLs without admin role
- [ ] API auth: Every API route has auth check
- [ ] Method override: POST routes don't accept GET
- [ ] Multi-tenant isolation: Org A cannot see Org B data
- [ ] Direct object reference: Manipulate query params to access unauthorized data

### A02:2025 — Security Misconfiguration

Tests:
- [ ] Security headers present (HSTS, CSP, X-Frame, X-Content-Type, Referrer-Policy)
- [ ] Server info not leaked in headers
- [ ] Error pages don't show stack traces
- [ ] Debug mode disabled
- [ ] Default credentials removed
- [ ] Directory listing disabled
- [ ] Source maps not in production build
- [ ] Admin endpoints not publicly discoverable

### A03:2025 — Software Supply Chain

Tests:
- [ ] npm audit / pip audit / cargo audit — check for known vulnerabilities
- [ ] Lock file exists and is up to date
- [ ] No typosquatting packages
- [ ] Dependencies have acceptable licenses

### A04:2025 — Cryptographic Failures

Tests:
- [ ] HTTPS enforced (no HTTP)
- [ ] TLS 1.2+ only
- [ ] Passwords hashed (bcrypt/argon2, NOT MD5/SHA1)
- [ ] Sensitive data encrypted at rest
- [ ] No secrets in client-side code
- [ ] No secrets in URL parameters

### A05:2025 — Injection

Tests:
- [ ] XSS: Input `<script>alert('XSS')</script>` in 5+ form fields
- [ ] XSS: Input `<img src=x onerror=alert(1)>` in text fields
- [ ] XSS: Test URL parameters with injection payloads
- [ ] SQL: Input `' OR '1'='1` in search and filter fields
- [ ] SQL: Parameterized queries verified (not string concatenation)
- [ ] Command injection: If any shell exec, test with `; ls` payloads
- [ ] NoSQL injection: If MongoDB, test operator injection

### A06:2025 — Insecure Design

Tests:
- [ ] Rate limiting on auth endpoints
- [ ] Rate limiting on API endpoints
- [ ] Account lockout after failed attempts
- [ ] Business logic abuse scenarios tested (price manipulation, quantity tampering)
- [ ] Resource exhaustion prevention (large file upload, infinite loops)

### A07:2025 — Identification & Authentication Failures

Tests:
- [ ] Password strength requirements enforced
- [ ] Session expires after inactivity
- [ ] Logout invalidates session
- [ ] Tokens not exposed in URLs
- [ ] MFA available for sensitive operations
- [ ] Session fixation prevented

### A08:2025 — Software & Data Integrity Failures

Tests:
- [ ] CI/CD pipeline secured
- [ ] No unsigned/unverified code in deploy
- [ ] Webhook signatures verified

### A09:2025 — Security Logging & Monitoring Failures

Tests:
- [ ] Auth events logged (login, logout, failed attempts)
- [ ] Access to sensitive data logged
- [ ] Logs don't contain sensitive data (passwords, tokens)
- [ ] Error tracking configured

### A10:2025 — Server-Side Request Forgery (SSRF)

Tests:
- [ ] User-supplied URLs validated
- [ ] Internal network not accessible via user input
- [ ] Redirect chains validated

### Additional Security Checks

- [ ] CORS properly restrictive (not wildcard)
- [ ] Cookies: httpOnly, secure, SameSite flags
- [ ] CSRF protection on state-changing operations
- [ ] File upload: type validation, size limits, no executable
- [ ] API keys not in client bundle (grep source)
- [ ] Supabase service role key not in client
- [ ] Environment variables all present
- [ ] No hardcoded credentials anywhere
