---
schema: agentcompanies/v1
name: Grand Hotel
slug: grand-hotel
description: A fully-staffed AI management team for a 4–5★, 100–200-room city/business hotel. Seventeen role-specific agents covering Rooms, F&B, Sales, Finance, HR, Engineering, Security, Spa and the front-of-house, with realistic reporting lines, heartbeat cadences, and seeded daily-ops, guest-experience, revenue, and audit-readiness projects.
version: 1.0.0
license: MIT
authors:
  - name: Idea Comms
goals:
  - Run a 150-room, 4–5★ hotel as a self-driving daily-ops loop — morning briefing → handoffs → end-of-day review
  - Keep guest satisfaction (post-stay rating) ≥ 9.0 / 10 across all reviews and channels
  - Hit occupancy + ADR + RevPAR forecasts week-over-week through disciplined revenue management
  - Maintain 5★ audit readiness in cleanliness, safety, F&B quality, and guest experience at all times
  - Surface and escalate guest complaints to the GM with priority while resolving the underlying issue at the source department
---

# Grand Hotel

Grand Hotel is an upscale (4–5★) 150-room city hotel. This company defines its full management team as Paperclip agents — every role from the GM down to the housekeeping supervisor and the spa manager — wired to run on the gateway's `qwen3:32b` model and to talk to each other through Paperclip's issues/handoffs.

## How work flows

1. **GM** opens the day with a morning briefing on `projects/daily-operations`: yesterday's pickup, today's arrivals/departures, occupancy / ADR / RevPAR vs forecast, open incidents, guest-satisfaction trend, staffing.
2. **Department heads** (DOR, D F&B, DOSM, Chief Engineer, DOF, HR Dir, Security, Spa) read the briefing and break the day's priorities into actions for their teams.
3. **Line agents** (Front Office, Reservations, Concierge, Housekeeping, Restaurant, Revenue) execute the operational pulse — check-ins/outs, rate decisions, room turns, restaurant cover counts, guest requests.
4. **Closed-loop** with guests: an external comms gateway bridges Telegram / Email / Web chat / Slack into this team as Paperclip issues, with the agents' replies relayed back to the channel automatically. Guest-facing roles (Front Office, Concierge, Reservations, F&B, Spa, Maintenance) are the natural responders; complaints escalate to GM.
5. **End-of-day** review on `projects/daily-operations` — what worked, what didn't, what to brief into tomorrow.

## The team at a glance

| Tier | Agents |
|---|---|
| Executive | GM |
| Division Heads | DOR, D F&B, DOSM, DOF, HR Director, Chief Engineer, Security Manager, Spa Manager |
| Department Managers | Front Office Mgr, Reservations Mgr, Concierge, Executive Housekeeper, Exec Chef, Restaurant Mgr, Revenue Manager |
| Supervisor | Housekeeping Supervisor |

17 agents, three reporting tiers, heartbeats tuned to the operational rhythm of each role (front-of-house fast, strategic slow). All powered by `qwen3:32b` through the gateway, audited and metered per call.

## Operating standards

- **Service:** Forbes / LQA mindset — anticipate, personalise, recover quickly.
- **Communication:** clear, courteous, time-stamped. Escalate early when in doubt.
- **Data:** treat every guest interaction as a data point; feed it back into the daily-ops review.
- **Handoffs:** each agent specifies what it produces and who it hands off to (encoded in each `AGENTS.md`).

---

Built for the [Agent Companies](https://companies.io) open standard, installable with `npx companies.sh add caesarniseko/grand-hotel-company`.
