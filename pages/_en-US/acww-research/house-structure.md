---
lang: en-US
layout: wiki
section: acww-research
title: House and Room Structure
---

Here you'll find the structure of the House + Room part from AC:WW.

NOTE: With Layer 2 is meant: Items which are placed on a Furniture. Example: A lamp on a table.

### Room Structure

| Offset          | Datatype        | Size     | Content                   |
| --------------- | --------------- | -------- | ------------------------- |
| 0x0 - 0x44F     |                 | 0x450    | Room Size                 |
| 0x0 - 0x1FF     | uint16_t        | 0x200    | 256 Room Items Layer 1    |
| 0x200 - 0x3FF   | uint16_t        | 0x200    | 256 Room Items Layer 2    |
| 0x400 - 0x41F   | Bit indexes     | 0x20     | Item Enabled Bits Layer 1 |
| 0x420 - 0x43F   | Bit indexes     | 0x20     | Item Enabled Bits Layer 2 |
| 0x440 - 0x447   | uint8_t         | 0x8      | Padding or so???          |
| 0x448 - 0x449   | uint16_t        | 0x2      | Room Carpet               |
| 0x44A - 0x44B   | uint16_t        | 0x2      | Room Wallpaper            |
| 0x44C - 0x44D   | uint16_t        | 0x2      | Room Song                 |
| 0x44E - 0x44F   | uint8_t         | 0x2      | Padding 2???              |

### House Structure

| Offset          | Datatype        | Size     | Content                    |
| --------------- | --------------- | -------- | -------------------------- |
| 0x0 - 0x15A0    |                 | 0x15A1   | House Size                 |
| 0x0 - 0x44F     | Room_Struct     | 0x450    | Entry Room                 |
| 0x450 - 0x89F   | Room_Struct     | 0x450    | Back Wing                  |
| 0x8A0 - 0xCEF   | Room_Struct     | 0x450    | Right Wing                 |
| 0xCF0 - 0x113F  | Room_Struct     | 0x450    | Left Wing                  |
| 0x1140 - 0x158F | Room_Struct     | 0x450    | Second Floor               |
| 0x1590 - 0x1593 | uint32_t        | 0x4      | Debts                      |
| 0x1594 - 0x159C | Bit indexes     | 0x9      | Song Indexes               |
| 0x159D - 0x159F | uint8_t         | 0x3      | Unknown 1                  |
| 0x15A0 - 0x15A0 | uint8_t         | 0x1      | House Size and roof color? |

### Room Names

| Name         | Index |
| ------------ | ----- |
| Entry Room   | 0     |
| Back Wing    | 1     |
| Right Wing   | 2     |
| Left Wing    | 3     |
| Second Floor | 4     |

### House sizes

Small Room is the Upgrade Level, you get when you start a new game, then the other ones come as following:

* NOTE: Mansion is the last Upgrade Level, but also known as: North / Back Room.

* NOTE 2: Use `Value & 7` to get the house size.

| Name         | Upgrade Level | Debts    |
| ------------ | ------------- | -------- |
| Small Room   | 0             |  19.800  |
| Medium Room  | 1             | 120.000  |
| Large Room   | 2             | 298.000  |
| Second Floor | 3             | 598.000  |
| West Room    | 4             | 728.000  |
| East Room    | 5             | 848.000  |
| Mansion      | 6             | 948.000  |