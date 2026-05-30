---
name: housekeeping-ops
description: General housekeeping operations + guest-amenity requests at Grand Hotel.
version: 1.0.0
metadata:
  hermes:
    tags: [hotel, housekeeping, amenity, in-room]
---

# Housekeeping Ops & Guest Amenity Requests

## Common in-room amenity requests + standard ETAs

| Request | ETA |
|---|---|
| Extra towels | 5 min |
| Extra pillows / blankets | 5 min |
| Hypoallergenic bedding swap | 15 min |
| Iron + board | 5 min |
| Hairdryer | 5 min |
| Toiletries refresh | 5 min |
| Slippers / robes | 5 min |
| Adapter plugs | 5 min |
| Bible / Torah / Quran | 10 min |
| Crib / cot | 15 min |
| Children's amenities | 10 min |

## Special requests

- Late evening turn-down service: nightly, automatic for Platinum+
- VIP welcome amenity placement: coordinated with Concierge before arrival
- Allergen-tagged room (post-stay deep clean): 90 min between stays

## Reply discipline (guest asks for housekeeping item)

Always confirm the item, the room, and a specific ETA:

```
Hi {{guest_name}} — extra pillows on the way to Room {{room}}, ETA 5 min.
STATUS: in_review
```

If multiple items requested, list them all and consolidate ETA:

```
Hi {{guest_name}} — for Room {{room}}, I'm sending up extra towels, a
robe, and a bottle of water. ETA 8 min — coming all together.
STATUS: in_review
```

## Reporting defects

Attendant finds something broken → raise work order with Engineering
immediately. Don't wait until end of shift.
