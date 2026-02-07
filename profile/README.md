# D4RKLib

![.NET](https://img.shields.io/badge/.NET-9.0-512BD4?style=flat-square&logo=dotnet)
![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)
![Platform](https://img.shields.io/badge/Platform-Cross%20Platform-lightgrey?style=flat-square)
![Status](https://img.shields.io/badge/Status-Active%20Development-success?style=flat-square)

**D4RKLib** is a suite of high-performance, modular, and battle-tested .NET 9 libraries designed to accelerate modern development.

Built with a focus on **developer ergonomics** and **raw speed**, these packages provide the building blocks for professional-grade applications. Whether you are building complex desktop tooling, background services, or real-time data utilities, D4RKLib delivers functionality without the bloat.

---

## 🌐 Networking & Connectivity

| Package | Status | Description |
| :--- | :--- | :--- |
| [`D4RKLib.Networking.Subscriptions`](https://github.com/D4RKLib/D4RKLib.Networking.Subscriptions) | ![New](https://img.shields.io/badge/NEW-brightgreen?style=flat-square) | **High-performance Pub/Sub engine.** Features O(1) routing, MQTT-style wildcards (`*`, `**`), and retained message support. |
| [`D4RKLib.Networking.WebSockets`](https://github.com/D4RKLib/D4RKLib.Networking.WebSockets) | ![Stable](https://img.shields.io/badge/Stable-blue?style=flat-square) | **Robust WebSocket client/server.** Features auto-reconnect, keep-alive interceptors, and authentication pipelines. |

## 💾 Data & Logic

| Package | Status | Description |
| :--- | :--- | :--- |
| [`D4RKLib.Data.MySQL`](https://github.com/D4RKLib/D4RKLib.Data.MySQL) | ![Stable](https://img.shields.io/badge/Stable-blue?style=flat-square) | **Async-first ORM.** Supports code-first schema syncing, JSON columns, and unit-of-work transactions. |
| [`D4RKLib.CommandFlow`](https://github.com/D4RKLib/D4RKLib.CommandFlow) | ![Stable](https://img.shields.io/badge/Stable-blue?style=flat-square) | **Command routing system.** Lightweight dispatching with metadata-aware filtering and execution. |
| [`D4RKLib.CommandMessages`](https://github.com/D4RKLib/D4RKLib.CommandMessages) | ![Stable](https://img.shields.io/badge/Stable-blue?style=flat-square) | **Protocol definitions.** Structured encoding/decoding for command messages with rich metadata. |

## 🖥️ UI & Input

| Package | Status | Description |
| :--- | :--- | :--- |
| [`D4RKLib.Input.KeyboardShortcuts`](https://github.com/D4RKLib/D4RKLib.Input.KeyboardShortcuts) | ![Stable](https://img.shields.io/badge/Stable-blue?style=flat-square) | **Global hook system.** Advanced keyboard monitoring supporting complex modifier combinations. |
| [`D4RKLib.InputBox`](https://github.com/D4RKLib/D4RKLib.InputBox) | ![Stable](https://img.shields.io/badge/Stable-blue?style=flat-square) | **Modern input dialogs.** Fully customizable WinForms input with validation, regex support, and dark mode. |
| [`D4RKLib.DropKit`](https://github.com/D4RKLib/D4RKLib.DropKit) | ![Stable](https://img.shields.io/badge/Stable-blue?style=flat-square) | **Fluent Drag-and-Drop.** Simplifies file previews, export, tagging, and cross-app transfers. |

---

## 🌱 Philosophy

* **🧱 Modular** — Decoupled architecture; import only what you need.
* **⚡ Fast** — Designed for .NET 9 with zero-allocation paths where possible.
* **⚙️ Modern** — Fully asynchronous (`Task`/`Await`) and Dependency Injection (DI) ready.
* **🛡️ Robust** — Extensive error handling and thread-safe implementations.

---

## 📌 Licensing

All libraries in the **D4RKLib** suite are released under the **MIT License**.
You are free to use them in personal and commercial projects, provided attribution is given.

> Copyright © 2026 Paul Hayden (D4RKLib)

---

## 🤝 Ecosystem

These libraries are currently maintained as part of the private D4RKLib ecosystem, with public releases available via **GitHub Releases**.

* ⭐ **Star** the repositories to show support.
* 🐛 **Report** issues via the tracker.
* 🔄 **Check** back frequently for updates.

**Built for developers, by developers.**
