# DroidWright

<div align="center">

![DroidWright Banner](./droidwright-banner.jpg)

**Powerful, flexible automation for Android — right on your device.**

[![Version](https://img.shields.io/badge/version-1.0.0--beta-blue)](https://github.com/tas33n/droidwright/releases)
[![License](https://img.shields.io/badge/license-MIT-green)](https://github.com/tas33n/droidwright/blob/main/LICENSE)
[![Platform](https://img.shields.io/badge/platform-Android-lightgrey)](https://www.android.com)

</div>

## What is DroidWright?

DroidWright is an on-device automation engine that runs JavaScript (QuickJS) with a Playwright/Appium-inspired API surface. It needs no desktop, no ADB cable—just your Android device.

### Highlights
- **Node-style runtime**: `os`, `fs` (sync), `path`, `crypto`, dialogs, global `fetch`, and a lightweight `axios` helper.
- **Deep UI automation**: tap, swipe, scroll, set text, wait for elements, dump trees—backed by Accessibility Service.
- **App control**: launch/close apps, clipboard access, device info, toasts, resilient screenshots (Android 14 compliant; path/base64).
- **Developer-friendly editor**: TextMate highlighting, VS Code–style status, Rhino validation with line/column errors.
- **Workspace-first**: scripts/logs/screenshots in `Documents/DroidWright` when allowed; easy to edit from any editor.
- **Safety built-in**: rate limiting, resource monitoring, foreground services where required.

## Getting Started
1. Install the latest APK from [Releases](https://github.com/tas33n/droidwright/releases) or build with `./gradlew assembleDebug`.
2. Enable the Accessibility service and overlay permission.
3. Place scripts in `Documents/DroidWright/scripts` (or create them in-app).
4. Run scripts and monitor logs in real time; use floating controls to pause/stop.

## Examples
- `examples/ss-telegram.js` — multi-shot capture and Telegram upload via global `fetch`.
- `examples/api-selftest.js` — exercises os/fs/path/crypto/fetch/axios/dialog.
- `examples/dialog-test.js` — verifies overlay dialogs (alert/confirm/prompt/select).

## Recent Release (Beta 4)
- Android 14–ready screenshots (media projection service type, virtual display reuse).
- Node-like globals and network upgrades (fetch/axios, multipart uploads).
- Dialog API hardened for overlay use; fs resolves to workspace root and supports rename.
- Editor UX polish: IME-safe, bottom nav hidden, VS Code–style status, precise validation.

## Contributing
Issues and PRs are welcome—bug fixes, docs, and example scripts especially. See [LICENSE](https://github.com/tas33n/droidwright/blob/main/LICENSE) for terms.
