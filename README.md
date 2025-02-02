<div align="center">

# 🧠 Roo Code Memory Bank

**Persistent Project Context for AI-Assisted Development**

[![VS Code Extension](https://img.shields.io/badge/VS%20Code-Extension-blue.svg)](https://github.com/RooVetGit/Roo-Code)
[![GitHub](https://img.shields.io/badge/View%20on-GitHub-lightgrey.svg)](https://github.com/GreatScottyMac/roo-code-memory-bank)

</div>

## 🎯 Overview

Roo Code Memory Bank solves a critical challenge in AI-assisted development: **maintaining context across sessions**. By providing a structured memory system integrated with VS Code, it ensures your AI assistant maintains a deep understanding of your project across sessions.

### Key Components

```mermaid
graph LR
    A[Memory Bank] --> B[Core Files]
    A --> C[Mode Rules]
    A --> D[VS Code UI]
    B --> E[Project Context]
    B --> F[Decisions]
    B --> G[Progress]
    C --> H[Architect]
    C --> I[Code]
    C --> J[Ask]
```

- 🧠 **Memory Bank**: Persistent storage for project knowledge
- 📋 **Mode Rules**: YAML-based behavior configuration
- 🔧 **VS Code Integration**: Seamless development experience

## 🚀 Quick Start

### 1. Configure Custom Instructions

#### a. Copy Rule Files
Download and copy these files to your project's **root** directory:

| Mode | Rule File | Purpose |
|------|-----------|----------|
| Code | [`.clinerules-code`](https://github.com/GreatScottyMac/roo-code-memory-bank/blob/main/.clinerules-code) | Implementation and coding tasks |
| Architect | [`.clinerules-architect`](https://github.com/GreatScottyMac/roo-code-memory-bank/blob/main/.clinerules-architect) | System design and architecture |
| Ask | [`.clinerules-ask`](https://github.com/GreatScottyMac/roo-code-memory-bank/blob/main/.clinerules-ask) | Information and assistance |

#### b. Configure VS Code Settings
> ⚠️ **Important**: Leave the "Custom Instructions" text boxes **empty** in VS Code settings (Roo Code Prompts section)

<details>
<summary>📷 View Settings Screenshot</summary>

![Roo Code Settings](https://github.com/GreatScottyMac/roo-code-memory-bank/blob/main/promt-settings-page.jpg)
</details>

### 2. Initialize Memory Bank

1. Switch to **Architect** or **Code** mode in Roo Code chat
2. Send a message (e.g., "hello")
3. Roo will automatically:
   - 🔍 Scan for `memory-bank/` directory
   - 📁 Create it if missing (with your approval)
   - 📝 Initialize core files
   - 🚦 Provide next steps

<details>
<summary>💡 Pro Tip: Project Brief</summary>

Create a `projectBrief.md` in your project root **before** initialization to give Roo immediate project context.
</details>

## 📚 Memory Bank Structure

```mermaid
graph TD
    MB[memory-bank/] --> AC[activeContext.md]
    MB --> DL[decisionLog.md]
    MB --> PC[productContext.md]
    MB --> PR[progress.md]
    MB --> PB[projectBrief.md]
    MB --> SP[systemPatterns.md]
    
    subgraph Core Files
        AC[Current Session State]
        DL[Technical Decisions]
        PC[Project Overview]
        PR[Progress Tracking]
    end
    
    subgraph Optional
        PB[Project Brief]
        SP[System Patterns]
    end
```

<details>
<summary>📖 View File Descriptions</summary>

| File | Purpose |
|------|----------|
| `activeContext.md` | Tracks current goals, decisions, and session state |
| `decisionLog.md` | Records architectural choices and their rationale |
| `productContext.md` | Maintains high-level project context and knowledge |
| `progress.md` | Documents completed work and upcoming tasks |
| `projectBrief.md` | Contains initial project requirements (optional) |
| `systemPatterns.md` | Documents recurring patterns and standards |

</details>

## ✨ Features

### 🧠 Persistent Context
- Remembers project details across sessions
- Maintains consistent understanding of your codebase
- Tracks decisions and their rationale

### 🔄 Smart Workflows
```mermaid
graph LR
    A[Architect Mode] -->|System Design| B[Memory Bank]
    C[Code Mode] -->|Implementation| B
    D[Ask Mode] -->|Information| B
    B -->|Context| A
    B -->|Context| C
    B -->|Context| D
```
- Mode-based operation for specialized tasks
- Automatic context switching
- Project-specific customization via rules

### 📊 Knowledge Management
- Structured documentation with clear purposes
- Technical decision tracking with rationale
- Automated progress monitoring
- Cross-referenced project knowledge

## 💡 Pro Tips

### Multiple Projects
```mermaid
graph TD
    A[Workspace] --> B[Project 1]
    A --> C[Project 2]
    B --> D[memory-bank/]
    C --> E[memory-bank/]
    D --> F[Automatic Detection]
    E --> F
```
Roo automatically handles multiple Memory Banks in your workspace!

### Session Management
> 💾 Use "UMB" or "update memory bank" in chat to save context before ending sessions

## 📖 Documentation

- [Developer Deep Dive](https://github.com/GreatScottyMac/roo-code-memory-bank/blob/main/developer-primer.md)
- [Update Log](https://github.com/GreatScottyMac/roo-code-memory-bank/blob/main/updates.md)

---

<div align="center">

**[View on GitHub](https://github.com/GreatScottyMac/roo-code-memory-bank) • [Report Issues](https://github.com/GreatScottyMac/roo-code-memory-bank/issues) • [Get Roo Code](https://github.com/RooVetGit/Roo-Code)**

</div>
=======
# Roo Code Memory Bank

## Maintain Project Context Across Sessions and Memory Resets

This repository contains the Memory Bank for the Roo Code project, designed to maintain project context across sessions and memory resets. 

**Documentation**

- [User Guide](docs/user-guide.txt): Comprehensive guide on using the Roo Code Memory Bank system.

**Custom Instructions**

- [Custom Instructions](custom-instructions/): Directory containing custom instructions for different modes (Architect, Code, Ask) to enhance Roo Code's functionality within this project.

**Key Features**

- **Persistent Project Context:** Ensures Roo Code retains project knowledge across sessions.
- **Organized Documentation:** User guide and instruction modules for easy reference.
- **GitHub Synchronization:** настроено для синхронизации только необходимых файлов, таких как документация и пользовательские инструкции.

**Getting Started**

Refer to the [User Guide](docs/user-guide.txt) for detailed setup and usage instructions.

**Repository Structure**

```
roo-code-memory-bank/
├── custom-instructions/
│   ├── global-instructions.md
│   ├── mode-arch.md
│   ├── mode-ask.md
│   ├── mode-code.md
│   ├── role-arch.md
│   ├── role-ask.md
│   └── role-code.md
├── docs/
│   └── user-guide.txt
├── memory-bank/ # Excluded from Git (local memory bank)
└── .gitignore 
```

**License**

[License information here]
