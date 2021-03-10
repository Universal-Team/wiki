---
category: GBA
lang: en-US
layout: wiki
section: sims2-research
title: Social Moves
---

## Notes
Social Moves seem to start from Offset `(Slot * 0x1000) + 0x3F0` and are 8 - 9(?) byte long.

The Structure *might* be wrong right now, more research needs to be done.

### Social Move Structure
{% capture SocialMoveStructure %}
| Offset    | DataType | Size  | Content                          |
| --------- | ---------| ----- | -------------------------------- |
| 0x0 - 0x8 | uint8_t  | 0x8/9 | Social Move Size                 |
|           |          |       |                                  |
| 0x0 - 0x3 | uint8_t  | 0x4   | Unknown                          |
| 0x4 - 0x4 | uint8_t  | 0x1   | See `Social Move Flags` below    |
| 0x5 - 0x7 | uint8_t  | 0x3   | Unknown                          |
| 0x8 - 0x8 | uint8_t  | 0x1   | See `Social Move Levels` below   |
{% endcapture %}

{{ SocialMoveStructure | markdownify }}

### Social Move List
{% capture SocialMoveList %}
| Offset | Social Move Name | Image                                                                     |
| ------ | ---------------- | ------------------------------------------------------------------------- |
| 0x3F0  | Chit-Chat        | <img src="/assets/images/s2-research/sm/0.png" width="100" height="100">  |
| 0x3F8  | Entertain        | <img src="/assets/images/s2-research/sm/1.png" width="100" height="100">  |
| 0x400  | Hug              | <img src="/assets/images/s2-research/sm/2.png" width="100" height="100">  |
| 0x408  | Brag             | <img src="/assets/images/s2-research/sm/3.png" width="100" height="100">  |
| 0x410  | Apologize        | <img src="/assets/images/s2-research/sm/4.png" width="100" height="100">  |
| 0x418  | Sweet Talk       | <img src="/assets/images/s2-research/sm/5.png" width="100" height="100">  |
| 0x420  | Flirt            | <img src="/assets/images/s2-research/sm/6.png" width="100" height="100">  |
| 0x428  | Blow Kiss        | <img src="/assets/images/s2-research/sm/7.png" width="100" height="100">  |
| 0x430  | Kiss             | <img src="/assets/images/s2-research/sm/8.png" width="100" height="100">  |
| 0x438  | Show Off Body    | <img src="/assets/images/s2-research/sm/9.png" width="100" height="100">  |
| 0x440  | Annoy            | <img src="/assets/images/s2-research/sm/10.png" width="100" height="100"> |
| 0x448  | Insult           | <img src="/assets/images/s2-research/sm/11.png" width="100" height="100"> |
| 0x450  | Threaten         | <img src="/assets/images/s2-research/sm/12.png" width="100" height="100"> |
| 0x458  | Rude Gesture     | <img src="/assets/images/s2-research/sm/13.png" width="100" height="100"> |
| 0x460  | Karate Moves     | <img src="/assets/images/s2-research/sm/14.png" width="100" height="100"> |
{% endcapture %}

{{ SocialMoveList | markdownify }}

### Social Move Flags
{% capture SocialMoveFlags %}
| Value | State    |
| ----- | -------- |
| 0     | Locked   |
| 1     | Unlocked |
| 2     | Blocked  |
{% endcapture %}

{{ SocialMoveFlags | markdownify }}

### Social Move Levels
{% capture SocialMoveLevels %}
| Value | Level    |
| ----- | -------- |
| 0     | Lv. 1    |
| 1     | Lv. 2    |
| 2     | Lv. 3    |
| 3     | Lv. None |
{% endcapture %}

{{ SocialMoveLevels | markdownify }}