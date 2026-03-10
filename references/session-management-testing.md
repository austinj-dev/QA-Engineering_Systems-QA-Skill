# Session Management Testing — QA Engineering

- [ ] Session created on login
- [ ] Expires after inactivity timeout
- [ ] Refresh on activity extends timeout
- [ ] Logout invalidates completely
- [ ] Cannot reuse token after logout
- [ ] Token not in URL parameters
- [ ] Token in httpOnly cookie (not localStorage)
- [ ] Multiple tabs share session
- [ ] Multiple devices independent sessions
- [ ] Expired → redirect to login with return URL
- [ ] Re-login → redirect back to previous page
- [ ] Remember me extends duration
- [ ] Admin force-logout terminates all sessions