---
lang: en-US
layout: wiki
section: acww-research
title: Letter Storage Structure
---
Here you'll find the structure of the Letter Storage part from AC:WW.

The Letter-Storage can be found at the town hall as the option "Save Letter" on the second station. Those Letters are externally handled from the main save.

## Structures
<details>
 <summary>EUR_USA Letter Storage Struct</summary>

{% capture eur_usa %}
| Offset              | Datatype        | Size     | Content                  |
| ------------------- | --------------- | -------- | ------------------------ |
| 0x2E20C - 0x3FFFF   |                 | 0x11DF4  | Letter Storage Size      |
|                     |                 |          |                          |
| 0x2E20C - 0x32987   | Letter_Struct   | 0x477C   | Player 1 with 75 Letters |
| 0x32988 - 0x37103   | Letter_Struct   | 0x477C   | Player 2 with 75 Letters |
| 0x37104 - 0x3B87F   | Letter_Struct   | 0x477C   | Player 3 with 75 Letters |
| 0x3B880 - 0x3FFFB   | Letter_Struct   | 0x477C   | Player 4 with 75 Letters |
| 0x3FFFC - 0x3FFFD   | uint8_t         | 0x2      | Unknown 1                |
| 0x3FFFE - 0x3FFFF   | uint16_t        | 0x2      | Letter Storage Checksum  |
{% endcapture %}

{{ eur_usa | markdownify }}

</details>

<details>
 <summary>JPN Letter Storage Struct</summary>

{% capture jpn %}
| Offset              | Datatype        | Size     | Content                  |
| ------------------- | --------------- | -------- | ------------------------ |
| 0x35BEC - 0x3FFFF   |                 | 0xA414   | Letter Storage Size      |
|                     |                 |          |                          |
| 0x35BEC - 0x384EF   | Letter_Struct   | 0x2904   | Player 1 with 75 Letters |
| 0x384F0 - 0x3ADF3   | Letter_Struct   | 0x2904   | Player 2 with 75 Letters |
| 0x3ADF4 - 0x3D6F7   | Letter_Struct   | 0x2904   | Player 3 with 75 Letters |
| 0x3D6F8 - 0x3FFFB   | Letter_Struct   | 0x2904   | Player 4 with 75 Letters |
| 0x3FFFC - 0x3FFFD   | uint8_t         | 0x2      | Unknown 1                |
| 0x3FFFE - 0x3FFFF   | uint16_t        | 0x2      | Letter Storage Checksum  |
{% endcapture %}

{{ jpn | markdownify }}

</details>

<details>
 <summary>KOR Letter Storage Struct</summary>

{% capture kor %}
| Offset              | Datatype        | Size     | Content                  |
| ------------------- | --------------- | -------- | ------------------------ |
| 0x337FC - 0x3FFFF   |                 | 0xC804   | Letter Storage Size      |
|                     |                 |          |                          |
| 0x337FC - 0x369FB   | Letter_Struct   | 0x3200   | Player 1 with 50 Letters |
| 0x369FC - 0x39BFB   | Letter_Struct   | 0x3200   | Player 2 with 50 Letters |
| 0x39BFC - 0x3CDFB   | Letter_Struct   | 0x3200   | Player 3 with 50 Letters |
| 0x3CDFC - 0x3FFFB   | Letter_Struct   | 0x3200   | Player 4 with 50 Letters |
| 0x3FFFC - 0x3FFFD   | uint8_t         | 0x2      | Unknown 1                |
| 0x3FFFE - 0x3FFFF   | uint16_t        | 0x2      | Letter Storage Checksum  |
{% endcapture %}

{{ kor | markdownify }}

</details>