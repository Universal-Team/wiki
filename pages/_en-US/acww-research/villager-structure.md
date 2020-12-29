---
lang: en-US
layout: wiki
section: acww-research
title: Village Structure
---

Here you'll find the structure of the Villager part from AC:WW.

### NOTE 1:
EUR, USA and JPN have a special character encoding, which i marked with the Datatype `WWChar`. For more about it, look at the Character Encoding part [here](character-encoding).

## Structures
<details>
 <summary>EUR_USA Villager Struct</summary>

{% capture eur_usa %}
| Offset          | Datatype       | Size     | What                    |
| --------------- | -------------- | -------- | ----------------------- |
| 0x0 - 0x6FF     |                | 0x700 	  | Villager size           |
|                 |                |          |                         |
| 0x0 - 0x33F     | uint8_t        | 0x340    | Unknown 1               |
| 0x340 - 0x567   | Pattern_Struct | 0x228    | Pattern                 |
| 0x568 - 0x65B   | Letter_Struct  | 0xF4     | Letter                  |
| 0x65C - 0x6AB   | uint8_t        | 0x50     | Unknown 2               |
| 0x6AC - 0x6AD   | uint16_t       | 0x2      | Furniture 1             |
| 0x6AE - 0x6AF   | uint16_t       | 0x2      | Furniture 2             |
| 0x6B0 - 0x6B1   | uint16_t       | 0x2      | Furniture 3             |
| 0x6B2 - 0x6B3   | uint16_t       | 0x2      | Furniture 4             |
| 0x6B4 - 0x6B5   | uint16_t       | 0x2      | Furniture 5             |
| 0x6B6 - 0x6B7   | uint16_t       | 0x2      | Furniture 6             |
| 0x6B8 - 0x6B9   | uint16_t       | 0x2      | Furniture 7             |
| 0x6BA - 0x6BB   | uint16_t       | 0x2      | Furniture 8             |
| 0x6BC - 0x6BD   | uint16_t       | 0x2      | Furniture 9             |
| 0x6BE - 0x6BF   | uint16_t       | 0x2      | Furniture 10            |
| 0x6C0 - 0x6C9   | uint8_t        | 0xA      | Unknown 3               |
| 0x6CA - 0x6CA   | uint8_t        | 0x1      | Personality             |
| 0x6CB - 0x6CB   | uint8_t        | 0x1      | ID / Species            |
| 0x6CC - 0x6EB   | uint8_t        | 0x20     | Unknown 4               |
| 0x6EC - 0x6ED   | uint16_t       | 0x2      | Shirt                   |
| 0x6EE - 0x6EE   | uint8_t        | 0x1      | Wallpaper               |
| 0x6EF - 0x6EF   | uint8_t        | 0x1      | Carpet                  |
| 0x6F0 - 0x6F3   | uint8_t        | 0x4      | Unknown 5               |
| 0x6F4 - 0x6F4   | uint8_t        | 0x1      | Umbrella                |
| 0x6F5 - 0x6FF   | uint8_t        | 0xA      | Unknown 6               |
{% endcapture %}

{{ eur_usa | markdownify }}
</details>

<details>
 <summary>JPN Villager Struct</summary>

{% capture jpn %}
| Offset          | Datatype       | Size     | What                    |
| --------------- | -------------- | -------- | ----------------------- |
| 0x0 - 0x5BF     |                | 0x5C0 	  | Villager size           |
|                 |                |          |                         |
| 0x0 - 0x27F     | uint8_t        | 0x280    | Unknown 1               |
| 0x280 - 0x49F   | Pattern        | 0x220    | Pattern                 |
| 0x4A0 - 0x52B   | Letter_Struct  | 0x8C     | Letter                  |
| 0x52C - 0x543   | uint8_t        | 0x18     | Unknown 2               |
| 0x544 - 0x544   | uint8_t        | 0x1      | Umbrella                |
| 0x545 - 0x577   | uint8_t        | 0x33     | Unknown 3               |
| 0x578 - 0x579   | uint16_t       | 0x2      | Furniture 1             |
| 0x57A - 0x57B   | uint16_t       | 0x2      | Furniture 2             |
| 0x57C - 0x57D   | uint16_t       | 0x2      | Furniture 3             |
| 0x57E - 0x57F   | uint16_t       | 0x2      | Furniture 4             |
| 0x580 - 0x581   | uint16_t       | 0x2      | Furniture 5             |
| 0x582 - 0x583   | uint16_t       | 0x2      | Furniture 6             |
| 0x584 - 0x585   | uint16_t       | 0x2      | Furniture 7             |
| 0x586 - 0x587   | uint16_t       | 0x2      | Furniture 8             |
| 0x588 - 0x589   | uint16_t       | 0x2      | Furniture 9             |
| 0x58A - 0x58B   | uint16_t       | 0x2      | Furniture 10            |
| 0x58C - 0x593   | uint8_t        | 0x8      | Unknown 4               |
| 0x594 - 0x594   | uint8_t        | 0x1      | Personality             |
| 0x595 - 0x595   | uint8_t        | 0x1      | ID / Species            |
| 0x596 - 0x5AD   | uint8_t        | 0x18     | Unknown 5               |
| 0x5AE - 0x5AF   | uint16_t       | 0x2      | Shirt                   |
| 0x5B0 - 0x5B0   | uint8_t        | 0x1      | Wallpaper               |
| 0x5B1 - 0x5B1   | uint8_t        | 0x1      | Carpet                  |
| 0x5B2 - 0x5BF   | uint8_t        | 0xE      | Unknown 6               |
{% endcapture %}

{{ jpn | markdownify }}

</details>

<details>
 <summary>KOR Villager Struct</summary>

{% capture kor %}
| Offset          | Datatype       | Size     | What                    |
| --------------- | -------------- | -------- | ----------------------- |
| 0x0 - 0x7EB     |                | 0x7EC 	  | Villager size           |
|                 |                |          |                         |
| 0x0 - 0x3FF     | uint8_t        | 0x400    | Unknown 1               |
| 0x400 - 0x633   | Pattern_Struct | 0x234    | Pattern                 |
| 0x634 - 0x733   | Letter_Struct  | 0x100    | Letter                  |
| 0x734 - 0x78B   | uint8_t        | 0x58     | Unknown 2               |
| 0x78C - 0x78D   | uint16_t       | 0x2      | Furniture 1             |
| 0x78E - 0x78F   | uint16_t       | 0x2      | Furniture 2             |
| 0x790 - 0x791   | uint16_t       | 0x2      | Furniture 3             |
| 0x792 - 0x793   | uint16_t       | 0x2      | Furniture 4             |
| 0x794 - 0x795   | uint16_t       | 0x2      | Furniture 5             |
| 0x796 - 0x797   | uint16_t       | 0x2      | Furniture 6             |
| 0x798 - 0x799   | uint16_t       | 0x2      | Furniture 7             |
| 0x79A - 0x79B   | uint16_t       | 0x2      | Furniture 8             |
| 0x79C - 0x79D   | uint16_t       | 0x2      | Furniture 9             |
| 0x79E - 0x79F   | uint16_t       | 0x2      | Furniture 10            |
| 0x7A0 - 0x7AD   | uint8_t        | 0xE      | Unknown 3               |
| 0x7AE - 0x7AE   | uint8_t        | 0x1      | Personality             |
| 0x7AF - 0x7AF   | uint8_t        | 0x1      | ID / Species            |
| 0x7B0 - 0x7D1   | uint8_t        | 0x22     | Unknown 4               |
| 0x7D2 - 0x7D3   | uint16_t       | 0x2      | Shirt                   |
| 0x7D4 - 0x7D4   | uint8_t        | 0x1      | Wallpaper               |
| 0x7D5 - 0x7D5   | uint8_t        | 0x1      | Carpet                  |
| 0x7D6 - 0x7D9   | uint8_t        | 0x4      | Unknown 5               |
| 0x7DA - 0x7DA   | uint8_t        | 0x1      | Umbrella                |
| 0x7DB - 0x7EB   | uint8_t        | 0x11     | Unknown 6               |
{% endcapture %}

{{ kor | markdownify }}

</details>
