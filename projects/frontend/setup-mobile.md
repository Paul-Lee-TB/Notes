# Project: Setup Mobile

**Status:** In Progress  
**Priority:** P1 (High)  
**Started:** 2026-02-02  
**Updated:** 2026-02-02  
**Est. Time:** 1-2 days  

## Overview

Mobile setup and configuration.

## Environments

| Branch/Feature | Dev | Beta | Prod |
|----------------|-----|------|------|
|                | [ ] | [ ]  | [ ]  |

## Tasks

### Backlog
- [ ] 

### To Do
- [ ] `P3` iOS setup

### In Progress
- [ ] `P1` Android setup - get working locally
- [ ] `P1` Get Node 24.12.0 working
- [ ] `P1` Get appropriate JDK 

### Done
- [x] Create project note

## Tech Stack

### Previous Environment (Reference)
- **Node:** 16.14.1
- **JDK:** OpenJDK 11.0.18 (2023-01-17 LTS)
- **Android Studio:** Dolphin | 2021.3.1 Patch 1
- **Android SDK:** Platform 31
- **ANDROID_HOME:** Must be set to Android SDK path

### Target Environment
- **Node:** 24.12.0
- **JDK:** TBD
- **Android Studio:** Otter
- **Android SDK:** TBD 

## Setup Checklist (Windows)

- [ ] Install Node.js 24.12.0
- [ ] Install OpenJDK 11 (or compatible version)
- [ ] Install Android Studio (Otter)
  - [ ] Android SDK
  - [ ] Android SDK Platform
  - [ ] Android Virtual Device
- [ ] Configure Android SDK (Preferences > Appearance & Behavior > System Settings > Android SDK)
  - [ ] Android SDK Build-Tools
  - [ ] Android Emulator
  - [ ] Android SDK Platform-Tools
  - [ ] Intel x86 Emulator Accelerator (HAXM installer)
- [ ] Set ANDROID_HOME environment variable
  - Path: `C:\Users\<username>\AppData\Local\Android\Sdk`

## Starting Android App

### Prerequisites
- Android Studio running with emulator/device connected
- Device created in Device Manager

### Steps

1. Start Android Studio and run emulator/connect device

2. Open VS Code, checkout branch (`rn-mobile-app-new`), go to root (`~/tradingblock`)

3. Run in terminal (git bash):
```bash
yarn clean
yarn
npx lerna bootstrap
npx lerna run check
yarn build:tsc
npx lerna run check
```

4. Open 2 terminals in `~/tradingblock/packages/mobile`:

**Terminal 1:**
```bash
yarn
yarn start
```

**Terminal 2:**
```bash
yarn android:dev   # or any other env
```

## Notes

### 2026-02-02

- Project created
- Priority for today: Get Android mobile working locally
- Updating from Node 16.14.1 to 24.12.0
- Need to determine compatible JDK version
- Upgrading Android Studio from Dolphin to Otter

## Links & Resources

- 
