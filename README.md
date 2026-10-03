# AI Project — OS Hardening

> Enterprise-grade cross-platform security hardening for Windows and Linux, with an AI-assisted configuration layer.

[![Status](https://img.shields.io/badge/status-scaffold-yellow)]()

## Overview

This project automates the application of security configurations for Windows
and Linux systems following industry best practices and compliance frameworks
(CIS, NIST). The goal is a tool that:

- **Hardens automatically** — applies secure baseline configurations across Windows 10/11, Ubuntu 20.04+, CentOS 7+
- **Explains itself** — an AI assistant layer that translates hardening decisions into plain language
- **Reports compliance** — before/after state tracking with PDF, HTML, and JSON reports
- **Rolls back safely** — full backup and restore of every changed configuration

## Status

> ⚠️ **Scaffold** — this repository is the planning home for the AI-assisted
> hardening project. The core hardening engine is implemented and maintained
> in the companion repository below.

## Canonical implementation

The working hardening engine lives at
**[scar8969/PS232_secutity-hard](https://github.com/scar8969/PS232_secutity-hard)**:

- Windows (10/11), Ubuntu, CentOS hardening modules
- Basic / Moderate / Strict security levels
- Backup & rollback, PDF/HTML/JSON reports
- CLI + GUI interfaces

This repo tracks the AI-assistant layer (natural-language hardening guidance,
explainable compliance reports) on top of that engine.

## Planned architecture

```
┌─────────────┐   ┌──────────────────┐   ┌─────────────────────┐
│  User asks  │──▶│  AI assistant    │──▶│  Hardening engine   │
│  "harden X" │   │  (LLM + rules)   │   │  (PS232, Windows/   │
└─────────────┘   └──────────────────┘   │   Linux modules)    │
                                          └─────────────────────┘
                                                │
                                                ▼
                                         Compliance report
                                         (PDF / HTML / JSON)
```

## License

MIT
