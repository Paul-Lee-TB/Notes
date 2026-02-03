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
- [ ] `P1` Android setup - get working locally (almost complete)

### Done
- [x] Create project note
- [x] `P1` Get Node 24.12.0 working
- [x] `P1` Get appropriate JDK (Java 17.0.17)
- [x] Install and configure Android Studio Otter 3

## Tech Stack

### Previous Environment (Reference)
- **Node:** 16.14.1
- **JDK:** OpenJDK 11.0.18 (2023-01-17 LTS)
- **Android Studio:** Dolphin | 2021.3.1 Patch 1
- **Android SDK:** Platform 31
- **ANDROID_HOME:** Must be set to Android SDK path

### Target Environment
- **Node:** 24.12.0
- **JDK:** Java 17.0.17
- **Android Studio:** Otter 3
- **Android SDK:** TBD 

## Setup Checklist (Windows)

- [x] Install Node.js 24.12.0
- [x] Install JDK (Java 17.0.17)
- [x] Install Android Studio (Otter 3)
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
- **EOD:** Setup nearly complete
  - Installed Java 17.0.17
  - Installed Android Studio Otter 3
  - Node v24.12.0 configured
  - Build completes successfully
  - **ISSUE:** App launches but hangs before reaching login page
    - Installation appears to hang right before app finishes loading
    - Working with Daniel to finalize

## Links & Resources

- 
