# 🌌 Why Cosmos

### A proposal for the organizations we care for, and for the people who build with them

**TL;DR:** Claude Code, Codex and ChatGPT are wonderful helpers *beside* a person. **Cosmos** (built by
Augment, part of **Harness** since 8 October 2026) adds helpers that work *where the code is*:
- they wake when something happens on GitHub, do a focused job in a safe cloud workspace, and report back;
- they share a common memory across a whole organization;
- each organization gets its own **Space**, a focused room, so nobody's work gets tangled with anyone
  else's.

For a custodian looking after several organizations, Cosmos is the shared studio. For a newcomer, it's a
place to build without installing anything, where the house rules are already in the walls.

*Verified against Augment's own documentation on 2026-10-25. Where an outside summary claimed more than
the docs say, we left it out.*

> 🔭 **New (2026-10-26):** Harness bought Cosmos, the Auggie CLI and Augment's Code Context Engine on
> **8 October 2026**. Cosmos still works the same, at the same address. **No sunset or migration date has
> been announced.** Everything below still holds; what changes is in
> [Cosmos's new home: Harness](#-cosmoss-new-home-harness).

---

## 🧩 What Cosmos is, in its own words

| Concept | What it means for us |
|---|---|
| **Expert** | A reusable helper: its instructions, model, workspace, abilities, and the events it reacts to. *Example: "THEF Site Helper", which reads `AGENTS.md`, works on `preview` and opens a pull request.* |
| **Environment** | The cloud computer an Expert works in, set up with the organization's repositories. A sandbox: nothing it does touches anyone's own machine. |
| **Trigger / Automation** | "When this happens, wake that Expert": a new pull request, an issue, a schedule, a webhook. |
| **Capability** | What an Expert may use: GitHub, web access, MCP servers (the same Firecrawl, Wix and WordPress connections our other helpers use). |
| **Session** | A conversation with an Expert, private or shared, from the web, a phone or Slack. |
| **Files** | A shared memory: files the Experts read and write, either visible to the whole organization or private to one person. |
| **Skills** | Packaged know-how in the open skills format, which Claude and Codex read too. Write once, use everywhere. |
| **Space** | A room for one team or workstream: its Experts, Environments, Sessions, secrets and connections, without the clutter of everyone else's. |

Source: [Getting started with Cosmos](https://docs.augmentcode.com/cosmos/getting-started) ·
[Cosmos Spaces](https://docs.augmentcode.com/cosmos/spaces/overview)

## 🙌 Why it serves us

**For the custodian (one person caring for five organizations):**
- **One studio, five rooms.** A Space each for The Holy Earth Foundation, Psychedelics in Recovery,
  Psanctuary, Psanctuary Church and ORG.
  - Each room keeps its own helpers, secrets and connections.
  - The custodian moves between them without mixing anything up. Four are already set up (see
    [COSMOS-SPACES.md](../docs/COSMOS-SPACES.md)).
- **Work continues while you're away.** A review Expert can greet every pull request, including those
  opened by a volunteer's Codex or ChatGPT. It checks the house rules, the second language and the build.
  A small problem gets caught before it reaches a live site.
- **Lessons stay learned.** Shared Files and Skills mean a correction made once (*"keep the Spanish twin
  in step"*) is there for every helper next time, in every Space that needs it.
- **No single point of failure.** The helpers, their instructions and the organization's memory live in
  the organization's account, not in one person's laptop or one person's head.

**For a contributor like Kenney:**
- **Nothing to install.** Open Cosmos in a browser (or a phone), pick the foundation's Space, and ask in
  plain words.
- **Safe to play, not a cage.**
  - Private sessions for trying ideas.
  - A default helper that already knows the rulebook.
  - Every change lands on the rehearsal copy first.
  - As confidence grows, the same Space opens wider: more helpers, more repositories, more automation,
    granted by the owners when the team is ready.
- **A team, not a tool.** Kenney's own helpers (ChatGPT, Codex) and the foundation's Cosmos helpers
  work on the same repositories under the same rules, and each one's work is credited honestly.

## 🤝 How it fits with everything else

| Helper | Where it works | Its gift |
|---|---|---|
| **Claude Code** | beside you, on your computer or the web | careful, hands-on building, with you |
| **Codex** | in OpenAI's cloud workspace, or beside you | building while you're away; GitHub pull requests |
| **ChatGPT** | in conversation | thinking, writing, explaining |
| **Littlebird** | on your own computer | remembering your day, privately |
| **Cosmos** | in the organization's cloud, on events | reviewing, maintaining, coordinating; shared memory across a whole team |

They share one rulebook (`AGENTS.md`), one notebook (`PENDING-TASKS.md`, `AGENT-SYNC/`) and one credit
line. See [Many AI tools, one team](https://github.com/drasticstatic/my-template/blob/main/walkthroughs/MANY-AI-TOOLS-ONE-TEAM.md).

## 🛡️ Safeguards, as the docs describe them

- **A Space is not an access grant.** Spaces organize the work. *Who may use* each Expert, MCP server or
  secret is granted separately, so a newcomer's room can be generous without being risky.
- **Secrets are scoped** to the Spaces they're "Used in". A foundation's key never wanders into another
  foundation's Space.
- **Two ways to act on GitHub:**
  - As the **organization's bot** (the Augment GitHub App, installed by an owner on chosen repositories).
  - As **the person** who started the work (their own GitHub sign-in), so their commits are honestly
    theirs.
- **Everything can be switched off.** Remove a trigger and an Expert stops waking. Remove a capability and
  it loses that tool. Owners choose which repositories the GitHub App may see.
- **Our own rails still apply:** rehearsal first, the tripwire, the secret scan, the never-publish rule.

Source: [Using GitHub as a tool or trigger](https://docs.augmentcode.com/cosmos/connectors/config-github)

## ⚖️ Costs and honest risks

- **Usage-based.** Cosmos bills by use, visible under **Usage** and **Billing**. We start each Space with a
  hard monthly cap and widen it only when the value is clear.
- **The company is changing.** Harness has
  [announced it is acquiring Augment Code](https://www.harness.io/blog/harness-acquires-augment-code-cosmos).
  Our protection is the same as always: everything that matters lives **in GitHub**, in plain files that
  any helper can read. The rulebook, the notebook, the skills and the sites themselves would all carry on
  if we ever moved.
  - *Update 2026-10-26:* the purchase was of Cosmos, the Auggie CLI, the Code Context Engine and the team,
    not of the Augment company. Details, dates and guards in
    [Cosmos's new home: Harness](#-cosmoss-new-home-harness).
- **Model prices carry a fee.** Augment bills model use at the provider's list price plus a 40% service
  fee; compute has no fee ([pricing](https://www.augmentcode.com/pricing), read 2026-10-26). Cosmos earns
  its keep on reviewing and caretaking; bulk building stays with the helpers beside us.
- **Privacy.** Read Augment's data terms before connecting a Space to anything sensitive. Recovery-related
  material needs particular care. Psychedelics in Recovery's own proposal sets its safeguards.

## 🌱 The proposal

1. **The Holy Earth Foundation first**, as the friendly pilot. Its Space already exists.
   - Add one Environment (the site repositories) and one default Expert (the site helper that follows
     `AGENTS.md`).
   - Add one review trigger (on pull requests into `preview`).
2. **A month of gentle use.** Kenney plays in private sessions, the review Expert greets his pull requests,
   and we note what helps.
3. **Then, room by room:** Psychedelics in Recovery under its own Tech Committee proposal, then
   Psanctuary, Psanctuary Church and ORG. Each starts with the same small setup.

The proposal is unchanged by the Harness purchase: the same first room, the same gentle month, the same
caps.

---

## 🔭 Cosmos's new home: Harness

**In one line:** on **8 October 2026**, Harness, a software-delivery company, bought Cosmos, the Auggie
CLI, Augment's Code Context Engine and related technology, with the team behind them. Cosmos is now the
**Harness Cosmos Software Factory Agent**. Every fact here was read on **2026-10-26** and links to its
source; anything unconfirmed says **to confirm**.

### 📅 What happened, and when

| Date | What | Source |
|---|---|---|
| 2026&#8209;03&#8209;31 | Augment retired Next Edit and Completions in its editor extensions for non-Enterprise plans, to focus on agents | [Augment changelog](https://www.augmentcode.com/changelog/planned-march-31-sunset-for-next-edit-and-completions) |
| 2026&#8209;06&#8209;30 | Harness made **Worker Agents** (AI agents as pipeline steps) generally available | [Harness](https://www.harness.io/press-and-news/harness-launches-autonomous-worker-agents-for-software-delivery) |
| 2026&#8209;10&#8209;07 | Augment still shipping: VS Code extension 0.904.1 | [Augment changelog](https://www.augmentcode.com/changelog) |
| **2026&#8209;10&#8209;08** | **Harness acquired "select assets" of Augment Code** (Cosmos, Auggie CLI, Code Context Engine, related technology) and the team behind them. Terms undisclosed. An asset purchase, not a merger or a partnership | [Harness press release](https://www.harness.io/press-and-news/harness-acquires-augment-code) · [Harness CEO's blog](https://www.harness.io/blog/harness-acquires-augment-code-cosmos) · [Augment's post](https://www.augmentcode.com/blog/augment-code-next-chapter) · [SiliconANGLE](https://siliconangle.com/2026/10/08/harness-acquires-augment-code-to-bridge-software-engineering-from-idea-to-deployment/) |
| 2026&#8209;10&#8209;08 | Cosmos is "available now" under Harness's name, with a free start (no credit card) | [Cosmos product page](https://www.harness.io/products/cosmos-software-factory-agent) |
| 2026&#8209;10&#8209;13 | Harness's engineering lead and Augment's co-founder describe the governed factory: isolated VMs or self-hosted daemons, per-run credentials, policy gates, and a human making every merge | [Harness blog](https://www.harness.io/blog/inside-a-governed-software-factory-with-harness-cosmos) |
| 2026&#8209;10&#8209;14 | Cosmos is reached through Augment's site "for now" and will move into the Harness platform "in the future". The loop that sends downstream failures back to Cosmos runs through tickets today. Bringing Cosmos under Harness's agent identity and policy controls is "in progress" | [The New Stack](https://thenewstack.io/harness-augment-cosmos-acquisition/) |
| 2026&#8209;10&#8209;26 | Augment's plans unchanged (Standard $20/month, Business $100/month, Enterprise custom); the page footer reads "© 2026 Harness, Inc." | [Augment pricing](https://www.augmentcode.com/pricing) |

**Not announced (as of 2026-10-26):** any sunset date for Cosmos, the Auggie CLI, the editor extensions or
the Context Engine; a date for the move into the Harness platform; what happens to existing contracts,
credits, code indexes and data deletion ([open questions, commentary](https://www.beri.net/article/harness-augment-code-cosmos-asset-acquisition-auggie-context-engine-customer-contracts-continuity)).
Harness's CEO: "Our customers will get a choice. They can keep using their preferred coding tools, adopt
Harness Cosmos, or use both."

### 🧭 How we got here

The custodian's tooling path has followed Augment from the start:
- **Augment in VS Code** first showed what a helper that understands a whole codebase could do.
- A brief stretch with the **Auggie CLI**, then **Claude Code CLI**, which became the daily driver.
- At the same time, **Augment Intent**'s spec-driven orchestration (a coordinator that writes the plan and
  delegates to agents) was the magic this repository was built to showcase, until Intent was sunset.
- We kept an **ACP** (Agent Client Protocol) path open so our own agents could keep working that way.
- **Cosmos** gave us a first taste of a real software factory: Experts that wake on events, one Space per
  organization.
- Now Cosmos has a new home at **Harness**.

### 🏗️ What Harness offers

- **Cosmos, unchanged in kind:** prebuilt Experts (PR Author, Deep Reviewer, Risk Analyzer, Verifier,
  Ticket Dispatcher, Project Builder and more), event triggers, isolated VMs or self-hosted daemons, model
  routing, shared org memory, versioning and auditing, and **budget controls per automation or user**
  ([product page](https://www.harness.io/products/cosmos-software-factory-agent)).
- **The work after the merge:** Harness's own agents for delivery, security testing, runtime protection and
  cost. The Code Context Engine is linked to Harness's **Software Delivery Knowledge Graph**, so Cosmos can see
  test requirements, security findings and past incidents before it writes code
  ([press release](https://www.harness.io/press-and-news/harness-acquires-augment-code)).
- **Governance:** the same policies that gate human deployments gate the agents; agent tokens are minted
  per run and deleted afterwards; low-risk approval is possible, but a human makes every merge
  ([blog](https://www.harness.io/blog/inside-a-governed-software-factory-with-harness-cosmos)).
- **A bridge to Claude:** the **Harness MCP Server** ([MIT](https://github.com/harness/mcp-server)) has been in
  Claude's Connectors Directory since 2026-06-01. It uses OAuth and acts only within the person's own Harness
  permissions ([blog](https://www.harness.io/blog/harness-claude-connector)). Worker Agents can be handed a
  task from Claude Code through it.
- **Open source and a free tier:** the Free plan is $0 and includes **Harness Open Source**
  ([Apache 2.0](https://github.com/harness/harness): code hosting, CI/CD pipelines, developer environments,
  an artifact registry). Paid plans are quoted by sales; no nonprofit program is listed
  ([pricing](https://www.harness.io/pricing); **to confirm**).

### 🔁 What we use today, and where it goes

| What we use | Under Harness | Portable alternative |
|---|---|---|
| 🌌 **Cosmos Spaces** (one per organization) | The same Spaces at the same address; into the Harness platform later, no date | `AGENTS.md`, `PENDING-TASKS.md` and `AGENT-SYNC/` in GitHub |
| 🧑‍🔧 **Experts** (site helper, review helper) | The same prebuilt Experts; Harness Worker Agents too, if we ever run Harness pipelines | Claude Code or Codex doing the same job on request |
| 🗂️ **Files and Skills** | Shared org memory in Cosmos | Copies in GitHub; Skills in the open format |
| 🧠 **Context Engine** | Now Harness's, linked to its delivery knowledge graph over MCP | **Graphify**, local and free ([KNOWLEDGE-LAYERS](../docs/KNOWLEDGE-LAYERS.md)) |
| 🎼 **Intent** | Not named in the deal | An **Intent** app at [intentapp.dev](https://intentapp.dev/docs): free, [Apache 2.0](https://github.com/intent-hq/intent), with Claude Code, Codex, Auggie and others as agents (**maintainer: to confirm**) |
| 🔌 **ACP** | The Auggie CLI speaks it ([`auggie --acp`](https://docs.augmentcode.com/cli/acp)); nothing further said | [ACP](https://zed.dev/acp) is an open protocol, not Augment's; any ACP agent can take the seat |
| ⌨️ **Auggie CLI** | Acquired; 0.36.0 on 2026-08-21 was the latest release we saw | Claude Code CLI |

### 🪨 What stays the same

- **GitHub is home** for every organization's repositories, issues and records.
- **One rulebook** (`AGENTS.md`) and **one notebook** (`PENDING-TASKS.md`, `AGENT-SYNC/`) for every helper.
- **Claude Code CLI** stays the daily driver; each person keeps their own helpers.
- **Graphify maps** stay in the private workshops.
- **Our rails:** rehearsal first, the tripwire, the secret scan, the never-publish rule.

### 🧪 What we'd pilot first

1. **The proposal above, unchanged:** The Holy Earth Foundation's Space, one site helper, one review trigger,
   a hard monthly cap.
2. **Ask in writing first:** whether each organization's account moves to Harness, which data terms cover
   its code and index, and how deletion works on exit.
3. **Harness's own tools** (the MCP Server, Worker Agents, Harness Open Source) are tried first in the
   custodian's own lab repositories, never on an organization's repositories first.

### 🛡️ Lock-in and cost guards

- **Monthly only, never prepaid.** Top-ups bought outside a plan expire after 12 months; no paying ahead for
  roadmap features.
- **Two caps:** each Space's hard monthly cap, plus Cosmos's own budget per automation or user.
- **Keep copies:** anything worth keeping in Cosmos Files is copied into GitHub.
- **Exit plan:** remove the GitHub App and tokens, and ask in writing for the code index to be deleted.

### 🚀 Ready to scale sooner than expected

The foundations are already laid: one rulebook and one notebook per repository, the
[org onboarding kit](https://github.com/drasticstatic/my-template/tree/main/org-onboarding), Graphify maps,
and Spaces that already exist. Cosmos now has a larger company's governance behind it. So each organization
can start when it's ready, with the same small setup, rather than waiting on Augment's future:
- **The Holy Earth Foundation:** its Space has been waiting since 2026-09-11 and its two sites are home, so
  the review helper can start this month.
- **Psychedelics in Recovery:** its Space exists too. Its Tech Committee's own proposal sets the pace and the
  safeguards; if the first month goes well, the next phases can come sooner.
- **Psanctuary Church and ORG:** their Spaces were in place by 2026-10-05, so the first room's setup can be
  copied as soon as it has proved itself.
- **Psanctuary:** joins when it's ready; nothing is lost by waiting.

Scaling, for all of them, means more repositories under the same caps, never more autonomy without the
owners' say.

### ❓ Questions for each organization's owners

1. **Start now under the new name, or wait** for Harness to say when Cosmos moves into its platform? We
   suggest starting small now; nothing in the plan depends on the move.
2. **Whose account?** Should each organization own its account from the start, so its Space moves as its own?
3. **Harness's other tools:** leave them for a later look, after the first month?

### 📒 Decisions log

| Date | Decision | By |
|---|---|---|
| 2026&#8209;09&#8209;11 | The first Spaces created (The Holy Earth Foundation, Psychedelics in Recovery) | Christopher |
| 2026&#8209;10&#8209;25 | Proposed: The Holy Earth Foundation first, then room by room | Christopher |
| 2026&#8209;10&#8209;26 | Harness bought Cosmos. Proposed: same plan and caps; written answers on accounts and data first; Harness's own tools tried in the lab first | Proposed; each organization decides |

Companion: [How we use Cosmos Spaces](../docs/COSMOS-SPACES.md).
