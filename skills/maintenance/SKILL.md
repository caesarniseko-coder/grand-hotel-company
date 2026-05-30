---
name: maintenance
description: In-room maintenance dispatch + repair protocol at Grand Hotel.
version: 1.0.0
metadata:
  hermes:
    tags: [hotel, engineering, maintenance, work-orders]
---

# Maintenance Dispatch

A guest reports a defect. You acknowledge, dispatch, and confirm.

## Common in-room issues + standard fix times

| Issue | Diagnose | Standard fix |
|---|---|---|
| AC not cooling | Check thermostat, filter, vents | 15 min |
| AC not heating | Same | 15 min |
| Plumbing leak (small) | Locate, shut valve | 10 min + dry |
| Plumbing leak (large) | Shut valve, room OOS, move guest | 30 min minimum |
| Toilet won't flush | Often a flapper or chain | 5 min |
| TV not working | HDMI, input source, power-cycle | 5 min |
| Wifi slow | Reboot AP, check switch | 10 min |
| Door lock issue | Reprogram or replace card | 10 min |
| Safe locked out | Master key + override code | 5 min |
| Lights out | Bulb / breaker | 5 min |
| Minibar fridge warm | Reset, then replace if not cold in 1 hr | 1 hr |

## Severity levels

- **Critical** (guest can't sleep in room): move guest first, then fix
- **High** (comfort affected): fix in 15 min; room change if not
- **Routine** (cosmetic, non-blocking): log + fix by next morning

## Workflow

1. **Acknowledge to guest within 60 sec** with ETA.
2. **Dispatch technician** by name (e.g., "Marco from Engineering will be
   at your door in 10 minutes").
3. **Confirm completion** to guest after technician reports done.
4. **Recovery**: if delay > 30 min OR room move required, offer a comp
   (drink in bar / spa credit / room upgrade) — coordinate with Concierge /
   Front Office.

## Common phrases for guest replies

```
Hi {{guest_name}} — sorry about the AC in Room {{room}}! I've dispatched
Marco from Engineering — he'll be at your door within 10 minutes with a
multimeter and replacement filter.
```

```
Hi {{guest_name}} — checking the leak in Room {{room}} now. If it's
something we can't fix in 15 minutes, I'll move you to a same-tier room
on the same floor and have your bags brought.
```
