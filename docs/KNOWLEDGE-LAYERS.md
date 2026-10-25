# 🧠 Knowledge layers: how our helpers (and our visitors) find what they need

**TL;DR:** five layers, each with one job. They complement each other; none replaces another.

| Layer | Who it serves | Its one job | Status (2026-10-25) |
|---|---|---|---|
| 🕸️ **Graphify** | AI helpers working on a codebase | A map of the code, so helpers read less and understand more | ✅ **In use:** I Am One Self and David Amaringo now carry one; eight fleet repos already did |
| 🧭 **BASE** | Claude Code, across a whole machine | Memory of rules, decisions and projects, placed into every turn | 🔍 **Promising; evaluate before installing** (below) |
| 🌌 **Cosmos Files** | A whole organization's Cosmos helpers | Shared notes and skills that every Expert in a Space can read | ⏳ With the Cosmos pilot ([WHY-COSMOS](../proposals/WHY-COSMOS.md)) |
| 📚 **Alexandrina** | Visitors and members | Answers **only from an organization's own materials**, with sources, plus help desks | ✅ **In use for PIR;** proposed for The Holy Earth Foundation |
| 🔎 **Site search** | Visitors | Finding a page or a phrase | ✅ In use (two kinds, below) |

---

## 🕸️ Graphify: rolled out

- **What:** a knowledge graph built from the code itself (tree-sitter), with a plain report
  (`graphify-out/GRAPH_REPORT.md`) and an interactive picture (`graph.html`).
- **Cost and privacy:** `graphify update .` builds the code graph **locally, with no AI calls and no API
  cost**. Nothing leaves the computer.
  - Documents, PDFs and images need an AI model (`graphify extract .`), which sends their text to that
    model's provider. So we keep that for repositories whose documents may leave the machine. Private
    proposals and recovery-related material stay code-only.
- **Rules we follow:**
  - A `.graphifyignore` keeps research, notes, imports and media out of the map.
  - The graph lives in the **private** workshop repository.
  - Each site's tripwire keeps `graphify-out/` out of anything published.
- **How helpers use it:** read the report first, and ask the graph questions (`graphify query`, `graphify
  path`, `graphify explain`) instead of searching file by file.
- **Guide:** [CONNECT-GRAPHIFY.md](https://github.com/drasticstatic/my-template/blob/main/walkthroughs/CONNECT-GRAPHIFY.md)
  · [full evaluation](https://github.com/drasticstatic/anthropas-argus-alfred-public-preview/blob/main/sandbox/GRAPHIFY_SETUP.md)

## 🧭 BASE: promising, evaluate before installing

[BASE ("basemode", by Christopher Kahler)](https://github.com/ChristopherKahler/base) is a single Rust
binary.
- **What it does:** it maps a workspace into a knowledge graph (code structure plus your projects, rules
  and decisions) and places the relevant slice into Claude Code at four moments: session start, each
  prompt, before a tool runs, and after it returns.
- **Where it comes from:** recommended in Charlie Automates' free resources, beside Graphify.

**Why we're not installing it fleet-wide yet:**
- **It hooks every Claude Code session on the machine.** The installer writes its hooks into the global
  `~/.claude/settings.json`, so it would shape every session in every repository, including private and
  sensitive ones. That is a big reach for a tool we haven't reviewed.
- **The install pipes a remote script into the shell** (`curl … | sh`). We review that kind of installer
  before running it, as we did for Firecrawl and Graphify.
- **Licence:** Functional Source License 1.1, which becomes Apache 2.0 after two years. It's fine for our
  own use, but it isn't an open-source licence today, so we don't vendor it into public templates.
- **It's young:** created June 2026, about 310 stars, version 0.16. It's moving fast, which is good, but it
  means pinning versions.
- **Overlap:** its code map overlaps with Graphify, which we already use. Its unique gift is the
  memory of rules and decisions. We partly cover that today with `AGENTS.md`, `PENDING-TASKS.md` and
  `AGENT-SYNC/`.

**How to evaluate it safely (one afternoon):**
1. Read `install.sh` and the hook scripts. Confirm what they read, write and send; that there are no
   network calls or telemetry beyond what's stated; and that there's an uninstall.
2. Install it under a **separate macOS user** (its own `~/.claude`), pointed at one public repository
   such as `my-template`. Pin `BASE_VERSION`.
3. Measure the tokens injected per turn, briefing quality, and any slowdown, against Graphify's report
   alone.
4. Then decide:
   - **Adopt** for builder machines (with a per-repository opt-out for sensitive ones).
   - **Watch** until Codex support lands, so one memory serves both helpers.
   - **Pass.**

## 📚 Alexandrina: the help desk layer (not a developer tool)

BASE and Graphify help **builders**. A.L.E.X.A.N.D.R.I.N.A. helps **visitors and members**:
- it answers **only** from an organization's own published materials, citing each source;
- it says *"I don't know, want to open a ticket?"* when nothing matches;
- it runs help desks (private threads, GitHub issues).

Each organization is its own tenant with its own sources, so one engine serves many fellowships without
mixing them.
- **In use:** Psychedelics in Recovery's `alex-desk`.
- **Proposed:** The Holy Earth Foundation's "Oracle, deepened" (THEF Proposal 003).

## 🔎 Site search: two kinds, both worth keeping

| | The kit's **⌘K / `/` search** (AstroLogs and portals) | **Pagefind** (I Am One Self) |
|---|---|---|
| **Reads** | Each site's `search.json`: entry titles, summaries, people, pinned links | Every word of every built page |
| **Reaches** | **Across sites:** a portal searches its AstroLog too | **One site, deeply** |
| **Languages** | As written | Separate English and Spanish indexes; results stay in the reader's language |
| **Best for** | "Take me to that entry / that person / that page" | "Where does the site talk about the dieta?" |
| **Weight** | Tiny; loads instantly | A small index that loads only when someone searches |

**Neither is superior; they answer different questions.** Keep both. A natural next step: let a site
with Pagefind contribute its results to the kit's ⌘K palette, so a portal's quick search can reach into a
retreat site's full text too.

## 🌱 What every organization gets, as these layers mature

1. **A code map** in each workshop repository (Graphify). This is now standard.
2. **One rulebook and one notebook** (`AGENTS.md`, `PENDING-TASKS.md`, `AGENT-SYNC/`). This is already
   standard ([org onboarding kit](https://github.com/drasticstatic/my-template/tree/main/org-onboarding)).
3. **A Cosmos Space** with shared Files and Skills.
4. **A cited help desk** (Alexandrina), when the organization wants one.
5. **Site search** that fits the site.

Whatever one organization learns, the others inherit.
