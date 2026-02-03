# Epic: Feature Flags

**Status:** Planning  
**Priority:** P2 (Medium)  
**Started:** 2026-02-02  
**Updated:** 2026-02-02  
**Est. Time:** 1-2 days (total across all projects)  

## Overview

Implement feature flag system across backend and frontend.

## Related Tasks

Search for `#feature-flag` tag across all projects.

| Project | Task | Status |
|---------|------|--------|
| Redis Auth (BE) | Add auth to Redis client | To Do |
| Redis Auth (BE) | Add auth to REST endpoints | To Do |
| RestHub (BE) | Add feature flag Redis code to RestHub | To Do |
| Blazor (BE) | Add feature flag page | Backlog |
| Feature Flags (FE) | Remove Redis service when BE RestHub is up | To Do |

## Security Concerns

- [ ] `P1` Add authentication to Redis client
- [ ] `P1` Add authentication to REST calls (secure endpoints)

## Sequence

1. **Backend**: Add auth to Redis client and REST endpoints
2. **Backend**: Add feature flag Redis code to RestHub
3. **Backend**: Add feature flag page to Blazor admin
4. **Frontend**: Remove Redis service once RestHub is live

## Notes

### 2026-02-02

Epic created to track feature flag implementation across services.

## Links & Resources

- 
