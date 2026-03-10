# Error Message Quality Testing — QA Engineering

## User-Facing Errors
- [ ] Messages are helpful, not generic ('Email is required' not 'Error')
- [ ] Messages suggest next action ('Try again' or 'Contact support')
- [ ] No technical jargon (no stack traces, SQL, internal codes)
- [ ] Messages match locale/language
- [ ] Messages use correct terminology (industry pack aware)

## Form Errors
- [ ] Required field: specific message per field
- [ ] Format error: specific ('Must be valid email' not 'Invalid')
- [ ] Errors clear when corrected
- [ ] Error summary accessible for screen readers

## Server Errors
- [ ] 500: friendly page (not raw error)
- [ ] 404: helpful page with navigation
- [ ] API errors: structured object (code, message, details)
- [ ] No stack traces in production