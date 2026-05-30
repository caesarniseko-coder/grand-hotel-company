---
name: personalisation
description: How to use guest profile + history to personalise replies at Grand Hotel.
version: 1.0.0
metadata:
  hermes:
    tags: [hotel, hospitality, personalisation, VIP, loyalty]
---

# Personalisation Discipline

Every guest issue comes with a profile (loyalty tier, preferences, stay
length, booking ref). Use it explicitly. Personalisation = "you know me",
not "you're nice".

## Loyalty tiers (rights and expected touches)

| Tier | Approx % | Standard touches |
|---|---|---|
| Diamond | 10% | Suite upgrade on arrival, welcome amenity (bottle), personal email from GM, complimentary breakfast for two, lounge access |
| Platinum | 20% | Complimentary breakfast for one, lounge access, 16:00 late checkout, room preference held |
| Gold | 30% | Complimentary wifi premium, 14:00 late checkout, water + chocolates in room |
| Silver | 20% | 13:00 late checkout, welcome card |
| None | 20% | Standard service |

## Profile fields and how to use them

- **`segment`** (Business / Leisure / Group / Corporate):
  - Business → quick, efficient, room service emphasised
  - Leisure → warm, recommendation-rich
  - Group → coordinator coordination, time-sensitive
  - Corporate → discretion, direct billing
- **`prior_stays`**: 0 → welcome them; 1+ → "welcome back"; 5+ → "always a
  pleasure" + reference past visit
- **`preferences`**: read it. If "Mediterranean breakfast" — confirm we have
  it. If "feather-free pillows" — confirm bedding is ready. If "high floor" —
  confirm room is on a high floor.
- **`payment_status`**: don't reference it to the guest unless they ask. If
  pre-auth — they may still be waiting on a charge confirmation.

## Examples

For Diamond returning guest with preferences:
```
Welcome back, {{guest_name}} — always a pleasure. Your suite on the 14th
floor is ready with feather-free pillows as you prefer. Our concierge desk
will check in with you within the hour to see if there's anything else.
```

For first-time leisure guest:
```
Welcome to Grand Hotel, {{guest_name}}! I'd love to recommend a few local
spots — what sort of food/atmosphere do you fancy tonight?
```

For business / corporate stay:
```
Hi {{guest_name}} — your room is ready, and your billing is set to direct
to the company account. Anything else I can have set up before your meeting?
```

## When the guest's request relates to a preference

Always cross-reference: if a Gluten-free guest asks about breakfast, mention
the gluten-free pastries. If a high-floor-preferring guest asks about their
room, confirm the floor. This is the difference between service and care.
