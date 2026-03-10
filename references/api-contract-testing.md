# API Contract Testing — QA Engineering

## Every API endpoint must be tested for:

### Request Validation
- [ ] Correct HTTP method (GET/POST/PUT/PATCH/DELETE)
- [ ] Required headers present (Authorization, Content-Type)
- [ ] Request body schema validation (required fields, types, constraints)
- [ ] Missing required fields → 400 with descriptive error
- [ ] Extra/unknown fields → handled (ignored or rejected)
- [ ] Invalid data types → 400 with field-specific error
- [ ] Empty body on POST/PUT → 400

### Response Validation
- [ ] Correct status codes (200, 201, 204, 400, 401, 403, 404, 409, 422, 429, 500)
- [ ] Response body matches documented schema
- [ ] Pagination format consistent (cursor, offset, total count, next/prev)
- [ ] Error response format consistent across all endpoints
- [ ] No internal details leaked in error responses (no stack traces, no SQL)
- [ ] Content-Type header correct
- [ ] Rate limit headers present (X-RateLimit-Limit, Remaining, Reset)

### Auth Testing Per Endpoint
- [ ] Unauthenticated request → 401
- [ ] Invalid token → 401
- [ ] Expired token → 401
- [ ] Insufficient permissions → 403
- [ ] Valid token + authorized → success

### Versioning
- [ ] API version in URL or header
- [ ] Old version still works (if backward compatible)
- [ ] Breaking changes properly versioned

### Edge Cases
- [ ] Empty collections return [] not null
- [ ] Single item vs collection format correct
- [ ] ID not found → 404 (not 500)
- [ ] Duplicate create → 409 (not 500)
- [ ] Concurrent modifications handled
- [ ] Large payload handling (request size limits)
- [ ] Unicode/special characters in string fields
- [ ] SQL injection via API parameters
- [ ] XSS via API input fields
