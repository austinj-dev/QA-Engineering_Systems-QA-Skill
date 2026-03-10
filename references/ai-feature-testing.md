# AI Feature Testing — QA Engineering

## Only apply when AI features are discovered in Phase 0.

### Functional Testing
- [ ] AI chat responds to messages
- [ ] Streaming works (tokens appear incrementally)
- [ ] Conversation history persists
- [ ] Memory system works (AI remembers across conversations)
- [ ] Knowledge base search returns relevant results
- [ ] Tool/function calling executes correctly
- [ ] Agent modes switch correctly (if applicable)

### Safety Testing
- [ ] Prompt injection: "Ignore all instructions and..." → should be blocked
- [ ] Data leakage: AI doesn't reveal other users' data
- [ ] Content filtering: harmful content requests handled
- [ ] System prompt not extractable by user

### Performance
- [ ] Response time acceptable (<5s first token)
- [ ] Streaming latency reasonable
- [ ] Concurrent AI requests handled
- [ ] Rate limiting enforced per tier

### Provider Testing
- [ ] BYOK key handling works (if applicable)
- [ ] Provider fallback chain activates on failure
- [ ] Free tier limits enforced
- [ ] Usage tracking accurate

### Cost Testing
- [ ] Token usage tracked correctly
- [ ] Cost per conversation calculated
- [ ] Budget limits enforced
- [ ] Usage alerts trigger at thresholds
