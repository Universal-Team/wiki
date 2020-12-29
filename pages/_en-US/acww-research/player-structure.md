---
lang: en-US
layout: wiki
section: acww-research
title: Player Structure
---

Here you'll find the structure of the Player part from AC:WW.

### NOTE 1:
EUR, USA and JPN have a special character encoding, which i marked with the Datatype `WWChar`. For more about it, look at the Character Encoding part [here](character-encoding).

## Structures
<details>
 <summary>EUR_USA Player Struct</summary>

{% capture eur_usa %}
| Offset          | Datatype       | Size     | Content                 |
| --------------- | -------------- | -------- | ----------------------- |
| 0x0 - 0x228B    |                | 0x228C   | Player size             |
|                 |                |          |                         |
| 0x0 - 0x227     | Pattern_Struct | 0x228    | Pattern 1               |
| 0x228 - 0x44F   | Pattern_Struct | 0x228    | Pattern 2               |
| 0x450 - 0x677   | Pattern_Struct | 0x228    | Pattern 3               |
| 0x678 - 0x89F   | Pattern_Struct | 0x228    | Pattern 4               |
| 0x8A0 - 0xAC7   | Pattern_Struct | 0x228    | Pattern 5               |
| 0xAC8 - 0xCEF   | Pattern_Struct | 0x228    | Pattern 6               |
| 0xCF0 - 0xF17   | Pattern_Struct | 0x228    | Pattern 7               |
| 0xF18 - 0x113F  | Pattern_Struct | 0x228    | Pattern 8               |
| 0x1140 - 0x1147 | uint8_t        | 0x8      | Unknown 1               |
| 0x1148 - 0x123B | Letter_Struct  | 0xF4     | Pocket Letter 1         |
| 0x123C - 0x132F | Letter_Struct  | 0xF4     | Pocket Letter 2         |
| 0x1330 - 0x1423 | Letter_Struct  | 0xF4     | Pocket Letter 3         |
| 0x1424 - 0x1517 | Letter_Struct  | 0xF4     | Pocket Letter 4         |
| 0x1518 - 0x160B | Letter_Struct  | 0xF4     | Pocket Letter 5         |
| 0x160C - 0x16FF | Letter_Struct  | 0xF4     | Pocket Letter 6         |
| 0x1700 - 0x17F3 | Letter_Struct  | 0xF4     | Pocket Letter 7         |
| 0x17F4 - 0x18E7 | Letter_Struct  | 0xF4     | Pocket Letter 8         |
| 0x18E8 - 0x19DB | Letter_Struct  | 0xF4     | Pocket Letter 9         |
| 0x19DC - 0x1ACF | Letter_Struct  | 0xF4     | Pocket Letter 10        |
| 0x1AD0 - 0x1AE7 | WWChar         | 0x18     | Default Letter Intro    |
| 0x1AE8 - 0x1AFF | uint8_t        | 0x18     | Unknown 2               |
| 0x1B00 - 0x1B1F | WWChar         | 0x20     | Default Letter End      |
| 0x1B20 - 0x1B20 | uint8_t        | 0x1      | Default Introname Index |
| 0x1B21 - 0x1B21 | uint8_t        | 0x1      | Unknown 3               |
| 0x1B22 - 0x1B23 | uint16_t       | 0x2      | Pocket Item 1           |
| 0x1B24 - 0x1B25 | uint16_t       | 0x2      | Pocket Item 2           |
| 0x1B26 - 0x1B27 | uint16_t       | 0x2      | Pocket Item 3           |
| 0x1B28 - 0x1B29 | uint16_t       | 0x2      | Pocket Item 4           |
| 0x1B2A - 0x1B2B | uint16_t       | 0x2      | Pocket Item 5           |
| 0x1B2C - 0x1B2D | uint16_t       | 0x2      | Pocket Item 6           |
| 0x1B2E - 0x1B2F | uint16_t       | 0x2      | Pocket Item 7           |
| 0x1B30 - 0x1B31 | uint16_t       | 0x2      | Pocket Item 8           |
| 0x1B32 - 0x1B33 | uint16_t       | 0x2      | Pocket Item 9           |
| 0x1B34 - 0x1B35 | uint16_t       | 0x2      | Pocket Item 10          |
| 0x1B36 - 0x1B37 | uint16_t       | 0x2      | Pocket Item 11          |
| 0x1B38 - 0x1B39 | uint16_t       | 0x2      | Pocket Item 12          |
| 0x1B3A - 0x1B3B | uint16_t       | 0x2      | Pocket Item 13          |
| 0x1B3C - 0x1B3D | uint16_t       | 0x2      | Pocket Item 14          |
| 0x1B3E - 0x1B3F | uint16_t       | 0x2      | Pocket Item 15          |
| 0x1B40 - 0x1B43 | uint32_t       | 0x4      | Wallet Amount           |
| 0x1B44 - 0x1C6B | uint8_t        | 0x128    | Unknown 4               |
| 0x1C6C - 0x1D5F | Letter_Struct  | 0xF4     | Future Letter           |
| 0x1D60 - 0x1D62 | uint8_t        | 0x3      | Future Letter D, M, Y   |
| 0x1D63 - 0x21E3 | uint8_t        | 0x481    | Unknown 5               |
| 0x21E4 - 0x21E7 | uint32_t       | 0x4      | Bank Amount             |
| 0x21E8 - 0x2224 | uint8_t        | 0x3D     | Unknown 6               |
| 0x2225 - 0x2225 | uint8_t        | 0x1      | Acorn Festival Acorns   |
| 0x2226 - 0x223B | uint8_t        | 0x16     | Unknown 7               |
| 0x223C - 0x223C | uint8_t        | 0x1      | See [Face_Hairstyle](#face_hairstyle) |
| 0x223D - 0x223D | uint8_t        | 0x1      | See [Tan_HairColor](#tan_haircolor) |
| 0x223E - 0x2275 | uint8_t        | 0x38     | Unknown 8               |
| 0x2276 - 0x2277 | uint16_t       | 0x2      | Town ID                 |
| 0x2278 - 0x227F | WWChar         | 0x8      | Town Name               |
| 0x2280 - 0x2281 | uint16_t       | 0x2      | Player ID               |
| 0x2282 - 0x2289 | WWChar         | 0x8      | Player Name             |
| 0x228A - 0x228A | uint8_t        | 0x1      | Gender                  |
| 0x228B - 0x228B | uint8_t        | 0x1      | Unknown 9               |
{% endcapture %}

{{ eur_usa | markdownify }}

</Details>

<details>
 <summary>JPN Player Struct</summary>

{% capture jpn %}
| Offset          | Datatype       | Size     | Content                 |
| --------------- | -------------- | -------- | ----------------------- |
| 0x0 - 0x1D0F    |                | 0x1D10   | Player size             |
|                 |                |          |                         |
| 0x0 - 0x21F     | Pattern_Struct | 0x220    | Pattern 1               |
| 0x220 - 0x43F   | Pattern_Struct | 0x220    | Pattern 2               |
| 0x440 - 0x65F   | Pattern_Struct | 0x220    | Pattern 3               |
| 0x660 - 0x87F   | Pattern_Struct | 0x220    | Pattern 4               |
| 0x880 - 0xA9F   | Pattern_Struct | 0x220    | Pattern 5               |
| 0xAA0 - 0xCBF   | Pattern_Struct | 0x220    | Pattern 6               |
| 0xCC0 - 0xEDF   | Pattern_Struct | 0x220    | Pattern 7               |
| 0xEE0 - 0x10FF  | Pattern_Struct | 0x220    | Pattern 8               |
| 0x1100 - 0x1107 | uint8_t        | 0x8      | Unknown 1               |
| 0x1108 - 0x1193 | Letter_Struct  | 0x8C     | Pocket Letter 1         |
| 0x1194 - 0x121F | Letter_Struct  | 0x8C     | Pocket Letter 2         |
| 0x1220 - 0x12AB | Letter_Struct  | 0x8C     | Pocket Letter 3         |
| 0x12AC - 0x1337 | Letter_Struct  | 0x8C     | Pocket Letter 4         |
| 0x1338 - 0x13C3 | Letter_Struct  | 0x8C     | Pocket Letter 5         |
| 0x13C4 - 0x144F | Letter_Struct  | 0x8C     | Pocket Letter 6         |
| 0x1450 - 0x14DB | Letter_Struct  | 0x8C     | Pocket Letter 7         |
| 0x14DC - 0x1567 | Letter_Struct  | 0x8C     | Pocket Letter 8         |
| 0x1568 - 0x15F3 | Letter_Struct  | 0x8C     | Pocket Letter 9         |
| 0x15F4 - 0x167F | Letter_Struct  | 0x8C     | Pocket Letter 10        |
| 0x1680 - 0x1689 | WWChar         | 0xA      | Default Letter Intro    |
| 0x168A - 0x1693 | uint8_t        | 0xA      | Unknown 2               |
| 0x1694 - 0x16A3 | WWChar         | 0x10     | Default Letter End      |
| 0x16A4 - 0x16A4 | uint8_t        | 0x1      | Default Introname Index |
| 0x16A5 - 0x16A5 | uint8_t        | 0x1      | Unknown 3               |
| 0x16A6 - 0x16A7 | uint16_t       | 0x2      | Pocket Item 1           |
| 0x16A8 - 0x16A9 | uint16_t       | 0x2      | Pocket Item 2           |
| 0x16AA - 0x16AB | uint16_t       | 0x2      | Pocket Item 3           |
| 0x16AC - 0x16AD | uint16_t       | 0x2      | Pocket Item 4           |
| 0x16AE - 0x16AF | uint16_t       | 0x2      | Pocket Item 5           |
| 0x16B0 - 0x16B1 | uint16_t       | 0x2      | Pocket Item 6           |
| 0x16B2 - 0x16B3 | uint16_t       | 0x2      | Pocket Item 7           |
| 0x16B4 - 0x16B5 | uint16_t       | 0x2      | Pocket Item 8           |
| 0x16B6 - 0x16B7 | uint16_t       | 0x2      | Pocket Item 9           |
| 0x16B8 - 0x16B9 | uint16_t       | 0x2      | Pocket Item 10          |
| 0x16BA - 0x16BB | uint16_t       | 0x2      | Pocket Item 11          |
| 0x16BC - 0x16BD | uint16_t       | 0x2      | Pocket Item 12          |
| 0x16BE - 0x16BF | uint16_t       | 0x2      | Pocket Item 13          |
| 0x16C0 - 0x16C1 | uint16_t       | 0x2      | Pocket Item 14          |
| 0x16C2 - 0x16C3 | uint16_t       | 0x2      | Pocket Item 15          |
| 0x16C4 - 0x16C7 | uint32_t       | 0x4      | Wallet Amount           |
| 0x16C8 - 0x1C6F | uint8_t        | 0x5A8    | Unknown 4               |
| 0x1C70 - 0x1C73 | uint32_t       | 0x4      | Bank Amount             |
| 0x1C74 - 0x1C9D | uint8_t        | 0x2A     | Unknown 5               |
| 0x1C9E - 0x1C9E | uint8_t        | 0x1      | Attic Bed               |
| 0x1C9F - 0x1CB0 | uint8_t        | 0x12     | Unknown 5               |
| 0x1CB1 - 0x1CB1 | uint8_t        | 0x1      | Acorn Festival Acorns   |
| 0x1CB2 - 0x1CC5 | uint8_t        | 0x14     | Unknown 6               |
| 0x1CC6 - 0x1CC6 | uint8_t        | 0x1      | See [Face_Hairstyle](#face_hairstyle) |
| 0x1CC7 - 0x1CC7 | uint8_t        | 0x1      | See [Tan_HairColor](#tan_haircolor) |
| 0x1CC8 - 0x1CFB | uint8_t        | 0x36     | Unknown 7               |
| 0x1CFC - 0x1CFD | uint16_t       | 0x2      | Town ID                 |
| 0x1CFE - 0x1D03 | WWChar         | 0x6      | Town Name               |
| 0x1D04 - 0x1D05 | uint16_t       | 0x2      | Player ID               |
| 0x1D06 - 0x1D0B | WWChar         | 0x6      | Player Name             |
| 0x1D0C - 0x1D0C | uint8_t        | 0x1      | Gender                  |
| 0x1D0D - 0x1D0F | uint8_t        | 0x3      | Unknown 8               |
{% endcapture %}

{{ jpn | markdownify }}
</Details>

<details>
 <summary>KOR Player Struct</summary>

{% capture kor %}
| Offset          | Datatype       | Size     | Content                 |
| --------------- | -------------- | -------- | ----------------------- |
| 0x0 - 0x249B    |                | 0x249C   | Player size             |
|                 |                |          |                         |
| 0x0 - 0x233     | Pattern_Struct | 0x234    | Pattern 1               |
| 0x234 - 0x467   | Pattern_Struct | 0x234    | Pattern 2               |
| 0x468 - 0x69B   | Pattern_Struct | 0x234    | Pattern 3               |
| 0x69C - 0x8CF   | Pattern_Struct | 0x234    | Pattern 4               |
| 0x8D0 - 0xB03   | Pattern_Struct | 0x234    | Pattern 5               |
| 0xB04 - 0xD37   | Pattern_Struct | 0x234    | Pattern 6               |
| 0xD38 - 0xF6B   | Pattern_Struct | 0x234    | Pattern 7               |
| 0xF6C - 0x119F  | Pattern_Struct | 0x234    | Pattern 8               |
| 0x11A0 - 0x11A7 | uint8_t        | 0x8      | Unknown 1               |
| 0x11A8 - 0x12A7 | Letter_Struct  | 0x100    | Pocket Letter 1         |
| 0x12A8 - 0x13A7 | Letter_Struct  | 0x100    | Pocket Letter 2         |
| 0x13A8 - 0x14A7 | Letter_Struct  | 0x100    | Pocket Letter 3         |
| 0x14A8 - 0x15A7 | Letter_Struct  | 0x100    | Pocket Letter 4         |
| 0x15A8 - 0x16A7 | Letter_Struct  | 0x100    | Pocket Letter 5         |
| 0x16A8 - 0x17A7 | Letter_Struct  | 0x100    | Pocket Letter 6         |
| 0x17A8 - 0x18A7 | Letter_Struct  | 0x100    | Pocket Letter 7         |
| 0x18A8 - 0x19A7 | Letter_Struct  | 0x100    | Pocket Letter 8         |
| 0x19A8 - 0x1AA7 | Letter_Struct  | 0x100    | Pocket Letter 9         |
| 0x1AA8 - 0x1BA7 | Letter_Struct  | 0x100    | Pocket Letter 10        |
| 0x1BA8 - 0x1BBB | char16_t       | 0x14     | Default Letter Intro    |
| 0x1BBC - 0x1BCF | uint8_t        | 0x14     | Unknown 2               |
| 0x1BD0 - 0x1BEF | char16_t       | 0x20     | Default Letter End      |
| 0x1BF0 - 0x1BF0 | uint8_t        | 0x1      | Default Introname Index |
| 0x1BF1 - 0x1BF1 | uint8_t        | 0x1      | Unknown 3               |
| 0x1BF2 - 0x1BF3 | uint16_t       | 0x2      | Pocket Item 1           |
| 0x1BF4 - 0x1BF5 | uint16_t       | 0x2      | Pocket Item 2           |
| 0x1BF6 - 0x1BF7 | uint16_t       | 0x2      | Pocket Item 3           |
| 0x1BF8 - 0x1BF9 | uint16_t       | 0x2      | Pocket Item 4           |
| 0x1BFA - 0x1BFB | uint16_t       | 0x2      | Pocket Item 5           |
| 0x1BFC - 0x1BFD | uint16_t       | 0x2      | Pocket Item 6           |
| 0x1BFE - 0x1BFF | uint16_t       | 0x2      | Pocket Item 7           |
| 0x1C00 - 0x1C01 | uint16_t       | 0x2      | Pocket Item 8           |
| 0x1C02 - 0x1C03 | uint16_t       | 0x2      | Pocket Item 9           |
| 0x1C04 - 0x1C05 | uint16_t       | 0x2      | Pocket Item 10          |
| 0x1C06 - 0x1C07 | uint16_t       | 0x2      | Pocket Item 11          |
| 0x1C08 - 0x1C09 | uint16_t       | 0x2      | Pocket Item 12          |
| 0x1C0A - 0x1C0B | uint16_t       | 0x2      | Pocket Item 13          |
| 0x1C0C - 0x1C0D | uint16_t       | 0x2      | Pocket Item 14          |
| 0x1C0E - 0x1C0F | uint16_t       | 0x2      | Pocket Item 15          |
| 0x1C10 - 0x1C13 | uint32_t       | 0x4      | Wallet Amount           |
| 0x1C14 - 0x24DF | uint8_t        | 0x7CC    | Unknown 4               |
| 0x23E0 - 0x23E3 | uint32_t       | 0x4      | Bank Amount             |
| 0x23E4 - 0x2420 | uint8_t        | 0x3D     | Unknown 5               |
| 0x2421 - 0x2421 | uint8_t        | 0x1      | Acorn Festival Acorns   |
| 0x2422 - 0x243B | uint8_t        | 0x1A     | Unknown 6               |
| 0x243C - 0x243C | uint8_t        | 0x1      | See [Face_Hairstyle](#face_hairstyle) |
| 0x243D - 0x243D | uint8_t        | 0x1      | See [Tan_HairColor](#tan_haircolor) |
| 0x243E - 0x247D | uint8_t        | 0x40     | Unknown 7               |
| 0x247E - 0x247F | uint16_t       | 0x2      | Town ID                 |
| 0x2480 - 0x248B | char16_t       | 0xC      | Town Name               |
| 0x248C - 0x248D | uint16_t       | 0x2      | Player ID               |
| 0x248E - 0x2499 | char16_t       | 0xC      | Player Name             |
| 0x249A - 0x249A | uint8_t        | 0x1      | Gender                  |
| 0x249B - 0x249B | uint8_t        | 0x1      | Unknown                 |
{% endcapture %}

{{ kor | markdownify }}

</Details>

### Face_Hairstyle

| Bit Index | Content   |
| --------- | --------- |
| 0 - 3     | Hairstyle |
| 4 - 7     | Facetype  |

### Tan_Haircolor

| Bit Index | Content   |
| --------- | --------- |
| 0 - 3     | Haircolor |
| 4 - 7     | Tan       |
