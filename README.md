# Augment Intent Properties 🔗

> Showcasing what Augment Intent's orchestration model does well when paired with Anthropic's Claude models — and documenting the interop rough edges worth ironing out along the way.

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

Augment Intent's spec-driven orchestration — the "properties/matrix" that coordinates workspaces, specs, and agent delegation — is genuinely strong when it's working as designed. This repo compiles a fair, evidence-based look at that model as it runs on Claude Code CLI as the underlying agent instead of native Auggie: what works well and is worth showcasing, alongside the specific interop friction (authentication/GitHub-connect flows, workspace-visibility quirks, platform-level timeouts) observed across real working sessions in this agent-fleet ecosystem. The goal is a constructive report Augment's own team can act on — getting to the bottom of the friction, not filing a grievance list.

**Developer / builder:** Christopher Wilson (`drasticstatic`)
**AI agents:** Mystarch (Augment Intent) — original findings compilation · Alfred (Claude Code CLI) — repo scaffolding & public-preview lane

---

<a id="the-goal"></a>
## 🎯 The Goal

Show how well Intent's orchestration model works under Anthropic's models when it's set up right — and turn the scattered, session-by-session friction into a single well-evidenced report Augment's support team can use to actually close the gap. Non-blocking hoped-for outcomes: a clearer support channel and recovery of any token usage lost to the affected sessions.

---

<a id="scope"></a>
## 🚀 Scope

- **In scope:** what Intent's spec/workspace/delegation model does well on a Claude-Code-CLI-backed agent seat, plus documented interop friction (authentication/connect flows, workspace/session platform behavior, timeout patterns) — generalized for a public audience.
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
