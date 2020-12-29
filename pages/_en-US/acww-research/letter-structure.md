---
lang: en-US
layout: wiki
section: acww-research
title: Letter Structure
---

Here you'll find the structure of the Letter part from AC:WW.

### NOTE 1:
EUR, USA and JPN have a special encoding, which i marked with the Datatype `WWChar`. For more about it, look at the Encoding part [here](character-encoding).

### NOTE 2:
If send to a villager, the first byte of the Receiver Player ID is the Receiver list index and the second the Villager ID.

## Structures
<details>
 <summary>>EUR_USA LetterStruct</summary>

{% capture eur_usa %}
| Offset        | Datatype | Size  | Content              |
| ------------- | -------- | ----- | -------------------- |
| 0x0 - 0xF3    |          | 0xF4  | Lettersize           |
|               |          |       |                      |
| 0x0 - 0x3     | uint32_t | 0x4   | Padding?             |
| 0x4 - 0x5     | uint16_t | 0x2   | Town ID Receiver     |
| 0x6 - 0xD     | WWChar   | 0x8   | Town Name Receiver   |
| 0xE - 0xF     | uint16_t | 0x2   | Player ID Receiver   |
| 0x10 - 0x17   | WWChar   | 0x8   | Player Name Receiver |
| 0x18 - 0x1B   | uint8_t  | 0x4   | Unknown 1            |
| 0x1C - 0x1D   | uint16_t | 0x2   | Town ID Sender       |
| 0x1E - 0x25   | WWChar   | 0x8   | Town Name Sender     |
| 0x26 - 0x27   | uint16_t | 0x2   | Player ID Sender     |
| 0x28 - 0x2F   | WWChar   | 0x8   | Player Name Sender   |
| 0x30 - 0x33   | uint8_t  | 0x4   | Unknown 2            |
| 0x34 - 0x4B   | WWChar   | 0x18  | Letter Intro Part    |
| 0x4C - 0xCB   | WWChar   | 0x81  | Letter Body Part     |
| 0xCC - 0xEB   | WWChar   | 0x20  | Letter End Part      |
| 0xEC - 0xEC   | uint8_t  | 0x1   | Intro Name Index     |
| 0xED - 0xED   | uint8_t  | 0x1   | Paper ID             |
| 0xEE - 0xEE   | uint8_t  | 0x1   | Letter Flags         |
| 0xEF - 0xEF   | uint8_t  | 0x1   | Unknown 3            |
| 0xF0 - 0xF1   | uint16_t | 0x2   | Attachment Item      |
| 0xF2 - 0xF3   | uint8_t  | 0x2   | Unknown 4            |
{% endcapture %}

{{ eur_usa | markdownify }}

</details>

<details>
 <summary>>JPN LetterStruct</summary>

{% capture jpn %}
| Offset        | Datatype | Size  | Content              |
| ------------- | -------- | ----- | -------------------- |
| 0x0 - 0x8B    |          | 0x8C  | Lettersize           |
|               |          |       |                      |
| 0x0 - 0x3     | uint32_t | 0x4   | Padding?             |
| 0x4 - 0x5     | uint16_t | 0x2   | Town ID Receiver     |
| 0x6 - 0xB     | WWChar   | 0x6   | Town Name Receiver   |
| 0xC - 0xD     | uint16_t | 0x2   | Player ID Receiver   |
| 0xE  - 0x13   | WWChar   | 0x6   | Player Name Receiver |
| 0x14 - 0x17   | uint8_t  | 0x4   | Unknown 1            |
| 0x18 - 0x19   | uint16_t | 0x2   | Town ID Sender       |
| 0x1A - 0x1F   | WWChar   | 0x6   | Town Name Sender     |
| 0x20 - 0x21   | uint16_t | 0x2   | Player ID Sender     |
| 0x22 - 0x27   | WWChar   | 0x6   | Player Name Sender   |
| 0x28 - 0x2B   | uint8_t  | 0x4   | Unknown 2            |
| 0x2C - 0x35   | WWChar   | 0xA   | Letter Intro Part    |
| 0x36 - 0x75   | WWChar   | 0x40  | Letter Body Part     |
| 0x76 - 0x85   | WWChar   | 0x10  | Letter End Part      |
| 0x86 - 0x86   | uint8_t  | 0x1   | Intro Name Index     |
| 0x87 - 0x87   | uint8_t  | 0x1   | Paper ID             |
| 0x88 - 0x88   | uint8_t  | 0x1   | Letter Flags         |
| 0x89 - 0x89   | uint8_t  | 0x1   | Unknown 2            |
| 0x8A - 0x8B   | uint16_t | 0x2   | Attachment Item      |
{% endcapture %}

{{ jpn | markdownify }}

</details>

<details>
 <summary>>KOR LetterStruct</summary>

{% capture kor %}
| Offset        | Datatype | Size  | Content              |
| ------------- | -------- | ----- | -------------------- |
| 0x0 - 0xFF    |          | 0x100 | Lettersize           |
|               |          |       |                      |
| 0x0 - 0x3     | uint32_t | 0x4   | Padding?             |
| 0x4 - 0x5     | uint16_t | 0x2   | Town ID Receiver     |
| 0x6 - 0x11    | char16_t | 0xC   | Town Name Receiver   |
| 0x12 - 0x13   | uint16_t | 0x2   | Player ID Receiver   |
| 0x14 - 0x1F   | char16_t | 0xC   | Player Name Receiver |
| 0x20 - 0x23   | uint8_t  | 0x4   | Unknown 1            |
| 0x24 - 0x25   | uint16_t | 0x2   | Town ID Sender       |
| 0x26 - 0x31   | char16_t | 0xC   | Town Name Sender     |
| 0x32 - 0x33   | uint16_t | 0x2   | Player ID Sender     |
| 0x34 - 0x3F   | char16_t | 0xC   | Player Name Sender   |
| 0x40 - 0x43   | uint8_t  | 0x4   | Unknown 2            |
| 0x44 - 0x57   | char16_t | 0x14  | Letter Intro Part    |
| 0x58 - 0xD7   | char16_t | 0x80  | Letter Body Part     |
| 0xD8 - 0xF7   | char16_t | 0x20  | Letter End Part      |
| 0xF8 - 0xF8   | uint8_t  | 0x1   | Intro Name Index     |
| 0xF9 - 0xF9   | uint8_t  | 0x1   | Paper ID             |
| 0xFA - 0xFA   | uint8_t  | 0x1   | Letter Flags         |
| 0xFB - 0xFB   | uint8_t  | 0x1   | Unknown 3            |
| 0xFC - 0xFD   | uint16_t | 0x2   | Attachment Item      |
| 0xFE - 0xFF   | uint8_t  | 0x2   | Unknown 4            |
{% endcapture %}

{{ kor | markdownify }}

</details>

## Other
<details>
 <summary>>Paper IDs</summary>

{% capture paper %}
| ID     | Name                     |
| ------ | ------------------------ |
| 0x0    | Butterfly Paper          |
| 0x1    | Airmail Paper            |
| 0x2    | New Years Cards          |
| 0x3    | Lacy Paper               |
| 0x4    | Cloudy Paper             |
| 0x5    | Petal Paper              |
| 0x6    | Snowy Paper              |
| 0x7    | Maple Leaf Paper         |
| 0x8    | Lined Paper              |
| 0x9    | Notebook Paper           |
| 0xA    | Flowery Paper            |
| 0xB    | Polka dot Paper          |
| 0xC    | Bottle Paper             |
| 0xD    | Ribbon Paper             |
| 0xE    | Sparkly Paper            |
| 0xF    | Vine Paper               |
| 0x10   | Formal Paper             |
| 0x11   | Snowman Paper            |
| 0x12   | Card Paper               |
| 0x13   | Leopard Paper            |
| 0x14   | Cow Paper                |
| 0x15   | Camouflage Paper         |
| 0x16   | Hamburger Paper          |
| 0x17   | Piano Paper              |
| 0x18   | Nook Paper               |
| 0x19   | Fox Paper                |
| 0x1A   | Birthday Cards           |
| 0x1B   | Four Leaf Paper          |
| 0x1C   | Town Hall Paper          |
| 0x1D   | Tortimer Paper           |
| 0x1E   | Insurance Paper          |
| 0x1F   | Academy Paper            |
| 0x20   | Lovely Paper             |
| 0x21   | Rainbow Paper            |
| 0x22   | Egyptian Paper           |
| 0x23   | Lotus Paper              |
| 0x24   | Tile Paper               |
| 0x25   | Mosaic Paper             |
| 0x26   | Elegant Paper            |
| 0x27   | Town View Paper          |
| 0x28   | Chinese Paper            |
| 0x29   | Ocean Paper              |
| 0x2A   | Industrial Paper         |
| 0x2B   | Fireworks Paper          |
| 0x2C   | Floral Paper             |
| 0x2D   | Mushroom Paper           |
| 0x2E   | Star Paper               |
| 0x2F   | Composer Paper           |
| 0x30   | Bathtub Paper            |
| 0x31   | SMB3 Paper               |
| 0x32   | Cool Paper               |
| 0x33   | Forest Paper             |
| 0x34   | Bubble Paper             |
| 0x35   | Buttercup Paper          |
| 0x36   | Tartan Paper             |
| 0x37   | Plaid Paper              |
| 0x38   | Lemon Lime Paper         |
| 0x39   | Crater Paper             |
| 0x3A   | Bejeweled Paper          |
| 0x3B   | Geometric Paper          |
| 0x3C   | Southwest Paper          |
| 0x3D   | Night Sky Paper          |
| 0x3E   | Chic Paper               |
| 0x3F   | Goldfish Paper           |
{% endcapture %}

{{ paper | markdownify }}

</details>

<details>
 <summary>>Letter Flags</summary>

{% capture letter_flags %}
| Flag  | Content                |
| ----- | ---------------------- |
| 0x0   | Does not exist         |
| 0x1   | Letter Created         |
| 0x2   | Letter Unread          |
| 0x3   | Letter Read            |
| 0x4   | Received Bottle Letter |
| 0x5   | Created Bottle Letter  |
| 0x40  | Letter from Mother     |
{% endcapture %}

{{ letter_flags | markdownify }}

</details>
