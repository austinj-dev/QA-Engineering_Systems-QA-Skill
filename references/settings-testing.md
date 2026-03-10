# Settings & Configuration Testing — QA Engineering

## User Settings
- [ ] Profile loads with current data
- [ ] Name, avatar, email update and persist
- [ ] Password change works

## Org Settings (Owner/Admin)
- [ ] General: name, description, logo editable
- [ ] Members: invite, remove, role change
- [ ] Module toggles: reflect in sidebar immediately
- [ ] Notification preferences save

## Persistence
- [ ] Change → reload → persists
- [ ] Change → logout → login → persists
- [ ] Revert → persists

## Permissions
- [ ] Owner: all settings
- [ ] Admin: most (not billing/danger)
- [ ] Manager: limited
- [ ] Member: profile only
- [ ] Viewer: profile read-only