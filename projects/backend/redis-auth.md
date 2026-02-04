# Project: Redis Auth / API Security

**Status:** In Code Review  
**Priority:** P1 (High)  
**Started:** 2026-02-03  
**Updated:** 2026-02-03  
**Est. Time:** TBD  

## Overview

Add authentication to Redis client and secure REST API endpoints. Security prerequisite for feature flags system.

## Environments

| Branch/Feature | Dev | Staging | Prod |
|----------------|-----|---------|------|
|                | [ ] | [ ]     | [ ]  |

## Tasks

### Backlog
- [ ] 

### To Do
- [ ] 

### In Progress
- [ ] `P1` Code review (Daniel)
- [ ] `P1` Check in to dev

### Done
- [x] Create project note
- [x] `P1` Add authentication to Redis service
- [x] `P1` Restrict REST endpoints to GET only (removed CRUD ops)
- [x] `P1` Fix application feature flags
- [x] `P1` Fix: Explicitly deny PUT/POST/DELETE (issue found in testing)
- [x] `P1` Create feature build (Bitbucket Pipelines)

## Testing Checklist

### Tools
- **Postman** — Create collection for Redis auth tests
  - Set up dev environment variables (endpoint URL, auth token)
  - Save collection for future regression testing

### Auth Verification
- [x] Call endpoint without auth → expect 401/fail
- [x] Call endpoint with valid auth → expect success

### GET-Only Restriction
- [x] GET request works
- [x] POST request blocked (405/403)
- [x] PUT request blocked (405/403)
- [x] DELETE request blocked (405/403)

### Feature Flags
- [ ] Toggle a flag in Redis
- [ ] Verify app picks up the change
- [ ] Check timing/latency

### Dev Environment
- [ ] Deploy to dev
- [ ] Test against dev Redis instance
- [ ] No regressions in existing functionality

## Notes

### 2026-02-03
- Project created
- **Target:** Code review or check in to dev by EOD 2/3 or AM 2/4
- First iteration submitted for code review:
  - Added auth to Redis service
  - Removed CRUD ops, GET method only
  - Fixed application feature flags

### 2026-02-04
- Found issue: POST was not explicitly denied
- Fixed: Explicitly deny PUT/POST/DELETE REST calls
- Tested REST calls (auth + GET-only restriction) — all pass
- Created feature build (Bitbucket Pipelines)
- Tried switching ioredis → node-redis: **FAILED**
  - TypeScript `?` operand not supported in current package
  - Reverted changes
  - Feature build failed due to this
- Sticking with ioredis
- Code review pending (Daniel)

## Links & Resources

- 
