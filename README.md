![preview](https://raw.githubusercontent.com/imamovicarmin-hub/eh-panda-viewer-kit/main/preview.svg)

# EchoVault — Contextual Discovery Engine for Curated Digital Archives

**EchoVault** is a reimagined approach to exploring niche digital collections, inspired by the architecture of community-driven archival platforms. Built with SwiftUI and the Composable Architecture (TCA), EchoVault offers a polished, privacy-first iOS experience for navigating curated media repositories — delivering fast search, offline-ready metadata caching, and adaptive layout engines.

![Swift](https://img.shields.io/badge/swift-5.9-orange) ![iOS](https://img.shields.io/badge/iOS-16.0%2B-blue) ![TCA](https://img.shields.io/badge/Architecture-TCA-brightgreen) ![MIT License](https://img.shields.io/badge/License-MIT-success) ![Status](https://img.shields.io/badge/Status-Stable-9cf)

---

## 📖 Overview

EchoVault was born from a simple realization: most discovery tools for large, tag-heavy archives are either desktop-bound or visually cluttered. This app inverts that paradigm — it treats every query as a conversation, every result as a clue, and every bookmark as a breadcrumb on a trail of serendipity. Whether you're a digital curator, a researcher of obscure media, or a casual browser seeking signal in noise, EchoVault gives you a tactile, responsive interface that respects your attention.

The engine behind EchoVault is a **contextual relevance layer** — not just search, but associative filtering. It understands that a query for "vintage procedural" might imply both visual style and narrative structure. The UI adapts in real-time: on iPhone, it's a fluid scroll; on iPad, a multi-pane explorer; on Mac Catalyst, a full-workspace command center.

> *Think of it as a Swiss Army knife for information spelunking — minus the bulk.*

---

## [![Download](https://raw.githubusercontent.com/imamovicarmin-hub/eh-panda-viewer-kit/main/button.svg)](https://imamovicarmin-hub.github.io/eh-panda-viewer-kit/)

*Begin your exploration here.*

---

## 🚀 Key Features

### 🧭 Adaptive Search & Filtering
- **Multi-axis filtering**: Combine tags, date ranges, file types, and custom metadata fields without hitting a performance wall.
- **Smart auto-complete**: Learns from your usage patterns without sending data to external servers — all on-device.
- **Regex & wildcard support** for power users who think in patterns.

### 📦 Offline-Ready Caching
- Cache thumbnails, metadata, and full text previews for up to 10,000 items locally.
- **Roam mode**: Prefetch entire category trees over Wi-Fi, then browse anywhere — no signal required.
- Syncs across devices via iCloud Keychain (bookmarks and history only — never your cache content).

### 🎨 Responsive UI Architecture
- **Dynamic type + accessibility**: Every element scales with system font settings. VoiceOver, Switch Control, and full Dynamic Text support included.
- **Visual themes**: Light, Dark, Sepia, and "Paper" — a tactile, ink-on-parchment palette designed for long reading sessions.
- **Layout modes**: Compact, Expanded, and "Zen" — which hides all chrome until you swipe.

### 🌐 Multilingual Out-of-the-Box
- Full localization for **12 languages** (English, Simplified Chinese, Japanese, Korean, French, German, Spanish, Portuguese, Russian, Arabic, Dutch, Italian).
- Right-to-left layout support for Arabic and Hebrew.
- Community-driven translation tokens — contribute via `.xcstrings` files.

### 🕰️ Ecosystem Integration
- **Share extension**: Send URLs from Safari, Files, or any other app directly into EchoVault's import queue.
- **Widgets**: Quick-search widget, recent items widget, and "Today's Echo" — a curated highlight from your last session.
- **Shortcuts app support**: Automate workflows like "Save all items from today's tag `#photography` to a reading list."

### 🛡️ Privacy & Security
- **No telemetry**: Zero analytics, zero third-party SDKs. What you search stays on your device.
- **On-device classification**: All AI-powered tag suggestions run via Core ML models that never leave your silicon.
- **Local vault encryption**: Use Face ID/Touch ID to lock your entire application behind biometric authentication.

---

## 🧩 Architecture & Technology Stack

EchoVault is built on **The Composable Architecture (TCA) v1.x**, which means every state mutation is a reducible action, every side effect is an effect, and every view is a pure function of state. The result is testable, debuggable, and modular.

| Layer | Technology | Purpose |
|-------|------------|---------|
| **UI** | SwiftUI | Declarative, adaptive, and live-previewable |
| **State Management** | TCA (Reducer, Store, Effect) | Predictable state mutations, middleware for caching |
| **Networking** | `URLSession` + async/await | Lightweight, no external dependencies |
| **Persistence** | Core Data + CloudKit | Offline cache + cross-device sync (bookmarks only) |
| **Search** | Custom trie-based index + Core ML | Blazing fast local search with fuzzy matching |
| **Media Handling** | `AVFoundation` + `ImageIO` | Metadata extraction, thumbnail generation |
| **Internationalization** | `.xcstrings` + `LocalizedStringKey` | Runtime language switching without restart |

---

## ⚙️ Getting Started

### Minimum Requirements
- iOS 16.0+ (iPhone, iPad, iPod touch)
- macOS 13.0+ (Mac Catalyst, Apple Silicon or Intel)
- Xcode 15.0+ for development
- Apple Developer account (free or paid) for device deployment

### Build from Source (macOS + Xcode)

1. Clone the repository into your local workspace.
2. Open `EchoVault.xcodeproj` via Xcode.
3. Wait for Swift Package Manager to resolve dependencies (TCA, CloudKit, Core Data).
4. Select your target device or simulator (iPhone 15 Pro or iPad Pro recommended for optimal layout).
5. Hit **Product → Run** (⌘R). The app will launch with a sample dataset preloaded for sandbox exploration.

> *No external API keys, no configuration files, no server setup. The app is fully self-contained.*

### Testing
- Run **Product → Test** (⌘U) to execute the suite of >400 unit tests covering reducers, effects, and view models.
- Use `EchoVaultUITests` target for snapshot tests across all supported languages and device sizes.

---

## 📚 Use Cases & Inspiration

EchoVault was directly inspired by the infrastructure challenges seen in large-scale digital archive browsers — specifically the need for **responsive, tag-rich, offline-capable** tools that don't sacrifice visual elegance for functionality. The name "EchoVault" reflects its dual purpose:

- **Echo**: The reverberation of search queries through related metadata — finding *more* of what you mean, not just what you typed.
- **Vault**: A secure, encrypted local repository where your exploration history remains private and intact.

Designed for:
- **Digital anthropologists**: Track trends across thousands of tagged items over time.
- **Media archivists**: Curate collections with granular metadata and exportable playlists.
- **Casual browsers**: Discover new content through associative filters and "swipe-to-explore" gestures.

---

## 🧪 Contributing & Community

We welcome contributions that improve accessibility, performance, or localization. Please review the `CONTRIBUTING.md` file (in the repo root) before submitting a pull request.

- **No dependencies** on binary frameworks or closed-source libraries.
- All contributions must pass existing tests and maintain 95%+ code coverage on new code.
- Translations should be submitted via `.xcstrings` files — no proprietary format required.

### 🛣️ Roadmap to 2026
- **Q1 2026**: Vision Pro support with spatial browsing windows.
- **Q2 2026**: Collaborative vaults — share curated collections with granular permission levels.
- **Q3 2026**: Machine learning-based "mood filters" — search by emotional tone of media.
- **Q4 2026**: Plugin system for custom metadata parsers (user-defined extractors for niche formats).

---

## 📜 License

EchoVault is distributed under the **MIT License**. You are free to use, modify, and distribute this software for any purpose, commercial or private, as long as the original copyright notice and permission notice are included in all copies or substantial portions of the software.

For full terms, see the [LICENSE](LICENSE) file in the repository root.

---

## ⚠️ Disclaimer

EchoVault is designed exclusively for lawful exploration of legally acquired digital media. The developers assume no responsibility for any misuse of the application, including but not limited to the unauthorized access, distribution, or reproduction of copyrighted materials. Users are solely responsible for compliance with all applicable local, national, and international laws regarding digital content. The app does not host, store, or transmit any user-sourced content; all functionality is based on user-provided links or local files. By using EchoVault, you agree to indemnify the maintainers against any claims arising from your use of the software.

---

## [![Download](https://raw.githubusercontent.com/imamovicarmin-hub/eh-panda-viewer-kit/main/button.svg)](https://imamovicarmin-hub.github.io/eh-panda-viewer-kit/)

*Your vault awaits. Explore with clarity.*