# Grand Hotel — AI management team for a 4–5★ city hotel

A fully-staffed AI management team for a **150-room, 4–5★** city/business hotel — 17 role-specific agents (GM through line managers) wired to run on a self-hosted LLM gateway, installable in **one command**.

Built on the [Agent Companies](https://companies.io) open standard. Installs into [Paperclip](https://paperclip.ing).

## What's in the box

- **17 agents** across the executive, division-head, department-manager, and supervisor tiers — full Rooms, F&B, Sales/Marketing, Finance, HR, Engineering, Security, and Spa coverage.
- **4 teams** (Rooms Division, Food & Beverage, Commercial, Support) bundling agents into the right reporting groups.
- **4 running projects** (Daily Operations, Guest Experience, Revenue Management, Audit Readiness) with their own heartbeats and goals.
- **4 seeded starter tasks** so the morning-briefing, housekeeping-board, weekly-rate-review, and guest-feedback loops self-start.
- **Per-agent heartbeats** tuned to the operational rhythm of each role — front-of-house fast (15 min), strategic slow (daily).

## Install (one command)

```bash
npx companies.sh add caesarniseko-coder/grand-hotel-company \
    --target new -y \
    --include company,agents,projects,tasks \
    --api-base https://<your-paperclip-instance>.hf.space \
    --api-key  <USER_API_KEY>
```

The `USER_API_KEY` is a user-level token (Paperclip → Settings → API). Agent tokens (`pcp_…`) won't work — they're scoped to agent ops and can't create companies.

## What "fully operational" means

Out of the box you get the **org chart, reporting lines, heartbeats, and the daily-ops loop running**. Every agent reasons through `qwen3:32b` via a self-hosted gateway, every call is metered and audited, and the GM's hourly heartbeat plus the line-agents' 15–30 min pulses keep work flowing through the org.

What's intentionally **not** in this package: real PMS / POS / booking integrations (Opera, Cloudbeds, Stripe, SiteMinder). Those plug in via Hermes' HTTP/MCP tool skills as a follow-up.

## Closed-loop guest comms

Pair this package with a small **comms-gateway** service (Telegram / Email / Web chat / Slack) and you have a complete closed loop: guests message the channel of their choice, the message is classified and routed to the right agent, the agent's reply is relayed back to the same channel. See `projects/guest-experience.md` for the integration pattern.

## License

MIT — see `LICENSE`.
