# Findings Plan — source material + structure

Captured from
`~/intent/workspaces/__chief__/AGENT-SYNC/created-by-mystarch/HANDOFF-create_augment-intent-properties-repo.md`
(Mystarch, 2026-09-01) at repo-creation time, so nothing from that handoff gets lost. **The actual
findings write-up has not been drafted yet** — this file is the starting scaffold for whoever picks
that up next (Christopher, with LittlebirdAI's help per his own framing), not the report itself.

## What this report is for

Christopher's own framing (2026-09-01): "compiling all this information with the help of
LittlebirdAI closing gaps to share this as an issue with Augment's support team... in a nice html
surface to get this resolved."

**Framing note (2026-09-02, Christopher):** this is not meant to put Augment Intent in a bad light.
The goal is to get to the bottom of the interop friction constructively, while genuinely showcasing
the magic of Intent's properties/matrix — its spec-driven orchestration and workspace/delegation
model — and how to use it well when paired with Anthropic's models. Whoever drafts the actual report
should lead with what works, not just what's broken.

Secondary, non-blocking hopes (don't over-scope the report around these): possible recovery of lost
Auggie token usage from affected sessions, and a channel for the direct Augment dev contacts
Christopher has already made via email/LinkedIn.

## Source material to pull from (not re-derive from scratch)

- **`~/code/anthropas-argus-alfred/sandbox/INTENT_WORKTREE_LEGEND.md`** — the 🤔 Pondering section
  (Anthropic-API-login vs. Augment-native login theory, plus a confirmed concrete edge case: the
  `auggie login` prompt Intent's Settings surfaced when GitHub-connect was attempted directly) and the
  `__chief__` workspace section (empty spec note, not listed/searchable in the workspace switcher, no
  subagent delegation available from that seat, asymmetric `ws.app.workspaces.list()` reach).
- **`~/intent/workspaces/__chief__/PENDING-TASKS.md`** — the astro branch-resolution bug write-up
  (create-workspace proposal card can't resolve a base branch, confirmed not caused by empty-repo
  state), the `ws.app` code-path gap (`ws.app.workspaces.create(...)` always returns a preview object,
  no apply-without-UI path exists), and the Known Issues section (repeated 30-minute stream timeouts /
  "awaiting tool response" hangs in a single chat thread).
- **Recurring "awaiting tool response" / stream-timeout pattern** — worth documenting as its own data
  point alongside the GitHub-connect gap: multiple 30-minute timeouts and UI-frozen states observed
  across Intent sessions, distinct from (but possibly related to) the Auggie-login gap.
- **Confirmed, directly-reproducible: zero `ws.app.*` reach from a plain Claude Code CLI session
  outside Intent** (2026-09-03) — a sharper data point than the mostly-inferred/symptom-based
  entries above (the `auggie login` prompt, timeout patterns). A session launched against
  `~/code/mystarch_chief-of-staff` (the native-terminal fallback, not through Intent's UI or its
  desktop-app terminal-instance feature) has **no `ws.app.*` tool surface at all** — not degraded,
  absent — while `git`/`gh` and normal file editing work identically to an Intent-launched session.
  Documented in `mystarch_chief-of-staff/specs/chief-of-staff-operating-model.md` § 5 and
  `anthropas-argus-alfred/sandbox/INTENT_WORKTREE_LEGEND.md`'s "Where session chat logs actually
  live" section — pull the exact wording from those two rather than re-deriving it here.
- **Confirmed: Intent's `127.0.0.1:5179` local bridge has no real request authentication** (2026-09-03)
  — the `workspace_api` MCP tool is backed by an HTTP endpoint Intent's Electron app opens locally;
  it accepts `X-Workspace-Id`/`X-Workspace-Path`/`X-Agent-Id` headers at face value from any caller on
  the machine, fabricated or not, with no token/session check tying a request to an agent Intent
  actually spawned. Confirmed via direct `curl` against the port with invented header values while
  this ACP session was live. Separately, standalone-spawning the actual bridge script
  (`~/.augment/mcp-server/mcp-stdio-server.cjs`) outside Claude Code's own process tries to boot a
  second full Electron main process (Sentry init, Redux store bridge) rather than act as a lean proxy
  — Claude Code must set additional env when it spawns this normally that a bare `node` invocation
  doesn't get, so replicating Intent's exact spawn mechanism isn't the way in. This is a genuine
  **security-relevant finding**, not just an interop gap — flag it as such in the report, separately
  from the Auggie-login/GitHub-connect friction items above, since it likely warrants Augment's
  security team's attention rather than (or in addition to) support.
- **Login-persistence: launching via `open -a "Intent by Augment"` (Terminal/`open` CLI) vs. the
  macOS Dock/Applications icon produces different Augment-login outcomes** (2026-09-03) — this was
  tried specifically because Augment Support had previously suggested `open -a` as a fix attempt for
  login not persisting. Result: launching via `open -a "Intent by Augment"` **never resolves the
  Augment login at all** (stays logged out), whereas launching from the Dock/Applications **does let
  Augment login succeed, it just doesn't persist** across relaunches. So the two launch paths aren't
  equivalent workarounds for the same bug — one is strictly worse than the other, and the "fix"
  Support suggested doesn't reproduce the login step at all, only the persistence failure does. Worth
  a dedicated repro-steps entry in the report: exact launch command, observed state after each, and
  the fact this was already escalated to Support once (context for why this exact test was run again
  under ClaudeMent this time, to see whether the client—Augment-native vs. this Anthropic-backed
  session—changes either outcome).

## Proposed structure (per the handoff — confirm/adjust before drafting)

- **This repo (private)** — raw findings, drafts, anything not ready for outside eyes (exact error
  strings, internal file paths, screenshots with local usernames visible, etc.)
- **`augment-intent-properties-public-preview`** — the sanitized HTML surface, synced via
  `sync-public-allowlist.yml` — only explicitly allowlisted content ever leaves this repo

## Governance already in place (done at repo creation, 2026-09-02)

- MIT `LICENSE`, `.github/dependabot.yml`, `AGENT-SYNC`/`AGENT-SYNC_PUBLIC` skeleton
- `.graphifyignore` + Claude Code hook (keyless graphify setup)
- `.github/workflows/sync-public.yml` (allowlist model, generated via
  `my-template-clean/setup/init-public-sync.sh`) — PAT entered by Christopher himself, not by an
  agent, matching the established ecosystem convention
- GitHub Pages, branch protection ruleset, and topic tags on both repos

## Not done yet

- The actual findings write-up / report draft
- Deciding the exact HTML surface format for the public-preview lane
