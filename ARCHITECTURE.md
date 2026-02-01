# Architecture

## Overview

ReVens is an Electron application with a React-based renderer and a Node-powered
main process. Configuration and package metadata live in JSON files under
`src/config`.

## Key Areas

### Main Process (Electron)
- Entry: `src/main.js`
- Shared utilities and download logic: `src/main/helper.js`
- IPC handlers: `src/main/ipc.js`

### Renderer (React)
- Entry: `src/app.js`
- UI components: `src/app/components`
- Assets: `src/app/assets`

### Configuration & Data
- App metadata: `src/config/app.json`
- Package definitions: `src/config/items.json`
- Sections and strings: `src/config/sections.json`, `src/config/strings.json`

## Build & Packaging

- Development build: `run.sh` (webpack + electron start)
- Production build: `build.sh` (webpack, packaging, installers, archives)
