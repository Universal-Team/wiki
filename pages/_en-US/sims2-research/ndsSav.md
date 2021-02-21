---
lang: en-US
layout: wiki
section: sims2-research
title: (NDS) SAV Structure
---

### Notes
The NDS SAV contains 5 possible Locations for the SAVSlots (`0x0`, `0x1000`, `0x2000`, `0x3000`, `0x4000`).. however only `3` can be at the maximum the actual displayed Slots in game. Checkout the External-Tool `LSSD` to get the Location of the `3` displayed Slots from in game.


## Structures

### NDSSAV
{% capture NDSSAV %}
| Offset           | Datatype        | Size     | Content                      |
| ---------------- | --------------- | -------- | ---------------------------- |
| 0x0 - 0x3FFFF    |                 | 0x40000  | Is 256 KB the actual size?   |
|                  |                 |          |                              |
| 0x0 - 0xFFF      | NDSSlot_Struct  | 0x1000   | First NDS Slot from Five     |
| 0x1000 - 0x1FFF  | NDSSlot_Struct  | 0x1000   | Second NDS Slot from Five    |
| 0x2000 - 0x2FFF  | NDSSlot_Struct  | 0x1000   | Third NDS Slot from Five     |
| 0x3000 - 0x3FFF  | NDSSlot_Struct  | 0x1000   | Fourth NDS Slot from Five    |
| 0x4000 - 0x4FFF  | NDSSlot_Struct  | 0x1000   | Fifth NDS Slot from Five     |
| 0x5000 - 0x3FFFF | uint8_t         | 0x3B000  | Unresearched yet             |
{% endcapture %}

{{ NDSSAV | markdownify }}