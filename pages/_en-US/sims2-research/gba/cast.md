---
category: GBA
lang: en-US
layout: wiki
section: sims2-research
title: Casts
---

## Notes
You'll have to subtract the offset to `- 0x5` if you are still on the `It All Began` Tutorial Episode for all Casts.

### Cast Structure
{% capture CastStructure %}
| Offset    | DataType | Size | Content                                 |
| --------- | ---------| ---- | --------------------------------------- |
| 0x0 - 0x9 | uint8_t  | 0xA  | Cast Size                               |
|           |          |      |                                         |
| 0x0 - 0x0 | uint8_t  | 0x1  | Friendly Conversation Level ( 0 - 3 )   |
| 0x1 - 0x1 | uint8_t  | 0x1  | Romance Conversation Level ( 0 - 3 )    |
| 0x2 - 0x2 | uint8_t  | 0x1  | Intimidate Conversation Level ( 0 - 3 ) |
| 0x3 - 0x3 | boolean  | 0x1  | Alternative Picture Unlocked State      |
| 0x4 - 0x7 | uint8_t  | 0x4  | Unknown                                 |
| 0x8 - 0x8 | boolean  | 0x1  | Mystery Unlocked State                  |
| 0x9 - 0x9 | uint8_t  | 0x1  | Unknown                                 |
{% endcapture %}

{{ CastStructure | markdownify }}


### Cast List
{% capture CastList %}
| Offset | Cast Name              | Image                                                                       |
| ------ | ---------------------- | --------------------------------------------------------------------------- |
| 0x46C  | Emperor Xizzle         | <img src="/assets/images/s2-research/cast/0.png" width="100" height="100">  |
| 0x476  | Burple                 | <img src="/assets/images/s2-research/cast/1.png" width="100" height="100">  |
| 0x480  | Ara Fusilli            | <img src="/assets/images/s2-research/cast/2.png" width="100" height="100">  |
| 0x48A  | Auda Sherif            | <img src="/assets/images/s2-research/cast/3.png" width="100" height="100">  |
| 0x494  | Ava Cadavra            | <img src="/assets/images/s2-research/cast/4.png" width="100" height="100">  |
| 0x49E  | Bigfoot                | <img src="/assets/images/s2-research/cast/5.png" width="100" height="100">  |
| 0x4A8  | Frankie Fusilli        | <img src="/assets/images/s2-research/cast/6.png" width="100" height="100">  |
| 0x4B2  | Dusty Hogg             | <img src="/assets/images/s2-research/cast/7.png" width="100" height="100">  |
| 0x4BC  | Giuseppi Mezzoalto     | <img src="/assets/images/s2-research/cast/8.png" width="100" height="100">  |
| 0x4C6  | Honest Jackson         | <img src="/assets/images/s2-research/cast/9.png" width="100" height="100">  |
| 0x4D0  | Jebediah Jerky         | <img src="/assets/images/s2-research/cast/10.png" width="100" height="100"> |
| 0x4DA  | Jimmy the Neck         | <img src="/assets/images/s2-research/cast/11.png" width="100" height="100"> |
| 0x4E4  | Kayleigh Wintercrest   | <img src="/assets/images/s2-research/cast/12.png" width="100" height="100"> |
| 0x4EE  | Luthor L. Bigbucks     | <img src="/assets/images/s2-research/cast/13.png" width="100" height="100"> |
| 0x4F8  | Mamma Hogg             | <img src="/assets/images/s2-research/cast/14.png" width="100" height="100"> |
| 0x502  | Misty Waters           | <img src="/assets/images/s2-research/cast/15.png" width="100" height="100"> |
| 0x50C  | Lord Mole              | <img src="/assets/images/s2-research/cast/16.png" width="100" height="100"> |
| 0x516  | Mummy                  | <img src="/assets/images/s2-research/cast/17.png" width="100" height="100"> |
| 0x520  | Optimum Alfred         | <img src="/assets/images/s2-research/cast/18.png" width="100" height="100"> |
| 0x52A  | Penelope Redd          | <img src="/assets/images/s2-research/cast/19.png" width="100" height="100"> |
| 0x534  | Pepper Pete            | <img src="/assets/images/s2-research/cast/20.png" width="100" height="100"> |
| 0x53E  | Kent Hackett           | <img src="/assets/images/s2-research/cast/21.png" width="100" height="100"> |
| 0x548  | Sancho Paco Panza      | <img src="/assets/images/s2-research/cast/22.png" width="100" height="100"> |
| 0x552  | Tank Grunt             | <img src="/assets/images/s2-research/cast/23.png" width="100" height="100"> |
| 0x55C  | Tristan Legend         | <img src="/assets/images/s2-research/cast/24.png" width="100" height="100"> |
| 0x566  | Yeti                   | <img src="/assets/images/s2-research/cast/25.png" width="100" height="100"> |
{% endcapture %}

{{ CastList | markdownify }}