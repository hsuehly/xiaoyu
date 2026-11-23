# 小遇 Xiaoyu

[简体中文](README.md) | **English**

A digital human companion app built with Flutter. Customize your companion's appearance, persona, and voice, and interact through real-time voice and video calls.

Supports **iOS / Android** · Current version `0.1.0+1` · **Closed beta** · Powered by Vidu S2-Avatar Real-Time

## Interface Preview

A dark background with soft purple accents, featuring a branded launch screen, floating two-tab navigation, horizontal character lists, full-screen calls, and text/action input panels.

The following iOS screenshots show the Home, Me, character creation, and call screens.

| Home | Me | Create Character |
| --- | --- | --- |
| ![iOS Home](docs/images/ios-home.png) | ![iOS Me](docs/images/ios-me.png) | ![iOS Create Character](docs/images/ios-edit.png) |

| Call View 1 | Call View 2 | Call View 3 | Call View 4 |
| --- | --- | --- | --- |
| ![iOS Call View 1](docs/images/ios-live1.png) | ![iOS Call View 2](docs/images/ios-live2.png) | ![iOS Call View 3](docs/images/ios-live3.png) | ![iOS Call View 4](docs/images/ios-live4.png) |

## Core Features

- **Character customization**: Choose an official avatar or upload a photo, define a persona, and edit or save drafts.
- **Voice selection**: Browse Qwen and Doubao voices by category and listen to previews.
- **Real-time calls**: Interact with a digital human in full screen, with microphone muting, playback controls, audio output routing, and hang-up controls.
- **Text and actions**: Qwen supports text conversations; both Qwen and Doubao support categorized quick actions.
- **Call history**: Characters, calls, and messages are stored locally. View details and reconcile call termination status with the platform.

## Quick Start

[Download Android APK](https://github.com/hsuehly/xiaoyu/releases) · [Automated Release Guide](docs/ANDROID_RELEASE.md)

[Unsigned iOS IPA](https://github.com/hsuehly/xiaoyu/releases) · [Build and Re-signing Guide](docs/IOS_RELEASE.md) (re-signing is required before installation)

The development environment uses Flutter `3.50.0` / Dart `3.14.0`. The app supports Android 8.0+ and iOS 15+. See the [Development Guide](docs/DEVELOPMENT.md) for platform SDK and signing configuration.

```sh
git clone https://github.com/hsuehly/xiaoyu.git
cd xiaoyu
flutter pub get
flutter devices
flutter run -d DEVICE_ID
```

Replace `DEVICE_ID` with an ID from the device list. After launching the app:

1. Configure and validate your Vidu API Key under Me → Settings (top right) → Account Settings.
2. Choose an official avatar or upload a photo, enter a persona, select a voice, and wait for the avatar to become ready.
3. Tap a character image under My Digital Humans, confirm billing, and allow microphone access to start a call.

Real calls require real-time API access and sufficient balance on [Vidu](https://platform.vidu.cn/). Billing and call termination status are determined by the platform's records. If a call is marked as pending reconciliation, continue checking it in the call history.

The mainland China version of Doubao supports voice and quick actions. Text conversations and changing voices during a call are currently unavailable. Keep the app in the foreground during calls.

The app is currently in closed beta. The component edition, knowledge base import, memory management, and in-app voice cloning are not yet available. See the [Usage Guide](docs/USAGE.md) for the full scope.

## Detailed Documentation

The linked project documents are currently in Chinese.

| Document | Contents |
| --- | --- |
| [Usage Guide](docs/USAGE.md) | Account configuration, character creation, call controls, feature limitations, and data handling |
| [Development Guide](docs/DEVELOPMENT.md) | Development environment, iOS signing, code generation, builds, and project structure |
| [Engineering Guidelines](AGENTS.md) · [Harness](docs/HARNESS.md) | Development workflow, testing, coverage, and device acceptance checks |
| [Product Requirements](docs/PRD.md) · [Technical Architecture](docs/TECHNICAL_ARCHITECTURE.md) · [Implementation Decisions](docs/DECISIONS.md) | Product behavior, layered design, and technology choices |
| [Voice Catalog](docs/VOICE_CATALOG.md) · [Quick Actions](docs/QUICK_ACTIONS.md) | Provider capabilities, catalog mapping, and maintenance |
| [Design Reference](design.html) · [Design Notes](DESIGN.md) · [Glass Component Migration](docs/LIQUID_GLASS_EASY_MIGRATION.md) | Screen appearance and component conventions |

## Related Links

[Vidu Developer Platform](https://platform.vidu.cn/) · [Flutter](https://flutter.dev/) · [LINUX DO Community](https://linux.do/)

## License

Copyright (c) 2026 hsuehly. Original code is licensed under [AGPL-3.0-only](LICENSE). Use, modification, and distribution must comply with the license's source code availability requirements.

Brand assets and third-party materials are excluded from this code license. Third-party dependencies and SDKs remain subject to their respective licenses and terms of service.
