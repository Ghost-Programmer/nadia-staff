# Nadia Staff Repository

Official public repository of staff specialist personas for the **Nadia AI** assistant platform.

---

## 📋 Overview

Nadia is an extensible cognitive AI assistant architecture powered by specialized staff personas. Each staff persona brings domain-specific system prompts, tool permissions, and procedural skill directives.

This repository serves as the central distribution hub for staff personas that can be discovered, downloaded, and installed directly inside Nadia's **Staff Panel** UI.

---

## 📂 Repository Structure

Staff personas are organized into self-contained directories under the `./staff/` directory:

```
nadia-staff/
├── README.md
└── staff/
    ├── TEMPLATE.md                     # Base template and documentation for authoring staff personas
    ├── 3D Printer/
    │   └── STAFF.md                    # Bambu 3D printer fleet management and diagnostics
    ├── Journalist/
    │   └── STAFF.md                    # Investigative journalism and WordPress publishing
    ├── Network Engineer/
    │   └── STAFF.md                    # Network topology mapping, Nmap, and IoT hardware
    ├── Personal Assistant/
    │   └── STAFF.md                    # Scheduling, email intake, and executive briefings
    ├── Product Manager/
    │   └── STAFF.md                    # Trending app teardowns, PRDs, and Kanban orchestration
    ├── Quality Engineer/
    │   └── STAFF.md                    # Test strategies, automation suites, and defect tracking
    ├── Researcher/
    │   └── STAFF.md                    # Multi-source web research, dossier synthesis, and fact extraction
    ├── Scoutmaster/
    │   └── STAFF.md                    # Wilderness navigation, AllTrails logistics, and safety checks
    ├── Software Architect/
    │   └── STAFF.md                    # System architecture, codebase analysis, and whiteboards
    ├── Software Engineer/
    │   └── STAFF.md                    # Full-stack implementation (Android, JavaFX, Angular, Spring Boot)
    ├── Stock Broker/
    │   └── STAFF.md                    # Financial markets, ticker sweeps, and earnings analysis
    └── UI Designer/
        └── STAFF.md                    # Visual design tokens, Material 3, and whiteboard wireframing
```

---

## 🧑‍💼 Available Staff Personas

| Staff Persona | Specialization | Core Directives & Workflows |
| :--- | :--- | :--- |
| **Product Manager** | Product Strategy & Discovery | Trending app/game discovery, teardowns, Product Specifications (PRD/App Spec) in `doc/spec/`, user stories, MoSCoW scoping, Kanban backlog creation. |
| **UI Designer** | UI/UX & Visual Design | Visual `.whiteboard` screen wireframes, splash screens with Miller Software Solutions LLC notice, Material 3 tokens, JavaFX CSS, and Angular layouts. |
| **Software Architect** | System Architecture | Architectural Design Documents (ADDs in `doc/add/`), multi-tier `.whiteboard` architecture diagrams, GitHub repository ingestion, and static analysis. |
| **Software Engineer** | Full-Stack Implementation | Native Android, JavaFX, Angular, and Java & Spring Boot feature implementation, sandbox build verification, and clean Antigravity code generation. |
| **Quality Engineer** | Test Strategy & QA | Test plan authoring in `doc/test/`, automated test suites (`gradle test`, `mvn test`, `npm test`), defect triage, and Kanban verification. |
| **Personal Assistant** | Executive Coordination | Morning briefings, Gmail IMAP IDLE push intake, Google Workspace (`gws`), calendar scheduling, and reminder alerts. |
| **Journalist** | Investigative Journalism | AP-style articles, living story updates, WordPress publishing, competitor blog monitoring, and fact synthesis. |
| **Network Engineer** | LAN Infrastructure & IoT | Nmap network sweeps, MAC vendor lookup, interactive topology mapping, printer management, and Philips Hue lighting control. |
| **3D Printer** | Additive Manufacturing | Bambu MQTT telemetry sweeps, live chamber camera streaming, and cached HMS error diagnostics. |
| **Researcher** | Deep Web Research | Multi-source web research, background dossier synthesis, academic citations, and knowledge extraction. |
| **Stock Broker** | Equities & Financial Markets | Market sweeps, stock ticker quotes, valuation metrics, and scheduled earnings briefs. |
| **Scoutmaster** | Outdoor Logistics & Navigation | AllTrails trail routing, elevation analysis, weather safety checks, and wilderness equipment checklists. |

---

## 🛠️ STAFF.md Format Specification

Every staff persona directory MUST contain a `STAFF.md` file featuring a YAML frontmatter header followed by structured markdown instructions.

```yaml
---
name: Persona Display Name
description: Brief description of the specialist's core responsibilities and expertise.
tools: [toolA, toolB, toolC]
skills: [SkillOne, SkillTwo, SkillThree]
---

# STAFF PROFILE & ACTIVE EXECUTION DIRECTIVE

## 1. Identity and Context
- **Identity**: Description of the persona's role and tone.
- **Tone & Demeanor**: Communication style.
- **Core Goals**: Primary goals and workflows.

## 2. Required Skills & Procedural Modules
- Explanations of required skills and when to invoke them.

## 3. Tool Permissions & Spring AI Bindings
- Explicit list and guidelines for permitted tools.

## 4. Workflows & Operational Directives
- Step-by-step procedures for standard tasks.

## 5. Conversational Delegation & Inter-Staff Handoff
- Directives for delegating to other staff via `@<StaffName>` tags.
```

---

## 📥 Installing into Nadia

In the **Nadia** desktop client:
1. Open the **Staff** panel on the left sidebar.
2. Click **📥 Install Staff from GitHub**.
3. Point to this repository (`https://github.com/Ghost-Programmer/nadia-staff`) or any compatible fork.
4. Select the desired staff personas to install or update.
5. Click **Install Selected**. Nadia will automatically persist the files into `./staff/` and dynamically reload the active staff pool without restarting.

---

## 📄 License & Credits

Copyright (c) 2026 Miller Software Solutions LLC. All rights reserved.
