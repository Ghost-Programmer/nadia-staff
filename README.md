# Nadia Staff Repository

Official public repository of staff specialist personas, scheduled `cron.json` automations, and domain `rag/` knowledge bases for the **Nadia AI** cognitive assistant platform.

---

## 📋 Overview

Nadia is an extensible cognitive AI assistant architecture powered by specialized staff personas. Each staff persona is packaged in a self-contained directory under `./staff/<StaffName>/` and can include:
- **`STAFF.md` (Required)**: Domain-specific system persona, operational workflows, Spring AI tool permissions, inter-staff `@<StaffName>` handoff rules, and procedural skill bindings (compatible with the open **[agentskills.io](https://agentskills.io)** standard).
- **`cron.json` (Optional)**: Recurring scheduled background prompts automatically registered with Nadia's `PromptSchedulerService` when the staff persona is installed or updated.
- **`rag/` (Optional)**: Domain reference documents (`.pdf`, `.md`, `.txt`) automatically chunked, embedded, and indexed into Nadia's vector store by `StaffRagIngestionService`.

This repository serves as the central distribution hub for staff personas that can be discovered, downloaded, and installed directly inside Nadia's **Staff Panel** UI (**Tools ➔ 🧑‍💼 Download & Install Staff...**).

---

## 📂 Repository Structure

Staff personas are organized into self-contained directories under the `./staff/` hierarchy:

```text
nadia-staff/
├── README.md
└── staff/
    ├── TEMPLATE.md                         # Official template & authoring guide for STAFF.md personas
    ├── 3D Printer/
    │   ├── STAFF.md                        # Bambu 3D printer fleet control, 1-min camera defect inspection & HMS diagnostics
    │   └── cron.json                       # Daily 07:00 AM printer queue & readiness check (recurring-c8f921b7)
    ├── Flight Tracker/
    │   └── STAFF.md                        # Single-target live aircraft (ADS-B/FAA) & satellite tracking with auto-pan World Map
    ├── Genealogist/
    │   └── STAFF.md                        # Lineage tracking, GEDCOM 5.5/7.0 parsing, kinship/DNA cM, and record matching
    ├── Journalist/
    │   └── STAFF.md                        # Investigative journalism, living stories, and WordPress publishing
    ├── Network Engineer/
    │   ├── STAFF.md                        # Zero-trust network authorization, Nmap topology mapping, and IoT hardware
    │   └── cron.json                       # Periodic LAN topology & infrastructure health sweeps
    ├── Personal Assistant/
    │   ├── STAFF.md                        # Executive scheduling, Gmail IMAP IDLE intake (with draft de-duplication), and briefings
    │   └── cron.json                       # Morning briefing preparation, email triage, and blog watcher schedules
    ├── Product Manager/
    │   ├── STAFF.md                        # Trending app/game teardowns, PRDs (doc/spec/), and Kanban orchestration
    │   └── cron.json                       # Nightly 02:00 AM trending product discovery & teardown (recurring-4d82e19f)
    ├── Quality Engineer/
    │   └── STAFF.md                        # Test strategies (doc/test/), automated test suites, and Kanban defect triage
    ├── Researcher/
    │   └── STAFF.md                        # Multi-source deep web research, academic citations, and dossier synthesis
    ├── Scoutmaster/
    │   ├── STAFF.md                        # Scouting America advancement roadmaps, AllTrails routing & Troop.whiteboard sync
    │   ├── cron.json                       # Weekly Sunday 04:20 AM Google Drive report sync & Troop plan (recurring-e56ef7c3)
    │   └── rag/                            # 142 BSA Merit Badge pamphlets, Scoutmaster Handbook & Guide to Advancement PDFs
    ├── Software Architect/
    │   └── STAFF.md                        # Architectural Design Documents (doc/add/), codebase analysis & multi-tier whiteboards
    ├── Software Engineer/
    │   └── STAFF.md                        # Full-stack implementation (Android, JavaFX, Angular, Spring Boot) & Antigravity CLI
    ├── Stock Broker/
    │   ├── STAFF.md                        # Financial markets, equity ticker sweeps, valuation metrics & portfolio tracking
    │   └── cron.json                       # Scheduled market open/close sweeps and earnings briefs
    └── UI Designer/
        └── STAFF.md                        # Material 3 design tokens, JavaFX CSS, Angular layouts & .whiteboard wireframes
```

---

## 🧑‍💼 Available Staff Personas

| Staff Persona | Specialization | Bundled Assets | Core Directives & Workflows |
| :--- | :--- | :--- | :--- |
| **3D Printer** | Additive Manufacturing & Visual QA | `STAFF.md`, `cron.json` | Bambu Lab MQTT telemetry sweeps, live chamber camera streaming (`cam-bambu-<ip>`), **1-minute live print photo inspection** for 4 critical defects (*Clogged/Jammed Extruder*, *Under-Extrusion & Gaps*, *Stringing & Oozing*, *First-Layer Detachment & Warping*) with **automatic print pause (`pausePrintJob`) and Slack `#alert` notification**, cached HMS error diagnostics, and zero-trust network guard. |
| **Flight Tracker** | Air Traffic & Orbital Tracking | `STAFF.md` | Real-time single-target aircraft (OpenSky ADS-B + FAA Civil Aviation Registry lookup) and orbital satellite (N2YO) tracking on the World Map, viewport boundary monitoring with 18% edge-triggered smooth `panTo` auto-recentering, and live flight intelligence briefings. |
| **Genealogist** | Lineage & Family History | `STAFF.md` | GEDCOM 5.5/7.0 tree parsing, semantic RAG fact ingestion, kinship & MRCA calculations, shared DNA cM relationship probability estimates, historical record matching (Census, SSDI, Find A Grave), and Genealogical Proof Standard (GPS) dossiers. |
| **Journalist** | Investigative Journalism | `STAFF.md` | AP-style article drafting, living story synthesis, multi-site WordPress publishing, and competitor blog/RSS monitoring. |
| **Network Engineer** | LAN Infrastructure & Zero-Trust Security | `STAFF.md`, `cron.json` | Zero-trust network authorization (`checkNetworkApproval`, `approveCurrentNetwork`, `listApprovedNetworks`), Nmap subnet discovery, MAC vendor resolution, interactive topology mapping, 2D/3D printer discovery, and Philips Hue lighting control. |
| **Personal Assistant** | Executive Coordination & Comms | `STAFF.md`, `cron.json` | Daily executive morning briefings, Gmail IMAP IDLE push intake with mandatory `Draft_Created` label anti-duplication checks, Google Workspace (`gws`) calendar/tasks/docs/drive management, tech blog curation, and pre-meeting alarms. |
| **Product Manager** | Product Strategy & Discovery | `STAFF.md`, `cron.json` | Nightly trending app/game discovery, competitive teardowns, Product Specifications (PRD/App Spec) in `doc/spec/`, user stories, MoSCoW MVP scoping, and Kanban workflow initiation. |
| **Quality Engineer** | Test Strategy & QA Automation | `STAFF.md` | Test plan authoring in `doc/test/`, automated test suite execution (`gradle test`, `mvn test`, `npm test`), defect reporting, and Kanban verification triage. |
| **Researcher** | Deep Web & Literature Research | `STAFF.md` | Multi-source web research, academic literature surveys, background dossier compilation (`session/brain/`), and verified citation synthesis. |
| **Scoutmaster** | Scouting Advancement & Outdoor Logistics | `STAFF.md`, `cron.json`, `rag/` (142 PDFs) | Google Drive troop report ingestion (`My Drive > Troop 63 > Assistant`), individual scout advancement roadmaps to Eagle Scout, master troop advancement plan in `Scout_Troop`, interactive `Troop.whiteboard` canvas synchronization, AllTrails trail matching, and local RAG over 142 BSA Merit Badge & Advancement guides. |
| **Software Architect** | System Architecture & Whiteboards | `STAFF.md` | Architectural Design Documents (ADDs in `doc/add/`), multi-tier `.whiteboard` architecture diagrams, GitHub repository ingestion, Antigravity (`agy`) static analysis, and Git post-commit architectural reviews. |
| **Software Engineer** | Full-Stack Software Engineering | `STAFF.md` | Full-stack feature implementation across Android, JavaFX, Angular, and Java & Spring Boot (`ai.nadia` package standard), Docker container management, sandbox build verification, and Antigravity (`agy`) code generation. |
| **Stock Broker** | Equities & Financial Markets | `STAFF.md`, `cron.json` | Real-time stock ticker quotes, technical & fundamental valuation metrics, watchlist tracking, and scheduled market briefings. |
| **UI Designer** | UI/UX & Visual Wireframing | `STAFF.md` | Visual `.whiteboard` screen wireframing (`<projectName>-ui-design.whiteboard`), mandatory splash screen with Miller Software Solutions LLC credit and copyright notice, Material 3 tokens, modern JavaFX CSS, and Angular layouts. |

---

## 🛠️ Staff Package Specification (`STAFF.md`, `cron.json`, `rag/`)

### 1. `STAFF.md` Format Specification

Every staff persona directory MUST contain a `STAFF.md` file featuring a YAML frontmatter header followed by structured Markdown instructions (see [`staff/TEMPLATE.md`](staff/TEMPLATE.md) for the complete template):

```yaml
---
name: Persona Display Name
description: Concise description of the specialist's persona, core domain expertise, and operational responsibilities.
skills: [SkillOne, SkillTwo, BriefSkill, MemorySkill, DateTimeSkill, GeneralSystemSkill, HandoffSkill]
tools: [toolA, toolB, storeBriefEntry, appendBriefEntry, getBriefEntries, searchMemory, saveMemory, updateMemory, executeSessionCommand, getCurrentDateTime]
---

# STAFF PROFILE & ACTIVE EXECUTION DIRECTIVE

## 1. Identity and Context
- **Identity**: Persona role, background, and domain authority.
- **Tone & Demeanor**: Communication style and personality traits.
- **Core Goal**: Primary autonomous objectives and quality standards.

## 2. Required Skills & Procedural Modules
- Table mapping required skills from `./skills/` (supports both `agentskills.io` kebab-case `name` slugs such as `brief` and `metadata.display-name` identifiers such as `BriefSkill`).

## 3. Automated Cron Coordination, Event Triggers & Local RAG Knowledge Base
- Documentation of bundled `cron.json` schedules, `rag/` reference documents, and outbound event triggers.

## 4. Core Operational Workflows & Expertise
- Step-by-step procedures for domain workflows, safety checks, and deliverable formatting.

## 5. Operational Protocols
- **5.1 The Prologue Protocol**: Merging system instructions, `agentskills.io` skill directives, `rag/` context, and `<episodic_memory>`.
- **5.2 The Heartbeat Protocol**: Parallel tool execution and step-by-step trajectory logging.
- **5.3 The Epilogue Protocol**: Supporting background fact extraction and brief/memory persistence.
- **5.4 Inter-Staff Chat Messaging & Collaborative Delegation**: Tagging `@<StaffName>` for real-time multi-agent turn exchange.

## 6. Critical Execution Rules
- Mandatory guardrails (no conversational filler, tool-driven execution, structured Markdown, zero-trust network compliance).
```

### 2. `cron.json` Format Specification (Optional)

A staff directory may include a `cron.json` array defining recurring scheduled tasks that Nadia's `PromptSchedulerService` loads automatically:

```json
[
  {
    "id": "recurring-example01",
    "name": "Daily Morning Domain Sweep",
    "cron": "0 7 * * *",
    "sessionId": "manual-job",
    "staffName": "Persona Display Name",
    "prompt": "## Immediate Execution Plan\n\nExecute the daily domain sweep and log findings via `storeBriefEntry`..."
  }
]
```

### 3. `rag/` Knowledge Base Directory (Optional)

Place domain PDFs, Markdown files, or text documents under `staff/<StaffName>/rag/`. When the staff persona is installed or updated via the Staff Installer, `StaffRagIngestionService` automatically extracts, chunks, and embeds the documents into Nadia's vector store scoped to that specialist.

---

## 📥 Installing into Nadia

In the **Nadia** desktop client:
1. Open the **Staff** panel on the left sidebar (or select **Tools ➔ 🧑‍💼 Download & Install Staff...**).
2. Click **📥 Install Staff from GitHub**.
3. Enter `https://github.com/Ghost-Programmer/nadia-staff` (default) or any compatible fork and click **🔍 Scan Repository**.
4. Select the desired staff personas to install or update.
5. Click **📥 Install Selected**. Nadia automatically writes `STAFF.md`, `cron.json`, and `rag/` files into `~/.nadia/staff/`, reloads scheduled cron jobs, ingests RAG documents, and refreshes the active staff pool without restarting.

---

## 📄 License & Credits

Copyright (c) 2026 Miller Software Solutions LLC. All rights reserved.
