# MN-ARCH-001 — Core Architecture Specification

## Metadata

- ID: MN-ARCH-001
- Title: Core Architecture Specification
- Version: 0.1.0
- Status: Draft
- Repository: med-nykuto-core
- Scope: architecture of the Core repository

## 1. Mission

Med Nykuto Core exists to be the source of truth for the Med Nykuto project.

It defines how the platform teaches, evaluates, organizes medical knowledge, validates questions and evolves over time.

The Core is not the final application. It is the reference system used by the application.

## 2. What belongs in the Core

The Core may contain:

- project constitution;
- architecture specifications;
- pedagogical rules;
- medical organization standards;
- question creation rules;
- quality control rules;
- AI behavior rules;
- templates;
- playbooks;
- decision records;
- study handoffs and historical notes.

## 3. What does not belong in the Core

The Core should not contain:

- production application code;
- unvalidated large question banks;
- random temporary files;
- duplicate versions without purpose;
- visual assets that should live in an assets repository;
- private credentials or secrets.

## 4. Main components

The repository is organized into responsibility areas:

```text
constitution/      foundational principles
engines/           pedagogical, exam, AI and quality models
pedagogy/          rules for learning and question design
medical-engine/    medical knowledge structure
prompts/           reusable AI instructions
templates/         standard file formats
playbooks/         operational procedures
decisions/         architecture decision records
study-sessions/    temporary or historical learning handoffs
docs/              architecture and repository documentation
archive/           deprecated material
```

## 5. Dependency rule

A lower-level document may depend on a higher-level document, but not the opposite.

Recommended order:

```text
Constitution
↓
Architecture
↓
Engines
↓
Pedagogy and Medical Engine
↓
Templates and Playbooks
↓
Site implementation
```

The site must follow the Core. The Core must not depend on the site implementation.

## 6. Document lifecycle

Each official document should move through these states:

```text
Draft → Review → Stable → Deprecated
```

- Draft: being written.
- Review: ready for correction.
- Stable: accepted as reference.
- Deprecated: replaced but kept for history.

## 7. Idea lifecycle

Every important idea follows this path:

```text
Idea → Discussion → Decision → Core document → Implementation → Validation
```

An idea should not become a site feature before its rule is clear in the Core.

## 8. Repository rule

The repository must remain navigable. A new contributor should understand the project by reading:

1. README.md
2. docs/CORE_ARCHITECTURE.md
3. constitution/med-nykuto-constitution.md
4. relevant engine documents

## 9. Immediate next steps

- Create the Constitution.
- Create the official glossary.
- Create the Professor Engine.
- Create the Question Engine.
- Convert old handoffs into organized study-session files.
