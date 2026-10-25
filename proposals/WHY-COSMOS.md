# 🌌 Why Cosmos

### A proposal for the organizations we care for, and for the people who build with them

**TL;DR:** Claude Code, Codex and ChatGPT are wonderful helpers *beside* a person. **Augment Cosmos**
adds helpers that work *where the code is*:
- they wake when something happens on GitHub, do a focused job in a safe cloud workspace, and report back;
- they share a common memory across a whole organization;
- each organization gets its own **Space**, a focused room, so nobody's work gets tangled with anyone
  else's.

For a custodian looking after several organizations, Cosmos is the shared studio. For a newcomer, it's a
place to build without installing anything, where the house rules are already in the walls.

*Verified against Augment's own documentation on 2026-10-25. Where an outside summary claimed more than
the docs say, we left it out.*

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

Companion: [How we use Cosmos Spaces](../docs/COSMOS-SPACES.md).
