# State Transition Testing — QA Engineering

## For Every Entity With Statuses
1. Map all states and valid transitions
2. Test every valid transition succeeds
3. Test every INVALID transition is blocked
4. Verify authorized roles can trigger each transition
5. Verify side effects fire (notifications, logs, automations)
6. Verify UI updates status correctly
7. Verify filter/sort by status works
8. Verify bulk status change works
9. Verify timestamps recorded per transition