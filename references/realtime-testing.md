# Real-time Feature Testing — QA Engineering

## Connection
- [ ] WebSocket/SSE connection establishes on page load
- [ ] Connection survives page navigation (if persistent)
- [ ] Reconnection after network drop (within reasonable time)
- [ ] Graceful degradation when real-time unavailable
- [ ] No memory leak from connection listeners

## Live Updates
- [ ] Create record in Tab A → appears in Tab B without refresh
- [ ] Update record in Tab A → updates in Tab B
- [ ] Delete record in Tab A → removes from Tab B
- [ ] Bulk operation reflects across all connected clients

## Presence
- [ ] Online/offline indicators update correctly
- [ ] Typing indicators show/hide correctly
- [ ] User list updates when users join/leave
- [ ] Stale presence cleaned up on disconnect

## Authorization
- [ ] Real-time events respect permissions (User A doesn't get User B's events)
- [ ] Org-scoped events only reach org members
- [ ] Unsubscribe from channels on logout/navigation
