# Monitoring Readiness Testing — QA Engineering

## Health Checks
- [ ] /health endpoint exists and responds 200
- [ ] Checks database, cache, external services
- [ ] Responds quickly (<500ms)

## Error Tracking
- [ ] Service configured (Sentry etc.)
- [ ] Errors captured with context
- [ ] Source maps uploaded

## Alerting
- [ ] Rules configured for error spikes, downtime
- [ ] Channels configured (email, Slack)
- [ ] Tested (triggered and verified)

## Logging
- [ ] Structured format (JSON)
- [ ] Correlation IDs
- [ ] No PII in logs
- [ ] Retention policy configured