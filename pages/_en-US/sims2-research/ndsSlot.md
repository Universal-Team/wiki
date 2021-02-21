---
lang: en-US
layout: wiki
section: sims2-research
title: (NDS) Slot Structure
---

## Notes
The NDSSlot contains a Header part starting at `0x0 - 0x13`, however `0x10 - 0x11` does not count to it, because that seems like a shared Checksum between Main Slot and Header. Then `0x14 - 0xFFF` seems to be the Main part of the Slot.

It seems to contain 3 Checksums in place of a single Slot:

`0xE - 0xF`: Header Checksum

`0x10 - 0x11`: Shared Checksum

`0x28 - 0x29`: Main Checksum

However.. the Header part *MUST* match with the Shared Checksum.. and the Main part *MUST* match with the Shared Checksum as well, otherwise this is an invalid Checksum and the game `"corrupts"` the Header part, so the game doesn't detect it anymore. If that happened, then that Slot isn't usable, until the Header gets fixed, which can be fixed with the `NDSSLotFixer` Tool which can be found on the `External-Tools` page.

## Structures

### NDSSLOT
{% capture NDSSlot %}
| Offset          | Datatype        | Size     | Content                                               |
| --------------- | --------------- | -------- | ----------------------------------------------------- |
| 0x0 - 0xFFF     |                 | 0x1000   | Slot Size                                             |
|                 |                 |          |                                                       |
| 0x0 - 0x13      | Header          | 0x14     | Slot Header (See `Header` for more)                   |
| 0x14 - 0x17     | uint32_t        | 0x4      | SAVCount stored again? (0x00000000 - 0xFFFFFFFF)      |
| 0x18 - 0x21     | uint8_t         | 0xA      | Unknown                                               |
| 0x22 - 0x23     | uint16_t        | 0x2      | Slot Position stored again? (0x22 + 0x23 is the Slot) |
| 0x24 - 0x27     | uint8_t         | 0x4      | Unknown                                               |
| 0x28 - 0x29     | uint16_t        | 0x2      | Main Checksum                                         |
| 0x2A - 0x2B     | uint8_t         | 0x2      | Unknown                                               |
| 0x2C - 0x2F     | uint32_t        | 0x4      | Simoleons (999.999 seems to be the max?)              |
| 0x30 - 0x36     | char            | 0x7      | Sim Name (7 Characters ASCII)                         |
| 0x37 - 0xFFF    | uint8_t         | 0xFC9    | Unknown                                               |
{% endcapture %}

{{ NDSSlot | markdownify }}

### Header
{% capture NDSHeader %}
| Offset          | Datatype        | Size     | Content                                                      |
| --------------- | --------------- | -------- | ------------------------------------------------------------ |
| 0x0 - 0x13      |                 | 0x14     | Header Size                                                  |
|                 |                 |          |                                                              |
| 0x0 - 0x7       | uint8_t         | 0x8      | Unique Header (See Unique_Header_Note for more)              |
| 0x8 - 0xB       | uint32_t        | 0x4      | SAVCount (0x00000000 - 0xFFFFFFFF)                           |
| 0xC - 0xD       | uint16_t        | 0x2      | Slot Position (0xC + 0xD is the Slot position)               |
| 0xE - 0xF       | uint16_t        | 0x2      | Header Checksum                                              |
| 0x10 - 0x11     | uint16_t        | 0x2      | Header x Slot Checksum (Shared Checksum)                     |
| 0x12 - 0x12     | uint8_t         | 0x1      | Unknown                                                      |
| 0x13 - 0x13     | uint8_t         | 0x1      | New Created Slot Flag? (0x0 for newly created, 0xFF for not) |
{% endcapture %}

{{ NDSHeader | markdownify }}

### Unique_Header_Note
A semi-valid header seems to be `0x64, 0x61, 0x74, 0x0, 0x20, 0x0, 0x0, 0x0` on the first 8 bytes. If the game noticed an invalid Checksum, it does store it as `0x2A, 0x2A, 0x2A, 0x0, 0x0, 0x0, 0x0, 0x0` instead. NOTE: DO NOT MODIFY THIS AT ALL! Otherwise it would not display the Slot either. It *MUST* be always `0x64, 0x61, 0x74, 0x0, 0x20, 0x0, 0x0, 0x0` to be detected.