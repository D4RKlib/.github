# 🌌 D4RKLib Suite

![.NET](https://img.shields.io/badge/.NET-9.0-512BD4?style=for-the-badge&logo=dotnet)
![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)
![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20Cross%20Platform-lightgrey?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Active%20Development-success?style=for-the-badge)

**D4RKLib** is a collection of high-performance, modular, and developer-ergonomic .NET 9 libraries designed to accelerate C# application development. Rather than a monorepo, it is structured as a suite of decoupled libraries, each hosted in its own dedicated GitHub repository. They are organized under a unified naming convention and workspace folder structure for local development simplicity, offering focused packages for core system concerns—ranging from real-time networking and database ORMs to low-level Windows UI hooks and modern OpenAI integrations.

---

## 📂 Workspace Layout

For local development, the repositories are cloned into a structured directory layout that mirrors their package naming convention:

```
D4RKLib/
├── ⚙️  Commands/
│    ├── CommandFlow/        # Action routing and dispatching
│    └── CommandMessages/    # Serialization contracts for command payloads
├── 💾  Data/
│    ├── MySQL/              # Async-first MySQL ORM
│    ├── Sqlite/             # Zero-friction SQLite ORM
│    └── Trackables/         # Object dirty-tracking / INotifyPropertyChanged
├── 🗺️  Google/
│    ├── Firebase/           # Auth, FCM Messaging, Analytics, Crashlytics (MAUI + Server)
│    └── Maps/               # Places, Routes, Geocoding, Static Maps, Elevation, Time Zone
├── ⌨️  Input/
│    └── KeyboardShortcuts/  # OS-level global keyboard shortcut hooks
├── ☁️  Microsoft/
│    └── Graph/              # OneDrive & Mail wrappers (no bloated Graph SDK)
├── 🌐  Networking/
│    ├── Discovery/          # LAN UDP auto-discovery
│    ├── Rest/               # Strongly-typed REST + JWT clients
│    ├── Sse/                # Server-Sent Events client
│    ├── Subscriptions/      # In-memory Pub/Sub engine
│    ├── WebHost/            # Composable Kestrel HTTP/WebSocket host
│    └── WebSocket/          # Event-driven WebSocket client
├── 🤖  OpenAI/
│    └── ApiSdk/             # Fluent OpenAI SDK (Chat, Tools, Audio, Images)
└── 🖥️  UI/
     └── WinForms/
          ├── DropKit/        # Fluent drag & drop for WinForms
          └── InputBox/       # Polished input dialogs (dark/light, validation)
```

---

## 📦 Package Registry

Below is a detailed overview of all libraries included in the **D4RKLib** suite, organized by category:

### ⚙️ Commands & Flow Control
Orchestrate execution logic and structure message communication between different layers of your applications.

| Package | GitHub Repository | Stability | Description |
| :--- | :--- | :--- | :--- |
| **D4RKLib.Commands.CommandFlow** | [`D4RKLib.CommandFlow`](https://github.com/D4RKlib/D4RKLib.CommandFlow) | ![Alpha](https://img.shields.io/badge/stability-alpha-orange?style=flat-square) | **Command routing system.** Lightweight dispatching with metadata-aware filtering and execution routing. |
| **D4RKLib.Commands.CommandMessages** | [`D4RKLib.CommandMessages`](https://github.com/D4RKlib/D4RKLib.CommandMessages) | ![Alpha](https://img.shields.io/badge/stability-alpha-orange?style=flat-square) | **Protocol contracts.** Structured serialization/deserialization for command payloads and message definitions. |

### 💾 Data & Object Tracking
Lightweight persistence layers and tracking mechanisms that avoid the overhead of heavy frameworks.

| Package | GitHub Repository | Stability | Description |
| :--- | :--- | :--- | :--- |
| **D4RKLib.Data.MySQL** | [`D4RKLib.Data.MySQL`](https://github.com/D4RKlib/D4RKLib.Data.MySQL) | ![Stable](https://img.shields.io/badge/Stable-blue?style=flat-square) | **Async-first MySQL ORM.** High-performance mapping, code-first automatic schema syncing, JSON columns, and transactions. |
| **D4RKLib.Data.Sqlite** | [`D4RKLib.Data.Sqlite`](https://github.com/D4RKlib/D4RKLib.Data.Sqlite) | ![Stable](https://img.shields.io/badge/Stable-blue?style=flat-square) | **Zero-friction SQLite ORM.** "God-tier" local DB management with automatic migrations, JSON/Enum mapping, and LINQ-to-SQL translation. |
| **D4RKLib.Data.Trackables** | [`D4RKLib.Data.Trackables`](https://github.com/D4RKlib/D4RKLib.Data.Trackables) | ![Stable](https://img.shields.io/badge/Stable-blue?style=flat-square) | **Object dirty-tracking.** Base classes that support property change notification (`INotifyPropertyChanged`) and property delta extraction. |

### ⌨️ Input Handling
System-wide input listeners and hotkey bindings.

| Package | GitHub Repository | Stability | Description |
| :--- | :--- | :--- | :--- |
| **D4RKLib.Input.KeyboardShortcuts** | [`D4RKLib.Input.KeyboardShortcuts`](https://github.com/D4RKlib/D4RKLib.Input.KeyboardShortcuts) | ![Stable](https://img.shields.io/badge/Stable-blue?style=flat-square) | **Global shortcut binding.** Windows global keyboard hooks supporting complex modifier key combinations and async actions. |

### ☁️ Microsoft Cloud Integrations
Lightweight wrappers for Microsoft APIs.

| Package | GitHub Repository | Stability | Description |
| :--- | :--- | :--- | :--- |
| **D4RKLib.Microsoft.Graph** | [`D4RKLib.Microsoft.Graph`](https://github.com/D4RKlib/D4RKLib.Microsoft.Graph) | ![Stable](https://img.shields.io/badge/Stable-blue?style=flat-square) | **Simple Graph API Wrapper.** Clean async DTO wrappers for OneDrive and Mail, removing dependency on the bloated Microsoft Graph SDK. |

### 🌐 Networking & Real-Time Communication
Robust, production-ready libraries covering protocols, servers, clients, and messaging topologies.

| Package | GitHub Repository | Stability | Description |
| :--- | :--- | :--- | :--- |
| **D4RKLib.Networking.Discovery** | [`D4RKLib.Networking.Discovery`](https://github.com/D4RKlib/D4RKLib.Networking.Discovery) | ![Stable](https://img.shields.io/badge/Stable-blue?style=flat-square) | **LAN auto-discovery.** Lightweight UDP broadcaster and listener for discovering local game instances, devices, or services. |
| **D4RKLib.Networking.Rest** | [`D4RKLib.Networking.Rest`](https://github.com/D4RKlib/D4RKLib.Networking.Rest) | ![Stable](https://img.shields.io/badge/Stable-blue?style=flat-square) | **HTTP REST / JWT Clients.** Strongly-typed `RestClient` combined with a `JwtRestClient` that automates login, refresh, and retry flows. |
| **D4RKLib.Networking.SseClient** | [`D4RKLib.Networking.Sse`](https://github.com/D4RKlib/D4RKLib.Networking.Sse) | ![Stable](https://img.shields.io/badge/Stable-blue?style=flat-square) | **Server-Sent Events (SSE).** Event-driven client for `text/event-stream` endpoints supporting automatic reconnect and streaming data. |
| **D4RKLib.Networking.Subscriptions** | [`D4RKLib.Networking.Subscriptions`](https://github.com/D4RKlib/D4RKLib.Networking.Subscriptions) | ![Stable](https://img.shields.io/badge/Stable-blue?style=flat-square) | **In-Memory Pub/Sub Engine.** High-performance thread-safe router featuring O(1) routing, MQTT wildcards (`*`, `**`), and retained messages. |
| **D4RKLib.Networking.WebHost** | [`D4RKLib.Networking.Http`](https://github.com/D4RKlib/D4RKLib.Networking.Http) | ![Stable](https://img.shields.io/badge/Stable-blue?style=flat-square) | **Composable Kestrel Host.** Composable server that supports REST routing, secure WebSockets, SSE, static files, and JWT auth in one instance. |
| **D4RKLib.Networking.WebSocketClient** | [`D4RKLib.Networking.WebSocket`](https://github.com/D4RKlib/D4RKLib.Networking.WebSocket) | ![Stable](https://img.shields.io/badge/Stable-blue?style=flat-square) | **Event-driven WebSocket client.** Minimal wrapper over `ClientWebSocket` that manages connection state and JSON framing. |

### 🗺️ Google Platform SDKs
C# SDKs for Google Maps Platform and Firebase, using modern endpoints and clean strongly-typed APIs.

#### Maps
| Package | GitHub Repository | Stability | Description |
| :--- | :--- | :--- | :--- |
| **D4RKLib.Google.Maps** | [`D4RKLib.Google.Maps`](https://github.com/D4RKlib/D4RKLib.Google.Maps) | ![Alpha](https://img.shields.io/badge/stability-alpha-orange?style=flat-square) | **Fluent Google Maps SDK.** Full builder API covering Places (New), Routes (New), Geocoding, Static Maps, Elevation, and Time Zone. Strongly-typed field mask enums, `System.Text.Json` throughout, and DI-ready. |

#### Firebase
| Package | GitHub Repository | Stability | Description |
| :--- | :--- | :--- | :--- |
| **D4RKLib.Google.Firebase.Core** | [`D4RKLib.Google.Firebase`](https://github.com/D4RKlib/D4RKLib.Google.Firebase) | ![Alpha](https://img.shields.io/badge/stability-alpha-orange?style=flat-square) | **Shared Firebase core.** Token store abstractions, platform enums, and shared interfaces used across all Firebase packages. |
| **D4RKLib.Google.Firebase.Auth** | [`D4RKLib.Google.Firebase`](https://github.com/D4RKlib/D4RKLib.Google.Firebase) | ![Alpha](https://img.shields.io/badge/stability-alpha-orange?style=flat-square) | **Server-side Firebase Auth.** Verify ID tokens, look up user records, and manage users via the Firebase Admin REST API. |
| **D4RKLib.Google.Firebase.Auth.Maui** | [`D4RKLib.Google.Firebase`](https://github.com/D4RKlib/D4RKLib.Google.Firebase) | ![Alpha](https://img.shields.io/badge/stability-alpha-orange?style=flat-square) | **MAUI client Auth.** Sign-in, sign-out, and token refresh for MAUI apps using the Firebase client identity toolkit. |
| **D4RKLib.Google.Firebase.Messaging** | [`D4RKLib.Google.Firebase`](https://github.com/D4RKlib/D4RKLib.Google.Firebase) | ![Alpha](https://img.shields.io/badge/stability-alpha-orange?style=flat-square) | **Server-side FCM.** Send push notifications to devices and topics via the Firebase Cloud Messaging v1 HTTP API. |
| **D4RKLib.Google.Firebase.Messaging.Maui** | [`D4RKLib.Google.Firebase`](https://github.com/D4RKlib/D4RKLib.Google.Firebase) | ![Alpha](https://img.shields.io/badge/stability-alpha-orange?style=flat-square) | **MAUI FCM client.** Receive push notifications and manage device token registration in MAUI apps. |
| **D4RKLib.Google.Firebase.Messaging.Web** | [`D4RKLib.Google.Firebase`](https://github.com/D4RKlib/D4RKLib.Google.Firebase) | ![Alpha](https://img.shields.io/badge/stability-alpha-orange?style=flat-square) | **Web FCM client.** Push notification support for Blazor/web frontends via the Firebase JS SDK bridge. |
| **D4RKLib.Google.Firebase.Analytics.Maui** | [`D4RKLib.Google.Firebase`](https://github.com/D4RKlib/D4RKLib.Google.Firebase) | ![Alpha](https://img.shields.io/badge/stability-alpha-orange?style=flat-square) | **MAUI Analytics.** Log custom events and user properties to Firebase Analytics from MAUI apps. |
| **D4RKLib.Google.Firebase.Crashlytics.Maui** | [`D4RKLib.Google.Firebase`](https://github.com/D4RKlib/D4RKLib.Google.Firebase) | ![Alpha](https://img.shields.io/badge/stability-alpha-orange?style=flat-square) | **MAUI Crashlytics.** Automatic crash reporting and non-fatal exception logging for MAUI apps via Firebase Crashlytics. |

### 🤖 OpenAI API Integration
Build AI-augmented applications without bloated dependencies.

| Package | GitHub Repository | Stability | Description |
| :--- | :--- | :--- | :--- |
| **D4RKLib.OpenAI.ApiSdk** | [`D4RKLib.OpenAI.ApiSdk`](https://github.com/D4RKlib/D4RKLib.OpenAI.ApiSdk) | ![Stable](https://img.shields.io/badge/Stable-blue?style=flat-square) | **Fluent OpenAI C# SDK.** Full-featured builder API covering Chat (w/ Tool/Function calls and Typed Structured Outputs), Speech, Transcription, and Images. |

### 🖥️ Windows Forms UI Componentry
Add modern interactive patterns to WinForms desktop applications.

| Package | GitHub Repository | Stability | Description |
| :--- | :--- | :--- | :--- |
| **D4RKLib.UI.WinForms.DropKit** | [`D4RKLib.DropKit`](https://github.com/D4RKlib/D4RKLib.DropKit) | ![Stable](https://img.shields.io/badge/Stable-blue?style=flat-square) | **Fluent Drag & Drop.** Complete supertool for WinForms drag/drop workflows, animated live previews, file exports, and tag validation. |
| **D4RKLib.UI.WinForms.InputBox** | [`D4RKLib.InputBox`](https://github.com/D4RKlib/D4RKLib.InputBox) | ![Stable](https://img.shields.io/badge/Stable-blue?style=flat-square) | **Polished Input Dialogs.** Customizable user prompts featuring dark/light themes, regular expression inputs, and built-in validation rules. |

---

## 🛠️ Local Development & Workspace Setup

### Prerequisites
- **.NET SDK 9.0+**
- Visual Studio 2022 (with WinForms workload for UI libraries) or JetBrains Rider.

### Workspace Setup
To clone all libraries into the expected workspace structure, you can clone each repository into its respective directory matching the layout.

### Building & Testing
Each repository is self-contained and contains its own solution file (e.g., `D4RKLib.OpenAI.ApiSdk.sln`). Navigate to a specific package's folder to compile or test it:
```bash
cd OpenAI/ApiSdk
dotnet build
dotnet test
```

### Reference & Consumption
To reference a package in your local projects:
1. **Source Reference (Local Workspace)**: Add a project reference pointing to the project file in your workspace:
   ```bash
   dotnet add reference <path-to-d4rklib-project-csproj>
   ```
2. **Package Reference**: Alternatively, consume pre-compiled packages directly via NuGet or GitHub Packages.

---

## ⚡ Design Philosophy

All libraries in the **D4RKLib** ecosystem adhere to three core pillars:
1. **Developer Ergonomics**: Intuitive fluent APIs, builders, and extensibility points that let you write less boilerplate code.
2. **Performance-First**: Minimal memory allocations, async/await everywhere, and direct P/Invoke calls to bypass heavy wrappers when working with system APIs.
3. **Decoupled & Composable**: No monolithic dependencies. You only import and pay for what you actually use.

---

## 🛡️ License

This suite is licensed under the **MIT License**. You are free to modify, distribute, and use it in both open-source and commercial applications.

> Copyright © 2026 Paul Hayden (D4RKLib)
