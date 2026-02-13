### OpenAppClaw Build
### The AI App Store Factory
<p align="center">
<picture>
<source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Xtact/open-app-claw/refs/heads/main/docs/assets/OpenAppClaw.PNG"> <img src="https://raw.githubusercontent.com/Xtact/open-app-claw/refs/heads/main/docs/assets/OpenAppClaw.PNG") alt="OpenAppClaw Build" width="500">
</picture>
</p>
<p align="center">
<strong>PROMPT. BUILD. SHIP. REPEAT.</strong>
</p>
<p align="center">
<a href="https://github.com/openclaw/openappclaw-build/actions"><img src="https://img.shields.io/badge/Build-Passing-00f2ff?style=for-the-badge&logo=githubactions&logoColor=black" alt="Build Status"></a>
<a href="https://github.com/openclaw/openappclaw-build/releases"><img src="https://img.shields.io/badge/Version-2.0.0-4c00ff?style=for-the-badge&logo=semver&logoColor=white" alt="Release"></a>
<a href="https://discord.gg/clawd"><img src="https://img.shields.io/badge/Discord-Join_The_Crew-5865F2?style=for-the-badge&logo=discord&logoColor=white" alt="Discord"></a>
<a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-blueviolet.svg?style=for-the-badge" alt="MIT License"></a>
</p>

<strong> OpenAppClaw Build - The World's First Agentic App Factory. </strong> 
OpenAppClaw Build allows you to build, test, sign, and submit REAL native applications to the Apple App Store and Google Play Store from any operating system (Windows, Linux, macOS).
Powered by the OpenClaw Agentic Platform, this tool eliminates the single biggest barrier in mobile development: The Apple Ecosystem Wall. You no longer need to own a Mac, learn Xcode, or wrestle with Provisioning Profiles to ship an iOS app. Your AI Agent handles the code, the compilation, and the compliance.
Website · Docs · Showcase · Getting Started · Discord
# OpenAppClaw Build

**The World's First Agentic App Factory.**

OpenAppClaw Build allows you to build, test, sign, and submit **REAL** native applications to the Apple App Store and Google Play Store from any operating system (Windows, Linux, macOS).

Powered by the **OpenClaw Agentic Platform**, this tool eliminates the single biggest barrier in mobile development: **The Apple Ecosystem Wall**. You no longer need to own a Mac, learn Xcode, or wrestle with Provisioning Profiles to ship an iOS app. Your AI Agent handles the code, the compilation, and the compliance.

[Website](#) · [Docs](#) · [Showcase](#) · [Getting Started](#) · [Discord](#)

---

## 🚀 Why OpenAppClaw Build?

Developing mobile apps is hard. Releasing them is harder. OpenAppClaw Build solves the "Last Mile" problem of mobile development.

| The Old Way (Pain) 😫 | The OpenAppClaw Way (Power) ⚡ |
| :--- | :--- |
| Buy a $2,000 MacBook just to compile iOS apps. | Build on Windows/Linux using our headless agentic cloud containers. |
| Spend days fighting Provisioning Profiles & Certs. | **Auto-Signing:** The Agent generates and manages keys instantly. |
| Manually upload binaries & screenshots to Connect. | **One-Prompt Submission:** "Ship v1.2 to TestFlight" — done. |
| Context switching between IDE, Browser, and Terminal. | **Unified Control Plane:** Chat with your builder in Slack, Discord, or Terminal. |

---

## 📦 Features

### 🤖 The Builder Agent
Your personal DevOps engineer. It doesn't just write code; it understands the build pipeline.
* **Scaffold Instantly:** "Create a React Native crypto wallet app with dark mode."
* **Fix Bugs:** "The build failed on Android linting. Fix it and retry."
* **Asset Generation:** Generates app icons, splash screens, and store screenshots automatically using integrated diffusion models.

### 🍎 iOS Compilation on Windows/Linux
OpenAppClaw Build abstracts the OS layer.
* **Headless Runners:** Uses ephemeral, headless macOS runners (or local Docker containers for Android) to perform the heavy lifting.
* **Zero-Config Signing:** The agent talks directly to the Apple Developer API to fetch certificates.

### 🚢 Store Command Center
Direct integration with App Store Connect and Google Play Console.
* **Metadata Management:** The Agent writes your description, keywords, and release notes based on the git commit history.
* **Compliance Check:** Pre-scans your app for common rejection triggers (private APIs, broken links) before uploading.

---

## 🛠️ Quick Start

**Prerequisites:** Node ≥22. No Xcode required.

### 1. Install the CLI
```bash
npm install -g openappclaw-build@latest
# or: pnpm add -g openappclaw-build

### 2. Onboard & Connect Accounts
The wizard will securely link your Apple Developer and Google Play Console credentials to your local keychain.
```bash
openappclaw onboard --type builder

### 3. Initialize a Project
# Create a new project directory
```bash
mkdir my-dream-app && cd my-dream-app

# Ask the agent to scaffold the base
openappclaw agent --task "Scaffold a fitness tracking app using React Native and Expo. Include a pedometer feature."

### 4. Build & Ship
The magic command. This bundles the app, signs it, and uploads it to TestFlight and Internal Testing track.
```bash
openappclaw ship --target all --track beta

### 🧠 The Architecture
OpenAppClaw Build sits on top of the core OpenClaw Gateway, utilizing specialized Worker Nodes for compilation.
'''mermaid
graph TD
    User[User (Windows/Linux)] -->|Prompt: 'Ship it'| Agent[OpenAppClaw Agent]
    Agent -->|Code Gen| LocalRepo[Local Repository]
    Agent -->|Orchestration| CloudBuilder[Headless Build Runners]
    
    CloudBuilder -->|IPA/APK| Signer[Auto-Signer Module]
    Signer -->|Signed Binary| StoreBot[Store Submission Bot]
    
    StoreBot -->|Upload| Apple[App Store Connect]
    StoreBot -->|Upload| Google[Google Play Console]

### 💬 Supported Channels
Interact with your build agent where you work. Receive build notifications and approve releases directly in:
• Slack / Discord / Teams: "Build https://www.google.com/search?q=%23402 is ready for review. [Download Link]. Approve upload to Production?"
• VS Code Extension: Watch the build logs stream in real-time.
### 🧩 Supported Frameworks
The Builder Agent is trained on the latest documentation for:
• React Native (Expo & CLI)
• Flutter
• SwiftUI (via headless runners)
• Kotlin/Jetpack Compose
• Ionic / Capacitor
🔐 Security & Privacy
We know your signing keys are sensitive.
• Local-First Keys: Your distribution certificates live on your machine or your private vault, never on our servers.
• Ephemeral Runners: Build environments are destroyed immediately after the artifact is generated.
• Audit Logs: Every action the Agent takes (modifying code, uploading binaries) is logged to build-audit.log.
### 📜 Roadmap
• [x] v1.0: Android Build & Submit (Local Docker)
• [x] v2.0: Remote iOS Building (Headless Runners)
• [ ] v2.5: AI-Generated App Store Screenshots & Video Previews
• [ ] v3.0: "Self-Healing" Builds – Agent automatically fixes compile errors without human intervention.
Star History
Community & Support
### Join the revolution. Stop configuring environments, start shipping apps.
• Discord: Join the #builders channel
• Twitter/X: @OpenAppClaw
• Issues: Report a bug
OpenAppClaw Build — The code is local. The reach is global.
