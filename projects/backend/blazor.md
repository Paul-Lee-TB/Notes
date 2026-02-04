# Project: Blazor

**Status:** In Progress  
**Priority:** P1 (High)  
**Started:** 2026-02-02  
**Updated:** 2026-02-02  
**Est. Time:** 2-3 days  

## Overview

Blazor application project.

## Environments

| Branch/Feature | Dev | Staging | Prod |
|----------------|-----|---------|------|
| feature/option-position-editor | [ ] | [ ] | [ ] |
| feature/options-expirations-page-restore | [ ] | [ ] | [ ] |

## Tasks

### Backlog
- [ ] `#feature-flag` Add feature flag page
- [ ] Add script for bouncing the dev/beta/prod tick proxy

### To Do
- [ ] `P1` Check calculations for open price, cost balance, cost balance per share
- [ ] `P1` Add GSMA changes - utilize AD for SQL access

### In Progress
- [ ] `P1` Push options expirations page changes to dev (Toby approved)
- [ ] `P1` **INVESTIGATION** - Build/publish pipeline options:
  - Find msbuild for publish script, OR
  - Use Jenkins for compilation
  - Output to Gitea or similar

### Done
- [x] Create project note
- [x] Fix the local build
- [x] Add keyboard enter fix for login page
- [x] Add keyboard enter fix for open position editor page
- [x] Feature branch code review
- [x] Merge Toby's code into dev

## Tech Stack

- .NET 8+
- Blazor (Server / WebAssembly / Web App)
- C#

## Notes

### 2026-02-02

- Got the Blazor project working properly
- Implemented enter key for login and open position editor pages
- Feature branch submitted for code review
- Finished merge with Toby's code into dev
- Deploying changes to dev Blazor server (follow up tomorrow)
- **PROD ISSUE**: Option expirations page

### 2026-02-04

- Toby approved pushing options expirations page to dev
- Toby suggested investigating build pipeline:
  - Option A: Find msbuild for publish script
  - Option B: Use Jenkins for compilation
  - Store output in Gitea or similar
- Need to investigate and clarify approach

## Links & Resources

- [Blazor Documentation](https://learn.microsoft.com/en-us/aspnet/core/blazor/)
