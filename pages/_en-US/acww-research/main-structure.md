---
lang: en-US
layout: wiki
section: acww-research
title: Main Structure
---

Here you'll find the structure of the Main part from AC:WW.

### NOTE 1:
EUR, USA and JPN have a special character encoding, which i marked with the Datatype `WWChar`. For more about it, look at the Character Encoding part [here](character-encoding).

## Structures
<details>
 <summary>EUR_USA Main Struct</summary>

{% capture eur_usa %}
| Offset          | Datatype        | Size     | Content                 |
| --------------- | --------------- | -------- | ----------------------- |
| 0x0 - 0x15FDF   |                 | 0x15FE0  | Main Save Size          |
|                 |                 |          |                         |
| 0x0 - 0x1       | uint16_t        | 0x2      | See [Gamecode](#gamecode) |
| 0x2 - 0x3       | uint16_t        | 0x2      | Town ID                 |
| 0x4 - 0xB       | WWChar          | 0x8      | Town Name               |
| 0xC - 0x2297    | Player_Struct   | 0x228C   | Player 1                |
| 0x2298 - 0x4523 | Player_Struct   | 0x228C   | Player 2                |
| 0x4524 - 0x67AF | Player_Struct   | 0x228C   | Player 3                |
| 0x67B0 - 0x8A3B | Player_Struct   | 0x228C   | Player 4                |
| 0x8A3C - 0x913B | Villager_Struct | 0x700    | Villager 1              |
| 0x913C - 0x983B | Villager_Struct | 0x700    | Villager 2              |
| 0x983C - 0x9F3B | Villager_Struct | 0x700    | Villager 3              |
| 0x9F3C - 0xA63B | Villager_Struct | 0x700    | Villager 4              |
| 0xA63C - 0xAD3B | Villager_Struct | 0x700    | Villager 5              |
| 0xAD3C - 0xB43B | Villager_Struct | 0x700    | Villager 6              |
| 0xB43C - 0xBB3B | Villager_Struct | 0x700    | Villager 7              |
| 0xBB3C - 0xC23B | Villager_Struct | 0x700    | Villager 8              |
{% endcapture %}

{{ eur_usa | markdownify }}

</details>

<details>
 <summary>JPN Main Struct</summary>

{% capture jpn %}
| Offset          | Datatype        | Size     | Content                 |
| --------------- | --------------- | -------- | ----------------------- |
| 0x0 - 0x12223   |                 | 0x12224  | Main Save Size          |
|                 |                 |          |                         |
| 0x0 - 0x1       | uint16_t        | 0x2      | See [Gamecode](#gamecode) |
| 0x2 - 0x3       | uint16_t        | 0x2      | Town ID                 |
| 0x4 - 0x9       | WWChar          | 0x6      | Town Name               |
| 0xA - 0xB       | uint8_t         | 0x2      | Unknown 1               |
| 0xC - 0x1D1B    | Player_Struct   | 0x1D10   | Player 1                |
| 0x1D1C - 0x3A2B | Player_Struct   | 0x1D10   | Player 2                |
| 0x3A2C - 0x573B | Player_Struct   | 0x1D10   | Player 3                |
| 0x573C - 0x744B | Player_Struct   | 0x1D10   | Player 4                |
| 0x744C - 0x7A0B | Villager_Struct | 0x5C0    | Villager 1              |
| 0x7A0C - 0x7FCB | Villager_Struct | 0x5C0    | Villager 2              |
| 0x7FCC - 0x858B | Villager_Struct | 0x5C0    | Villager 3              |
| 0x858C - 0x8B4B | Villager_Struct | 0x5C0    | Villager 4              |
| 0x8B4C - 0x910B | Villager_Struct | 0x5C0    | Villager 5              |
| 0x910C - 0x96CB | Villager_Struct | 0x5C0    | Villager 6              |
| 0x96CC - 0x9C8B | Villager_Struct | 0x5C0    | Villager 7              |
| 0x9C8C - 0xA24B | Villager_Struct | 0x5C0    | Villager 8              |
{% endcapture %}

{{ jpn | markdownify }}

</details>

<details>
 <summary>KOR Main Struct</summary>

{%capture kor %}
| Offset          | Datatype        | Size     | Content                 |
| --------------- | --------------- | -------- | ----------------------- |
| 0x0 - 0x12223   |                 | 0x12224  | Main Save Size          |
|                 |                 |          |                         |
| 0x0 - 0x1       | uint16_t        | 0x2      | See [Gamecode](#gamecode) |
| 0x2 - 0x3       | uint16_t        | 0x2      | Town ID                 |
| 0x4 - 0xF       | char16_t        | 0xC      | Town Name               |
| 0x10 - 0x13     | uint8_t         | 0x4      | Unknown 1               |
| 0x14 - 0x24AF   | Player_Struct   | 0x249C   | Player 1                |
| 0x24B0 - 0x494B | Player_Struct   | 0x249C   | Player 2                |
| 0x494C - 0x6DE7 | Player_Struct   | 0x249C   | Player 3                |
| 0x6DE8 - 0x9283 | Player_Struct   | 0x249C   | Player 4                |
| 0x9284 - 0x9A6F | Villager_Struct | 0x7EC    | Villager 1              |
| 0x9A70 - 0xA25B | Villager_Struct | 0x7EC    | Villager 2              |
| 0xA25C - 0xAA47 | Villager_Struct | 0x7EC    | Villager 3              |
| 0xAA48 - 0xB233 | Villager_Struct | 0x7EC    | Villager 4              |
| 0xB234 - 0xBA1F | Villager_Struct | 0x7EC    | Villager 5              |
| 0xBA20 - 0xC20B | Villager_Struct | 0x7EC    | Villager 6              |
| 0xC20C - 0xC9F7 | Villager_Struct | 0x7EC    | Villager 7              |
| 0xC9F8 - 0xD1E3 | Villager_Struct | 0x7EC    | Villager 8              |
{% endcapture %}

{{ kor | markdownify}}

</details>

### Gamecode
Byte 0x0 seems to contain a Gamecode or something like that in the savefile, which is listed below.

Byte 0x1 seems to be always 0x0.

| Gamecode | Region   |
| -------- | -------- |
| 0xC5     | Europe   |
| 0x8A     | USA      |
| 0x32     | Japanese |
| 0x32     | Korean   |
