# Email & Notification Testing — QA Engineering

## Transactional Email
- [ ] Welcome email sends on signup
- [ ] Password reset email sends and link works
- [ ] Email verification sends and link works
- [ ] Invitation email sends with correct link
- [ ] Invoice/receipt email sends with correct data
- [ ] Notification digest emails send at scheduled time
- [ ] Emails render correctly (check with Litmus/Email on Acid or manual)
- [ ] From address correct and not spam-flagged
- [ ] Reply-to address correct
- [ ] Unsubscribe link present and functional
- [ ] Email contains correct dynamic data (user name, amounts, dates)
- [ ] No PII leakage in email headers

## In-App Notifications
- [ ] Bell/icon shows unread count
- [ ] Clicking notification navigates to correct page
- [ ] Mark as read (individual and bulk)
- [ ] Notification list loads and paginates
- [ ] Real-time notification appears without refresh
- [ ] Empty state when no notifications
- [ ] Notification preferences respected (if configured off, don't send)

## Toast Messages
- [ ] Success toast on create/update/delete
- [ ] Error toast on failed operations
- [ ] Auto-dismiss after reasonable time
- [ ] No infinite stacking
- [ ] Correct terminology per context (industry pack, etc.)
- [ ] Toast doesn't block UI interaction

## Push Notifications (if applicable)
- [ ] Push permission prompt works
- [ ] Push sends on trigger events
- [ ] Push deep links to correct page
- [ ] Push works when app is backgrounded
