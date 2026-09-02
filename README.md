# Augment Intent Properties 🔗

> Documenting interop rough edges between Augment Intent and Claude Code CLI — compiled for a clean, evidenced support report.

[![License: MIT](https://img.shields.io/badge/license-MIT-lightgrey?style=flat)](LICENSE)
[![Public Preview](https://img.shields.io/badge/%F0%9F%8C%90%20Public%20Preview-Available-brightgreen)](https://drasticstatic.github.io/augment-intent-properties-public-preview/) [![Synced via GitHub Actions](https://img.shields.io/badge/Synced%20via-GitHub%20Actions-blue)](https://github.com/drasticstatic/augment-intent-properties/actions/workflows/sync-public.yml) [![Built with Claude Code](https://img.shields.io/badge/Built%20with-Claude%20Code%20CLI-blueviolet)](https://code.claude.com/docs/en/overview) [![Status](https://img.shields.io/badge/Status-%F0%9F%94%A5%20Active%20Build-orange)](https://github.com/drasticstatic/augment-intent-properties)

---

**🌐 [Explore the Public Preview →](https://drasticstatic.github.io/augment-intent-properties-public-preview/)**

---

> 🔒 **Public mirror notice:** This repository is partially mirrored to a public preview via an automated GitHub Actions pipeline. The public version includes only sanitized, generalized findings. Internal file paths, error strings, screenshots, and other raw diagnostic material stay private.

---

## Table of Contents

- [👋 What This Is](#what-this-is)
- [🎯 The Goal](#the-goal)
- [🚀 Scope](#scope)
- [🏗️ Architecture](#architecture)
- [🤝 Collaboration](#collaboration)
- [📜 License](#license)

---

<a id="what-this-is"></a>
## 👋 What This Is

A compiled, evidence-based writeup of the interop gaps that show up when Augment Intent runs on Claude Code CLI as its underlying agent, instead of native Auggie — things like authentication/GitHub-connect friction, workspace-visibility quirks, and platform-level timeouts observed across real working sessions in this agent-fleet ecosystem. The goal is a clean report Augment's own team can act on, not a grievance list.

**Developer / builder:** Christopher Wilson (`drasticstatic`)
**AI agents:** Mystarch (Augment Intent) — original findings compilation · Alfred (Claude Code CLI) — repo scaffolding & public-preview lane

---

<a id="the-goal"></a>
## 🎯 The Goal

Turn scattered, session-by-session friction into a single well-evidenced report that Augment's support team can use to actually close the gap — plus, as non-blocking hoped-for outcomes, a clearer support channel and recovery of any token usage lost to the affected sessions.

---

<a id="scope"></a>
## 🚀 Scope

- **In scope:** documented interop friction between Augment Intent and a Claude-Code-CLI-backed agent seat — authentication/connect flows, workspace/session platform behavior, timeout patterns — generalized for a public audience.
- **Out of scope:** private ecosystem specifics (internal repo names, file paths, exact error text, screenshots) — those stay in the private source repo, referenced only in the final report as sanitized findings.

---

<a id="architecture"></a>
## 🏗️ Architecture

- **Private repo (this one):** raw findings, drafts, internal references
- **Public preview:** the sanitized, publishable version of the report
- **Sync:** GitHub Actions, allowlist model — everything private by default, only explicitly-classified paths reach the public mirror

---

<a id="collaboration"></a>
## 🤝 Collaboration

This is a solo-developer project (Christopher Wilson) built with AI-agent assistance across two platforms. Issues and discussion on the public preview are welcome.

---

<a id="license"></a>
## 📜 License

[MIT](LICENSE) — applies to this repo's own content (docs, configuration). It does not extend to Augment's own product or brand.

---

*Built and maintained by [drasticstatic](https://github.com/drasticstatic) · w/ Anthropic's Claude Code CLI + Augment Intent*
