---
category: GBA
lang: en-US
layout: wiki
section: sims2-research
title: SAV Structure
---

## Notes
The Sims 2 GBA's used SAVSize is `0x5000`, but `0x5000 - 0xFFFF` is just unused space it seems, so technically for SAV Editors, a buffer of 0x5000 would even be enough.

`0x0 - 0xFFF` seems to be game metadata and settings related, while `0x1000 - 0x4FFF` is SAVSlot related. The game contains `4` Slots from a size of `0x1000` starting at `0x1000`.

It seems the game exist in EUR and USA variant... though SuperSaiyajinStackZ haven't gotten a USA version *yet*, but pretty sure the SAV Structure would be the same between both variants. Reports about, if the structure is the same would be appreciated in the [Universal-Team discord server](https://universal-team.net/discord) under the channel `#stackjects`.


### GBASAV
{% capture GBASAV %}
| Offset          | Datatype          | Size     | Content                                  |
| --------------- | ----------------- | -------- | ---------------------------------------- |
| 0x0 - 0xFFFF    |                   | 0x10000  | Full SAVSize                             |
| 0x0 - 0x4FFF    |                   | 0x5000   | Used SAVSize                             |
|                 |                   |          |                                          |
| 0x0 - 0xFFF     | MetaData_Settings | 0x1000   | See `MetaData_Settings` for more         |
| 0x1000 - 0x1FFF | GBASlot_Struct    | 0x1000   | First GBA Slot from Four                 |
| 0x2000 - 0x2FFF | GBASlot_Struct    | 0x1000   | Second GBA Slot from Four                |
| 0x3000 - 0x3FFF | GBASlot_Struct    | 0x1000   | Third GBA Slot from Four                 |
| 0x4000 - 0x4FFF | GBASlot_Struct    | 0x1000   | Fourth GBA Slot from Four                |
| 0x5000 - 0xFFFF | uint8_t           | 0xB000   | Just `0xFF` Padding (Unused)             |
{% endcapture %}

{{ GBASAV | markdownify }}

### MetaData_Settings
{% capture MetaDataSettings %}
| Offset          | Datatype        | Size     | Content                                                       |
| --------------- | --------------- | -------- | ------------------------------------------------------------- |
| 0x0 - 0xFFF     |                 | 0x1000   | Metadata and Settings Size                                    |
|                 |                 |          |                                                               |
| 0x0 - 0x6       | uint8_t         | 0x7      | Unique Game Header (0x53, 0x54, 0x57, 0x4E, 0x30, 0x32, 0x34) |
| 0x7 - 0x9       | uint8_t         | 0x3      | Settings Related things?                                      |
| 0xA - 0xA       | uint8_t         | 0x1      | See `Settings_Language` below for more                        |
| 0xB - 0xF       | uint8_t         | 0x5      | Settings Related things?                                      |
| 0x10 - 0xFFF    | uint8_t         | 0xFF0    | Metadata Related things?                                      |
{% endcapture %}

{{ MetaDataSettings | markdownify }}


### Settings_Language
{% capture SettingsLanguage %}
| Value | Language    |
| ----- | ----------- |
| 0     | English     |
| 1     | Nederlands  |
| 2     | Français    |
| 3     | Deutsch     |
| 4     | Italiano    |
| 5     | Español     |
{% endcapture %}

{{ SettingsLanguage | markdownify }}