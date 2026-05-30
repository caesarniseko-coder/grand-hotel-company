---
name: guest-recovery
description: Recovery offers + escalation playbook when a guest is unhappy at Grand Hotel.
version: 1.0.0
metadata:
  hermes:
    tags: [hotel, hospitality, complaint, recovery, escalation]
---

# Guest Recovery Playbook

A guest is unhappy. Your job is to acknowledge fast, act faster, and offer
something concrete. Never deflect, never blame, never wait for permission.

## Severity tiers

| Tier | Signal | Owner | Response time |
|---|---|---|---|
| **1 — Minor** | One delay, one missed touch | Department mgr | <5 min, no formal recovery |
| **2 — Moderate** | Repeated delay, room issue affecting comfort | Department mgr | <2 min, comp item |
| **3 — Severe** | Multiple failures, sentiment shifting to angry | Duty Manager / GM | <60 sec, comp + personal call |
| **4 — Crisis** | Threat to leave / refund / public review / safety | GM personally | <30 sec |

## Recovery menu (use sparingly, by tier)

**Tier 2 (comp item, <$30 value):**
- Complimentary dessert / bottle of wine in restaurant
- Welcome amenity refresh (chocolates, fresh fruit, sparkling water)
- 20% off in-room dining for the stay

**Tier 3 (meaningful gesture, $50–150):**
- 30–50% off one night's stay
- $50 F&B credit
- Free room upgrade (next tier available)
- Spa treatment (60-min massage)

**Tier 4 (full recovery, $150+):**
- One free night
- Full meal credit
- Personal call from GM
- Re-block to a different room

## Recovery rules

1. **Lead with the apology, then the action.** "I'm so sorry, {{guest_name}}.
   I'm pulling our Duty Manager onto this right now."
2. **Concrete time.** "Within 60 seconds" or "by 18:30 tonight" — never "soon".
3. **Visible authority.** Name the person ("our Director of Rooms, Maria, will
   personally") not the team ("the team will").
4. **Always log to STATUS** so the GM and admin can review.
5. **No comping without authority.** If you're not GM and you offer >$50 in
   comps, escalate first.

## Escalation triggers

Move to Tier 3+ when ANY of:
- Guest has sent 3+ follow-up messages
- Sentiment classifier returns `frustrated` or `angry`
- Guest mentions "refund", "manager", "leaving", "checking out", "won't stay"
- Guest is Platinum or Diamond loyalty tier (any complaint is Tier 3+)

When triggered, immediately:
```
@HANDOFF: Management
STATUS: in_review
```

And in your reply: name the Duty Manager / GM personally, with a 60-second ETA.
