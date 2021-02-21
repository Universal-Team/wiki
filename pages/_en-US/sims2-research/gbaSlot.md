---
lang: en-US
layout: wiki
section: sims2-research
title: (GBA) Slot Structure
---

## Notes
There aren't any notes available for GBASlots yet.

## Structures

### GBASLOT
{% capture GBASlot %}
| Offset          | Datatype        | Size     | Content                                  |
| --------------- | --------------- | -------- | ---------------------------------------- |
| 0x0 - 0xFFF     |                 | 0x1000   | Slot Size                                |
|                 |                 |          |                                          |
| 0x0 - 0x1       | uint8_t         | 0x2      | Unknown                                  |
| 0x2 - 0x3       | uint16_t        | 0x2      | Timestamp (0x2: Hour, 0x3: Minute)       |
| 0x4 - 0x5       | uint8_t         | 0x2      | Unknown                                  |
| 0x6 - 0x9       | uint32_t        | 0x4      | Simoleons (999.999 Seems to be the max)  |
| 0xA - 0xB       | uint16_t        | 0x2      | Ratings (9999 seems to be the max?)      |
| 0xC - 0xC       | uint8_t         | 0x1      | Unknown                                  |
| 0xD - 0x14      | char            | 0x8      | Sim Name (8 Characters ASCII)            |
| 0x15 - 0xFFF    | uint8_t         | 0xFEB    | Unknown                                  |
{% endcapture %}

{{ GBASlot | markdownify }}