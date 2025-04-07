# Stardust Tunnel VPN 🚀✨

Welcome to **Stardust Tunnel**, a cross-platform and FREE VPN solution aimed at providing a seamless, modern desktop client experience without any paid BS subscriptions and registrations! This project is split across two main repositories (for now):

- [**Stardust Core**](https://github.com/Stardust-Tunnel-VPN/core) – The backend (FastAPI-based), responsible for core VPN functionality, connection management, and API services.  
- [**Stardust Desktop**](https://github.com/Stardust-Tunnel-VPN/stardust-desktop) – The Electron-based desktop application, providing a friendly UI to interact with the backend.

> **Note**: For now, this is an MVP (Minimal Viable Product). Some features may be incomplete or behave unpredictably. We appreciate your feedback and welcome contributions!

---

## Overview 💡

- **Electron Desktop App**  
  The desktop client is built with Electron, bundling the frontend (Vue + Vite + Tailwind) and launching the backend automatically on startup.

- **Stardust Core**  
  A FastAPI server compiled (e.g., via PyInstaller) into `main.exe` (Windows) or `main` (macOS/Linux). It handles VPN API calls (connect/disconnect, status checks, server listings) and implements evolving features like a Kill-Switch (currently in progress).

- **Request Interception**  
  The desktop intercepts requests beginning with `/api/v1` and redirects them to the local backend (`http://localhost:8000`). This avoids CORS issues and keeps all traffic local.

- **Cross-Platform Aspirations**  
  Targeting Windows, macOS, and Linux. Each platform’s binary is packaged and automatically launched by the Electron app.

- **Early MVP Warning**  
  - Some Windows functionality may be unstable (e.g., `rasdial` quirks, no Kill-Switch yet).
  - macOS Kill-Switch is available and works but still under refinement.

## Repositories 📂

### 1. Stardust Core
- **Language**: Python (FastAPI), TypeScript, Vue
- **Purpose**: Main VPN logic, server listings, connection status, frontend part, etc.
- **Kill-Switch**: Implemented for macOS, still a work in progress for other platforms.

### 2. Stardust Desktop
- **Framework**: Electron + Vue.js + Vite + Tailwind
- **Purpose**: Provide a native-like UI, intercept `/api/v1` calls, display server lists, manage connection states, etc.
- **Packaging**:  
  - Windows: `.exe` installer  
  - macOS: `.dmg`  installer (waiting for Apple developer license; For now, you can run it either locally via core repo or using `npm start` in stardust-desktop (you should do it in /electron folder)
  - (Future) Linux: `.AppImage` or similar

## Key Features 🌟

1. **Connect/Disconnect**  
   Easily connect to or disconnect from a chosen VPN server.
2. **Server List**  
   Fetch and display available VPN servers (sortable by country, etc.).
3. **Automatic Backend Launch**  
   No separate manual steps required; launching the desktop app also runs the local API.
4. **Custom Branding**  
   Branded icons and an application logo, labeled as “Stardust VPN Client.”
5. **Kill-Switch (WIP)**  
   - Partially implemented for macOS  
   - Windows kill-switch is **not** yet available
6. **Real-time Connection Status**  
   The UI refreshes to show whether you’re connected, disconnected, or encountering an error.

## Installation & Usage 🏃
Go to our **Stardust-Desktop** repository and just open the last relevant release for your OS (macOS/Windows). Usually, there is only an installer that you have to download and use!

## Known Limitations ⚠️

**Rasdial Instability**

On Windows, some connection steps may fail or behave erratically due to the chaotic nature of rasdial. We'll be working on this part soon.

## Kill-Switch
Not implemented on Windows yet; works for macOS.

## MVP State
Certain advanced features (VPN statistics, extended settings, polished UI/UX) are still under development.

## Contributing 🤝
We welcome Pull Requests, bug reports, and feature requests!

Issues: Report or track them on the core repo.

Pull Requests: Feel free to fork and submit PRs to either repository.

Suggestions: Start a discussion or open an issue. We value your input!

Enjoy using Stardust Tunnel VPN? Please ⭐ our repos and share your feedback!
Special thanks to everyone testing this MVP and helping us move toward a robust, user-friendly VPN client!

You can also thank us by supporting us on the platform buymeacoffee!
https://buymeacoffee.com/roman.rudyi
