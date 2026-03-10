# Webhook Testing — QA Engineering

## Inbound Webhooks
- [ ] Endpoint accepts POST requests
- [ ] Signature verification works (HMAC-SHA256 or equivalent)
- [ ] Invalid signature → 401
- [ ] Missing signature → 401
- [ ] Payload parsing succeeds for all event types
- [ ] Idempotency: sending same webhook twice doesn't duplicate data
- [ ] Unknown event types handled gracefully (logged, not errored)
- [ ] Responds 200 quickly (async processing, not blocking)
- [ ] Retry handling: re-delivered webhook doesn't cause issues
- [ ] Large payloads handled within size limits
- [ ] Rate limiting on webhook endpoint

## Outbound Webhooks
- [ ] Webhook fires on configured trigger events
- [ ] Payload format matches documentation
- [ ] Includes signature header for verification
- [ ] Retry on failure (exponential backoff)
- [ ] Dead letter handling for permanent failures
- [ ] Webhook delivery logging
- [ ] Webhook disable after N consecutive failures
