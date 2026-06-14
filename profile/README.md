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
├── ⚙️ Commands/        # Action routing, dispatching, and message contracts
├── 💾 Data/            # Databases (MySQL, SQLite) and object dirty-tracking
├── 🎨 Graphics/        # High-performance native pixel reading
├── ⌨️ Input/           # OS-level keyboard shortcut hooks
├── ☁️ Microsoft/       # Simplifies Microsoft Graph API integrations
├── 🌐 Networking/      # LAN discovery, REST/JWT, SSE, Pub/Sub, WebHost, WebSockets
├── 🤖 OpenAI/          # Fluent SDK for OpenAI API (Chat, Audio, Images, Tools)
└── 🖥️ UI/              # WinForms UI extensions (DropKit Drag/Drop, InputBox)
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

### 🎨 Graphics
Low-level screen reading and graphics manipulation.

| Package | GitHub Repository | Stability | Description |
| :--- | :--- | :--- | :--- |
| **D4RKLib.Graphics** | [`D4RKLib.Graphics`](https://github.com/D4RKlib/D4RKLib.Graphics) | ![Stable](https://img.shields.io/badge/Stable-blue?style=flat-square) | **High-speed pixel reader.** Fast screen pixel and region reading utilizing native `GDI32`/`USER32` P/Invokes to bypass managed GDI overhead. |

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
