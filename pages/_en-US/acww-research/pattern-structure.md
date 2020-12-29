---
lang: en-US
layout: wiki
section: acww-research
title: Pattern Structure
---

Here you'll find the structure of the Pattern part from AC:WW.

### NOTE 1:
EUR, USA and JPN have a special character encoding, which i marked with the Datatype `WWChar`. For more about it, look at the Character Encoding part [here](character-encoding).

## Structures
<details>
 <summary>EUR_USA Pattern Struct</summary>

{% capture eur_usa %}
| Offset        | Datatype | Size   | What                     |
| ------------- | -------- | ------ | ------------------------ |
| 0x0 - 0x227   |          | 0x228  | Pattern Size             |
|               |          |        |                          |
| 0x0 - 0x1FF   | uint8_t  | 0x200  | Pattern Image            |
| 0x200 - 0x201 | uint16_t | 0x2    | Creator Town ID          |
| 0x202 - 0x209 | WWChar   | 0x8    | Creator Town Name        |
| 0x20A - 0x20B | uint16_t | 0x2    | Creator Player ID        |
| 0x20C - 0x213 | WWChar   | 0x8    | Creator Player Name      |
| 0x214 - 0x214 | uint8_t  | 0x1    | Creator Player Gender    |
| 0x215 - 0x215 | uint8_t  | 0x1    | Unknown 1                |
| 0x216 - 0x225 | WWChar   | 0xF    | Pattern Name             |
| 0x226 - 0x226 | uint8_t  | 0x1    | See [DesignType_Palette](#designtype_palette) |
| 0x227 - 0x227 | uint8_t  | 0x1    | Unknown 2                |
{% endcapture %}

{{ eur_usa | markdownify }}

</details>

<details>
 <summary>JPN Pattern Struct</summary>

{% capture jpn %}
| Offset        | Datatype | Size   | What                     |
| ------------- | -------- | ------ | ------------------------ |
| 0x0 - 0x227   |          | 0x220  | Pattern Size             |
|               |          |        |                          |
| 0x0 - 0x1FF   | uint8_t  | 0x200  | Pattern Image            |
| 0x200 - 0x201 | uint16_t | 0x2    | Creator Town ID          |
| 0x202 - 0x207 | WWChar   | 0x6    | Creator Town Name        |
| 0x208 - 0x209 | uint16_t | 0x2    | Creator Player ID        |
| 0x20A - 0x21F | WWChar   | 0x6    | Creator Player Name      |
| 0x210 - 0x210 | uint8_t  | 0x1    | Creator Player Gender    |
| 0x211 - 0x211 | uint8_t  | 0x1    | Unknown 1                |
| 0x212 - 0x21B | WWChar   | 0xA    | Pattern Name             |
| 0x21C - 0x21C | uint8_t  | 0x1    | See [DesignType_Palette](#designtype_palette) |
| 0x21D - 0x21F | uint8_t  | 0x3    | Unknown 2                |
{%endcapture%}

{{ jpn | markdownify }}

</details>

<details>
 <summary>KOR Pattern Struct</summary>

{% capture kor %}
| Offset        | Datatype | Size   | Content                  |
| ------------- | -------- | ------ | ------------------------ |
| 0x0 - 0x227   |          | 0x234  | Pattern Size             |
|               |          |        |                          |
| 0x0 - 0x1FF   | uint8_t  | 0x200  | Pattern Image            |
| 0x200 - 0x201 | uint16_t | 0x2    | Creator Town ID          |
| 0x202 - 0x20D | char16_t | 0xC    | Creator Town Name        |
| 0x20E - 0x20F | uint16_t | 0x2    | Creator Player ID        |
| 0x210 - 0x21B | char16_t | 0xC    | Creator Player Name      |
| 0x21C - 0x21C | uint8_t  | 0x1    | Creator Player Gender    |
| 0x21D - 0x21D | uint8_t  | 0x1    | Unknown 1                |
| 0x21E - 0x231 | char16_t | 0x14   | Pattern Name             |
| 0x232 - 0x232 | uint8_t  | 0x1    | See [DesignType_Palette](#designtype_palette)         |
| 0x233 - 0x233 | uint8_t  | 0x1    | Unknown 2                |
{% endcapture %}

{{ kor | markdownify }}

</details>

## DesignType_Palette

| Bit Index | Content    |
| --------- | ---------- |
| 0 - 3     | Palette    |
| 4 - 7     | DesignType |
