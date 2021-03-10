---
category: GBA
lang: en-US
layout: wiki
section: sims2-research
title: Slot Structure
---

## Notes
Checkout the other pages for notes about the listed Structures.

Sizes marked with `0x8/9` means, the exact size is not 100% known yet.

### GBASLOT
{% capture GBASlot %}
| Offset          | Datatype          | Size     | Content                                  |
| --------------- | ----------------- | -------- | ---------------------------------------- |
| 0x0 - 0xFFF     |                   | 0x1000   | Slot Size                                |
|                 |                   |          |                                          |
| 0x0 - 0x1       | uint8_t           | 0x2      | Unknown                                  |
| 0x2 - 0x3       | uint16_t          | 0x2      | Timestamp (0x2: Hour, 0x3: Minute)       |
| 0x4 - 0x5       | uint8_t           | 0x2      | Unknown                                  |
| 0x6 - 0x9       | uint32_t          | 0x4      | Simoleons (999.999 Seems to be the max)  |
| 0xA - 0xB       | uint16_t          | 0x2      | Ratings (9999 seems to be the max?)      |
| 0xC - 0xC       | uint8_t           | 0x1      | Unknown                                  |
| 0xD - 0x14      | char              | 0x8      | Sim Name (8 Characters ASCII)            |
| 0x15 - 0xFB     | uint8_t           | 0xE7     | Unknown                                  |
| 0xFC - 0xFC     | uint8_t           | 0x1      | Empty Chug-Chug Cola Can Amount          |
| 0xFD - 0xFD     | uint8_t           | 0x1      | Cowbells Amount                          |
| 0xFE - 0xFE     | uint8_t           | 0x1      | Alien Spaceship Parts Amount             |
| 0xFF - 0xFF     | uint8_t           | 0x1      | Nuclear Fuelrods Amount                  |
| 0x100 - 0x112   | uint8_t           | 0x13     | Unknown                                  |
| 0x10A - 0x113   | Episode_Struct    | 0xA      | Buried By the Mob Episode                |
| 0x114 - 0x11D   | Episode_Struct    | 0xA      | What Digs Beneath Episode                |
| 0x11E - 0x122   | Episode_Struct    | 0x5      | The Doomed Earth Episode                 |
| 0x123 - 0x127   | Episode_Struct    | 0x5      | Blackout Episode                         |
| 0x128 - 0x12C   | Episode_Struct    | 0x5      | Aliens Arrived Episode                   |
| 0x12D - 0x136   | Episode_Struct    | 0xA      | The New Cola Episode                     |
| 0x137 - 0x145   | Episode_Struct    | 0xF      | A Brand New Scent Episode                |
| 0x146 - 0x14F   | Episode_Struct    | 0xA      | Triassic Trouble Episode                 |
| 0x150 - 0x16D   | Episode_Struct    | 0x1E     | There Was This Mummy Episode             |
| 0x16E - 0x172   | Episode_Struct    | 0x5      | A Very Special Reunion Episode           |
| 0x173 - 0x177?  | Episode_Struct    | 0x5?     | It All Came to an End Episode            |
| 0x178 - 0x3EF   | uint8_t           | 0x288    | Unknown                                  |
| 0x3F0 - 0x3F8   | SocialMove_Struct | 0x8/9    | Chit Chat Social Move                    |
| 0x3F8 - 0x400   | SocialMove_Struct | 0x8/9    | Entertain Social Move                    |
| 0x400 - 0x408   | SocialMove_Struct | 0x8/9    | Hug Social Move                          |
| 0x408 - 0x410   | SocialMove_Struct | 0x8/9    | Brag Social Move                         |
| 0x410 - 0x418   | SocialMove_Struct | 0x8/9    | Apologize Social Move                    |
| 0x418 - 0x420   | SocialMove_Struct | 0x8/9    | Sweet Talk Social Move                   |
| 0x420 - 0x428   | SocialMove_Struct | 0x8/9    | Flirt Social Move                        |
| 0x428 - 0x430   | SocialMove_Struct | 0x8/9    | Blow Kiss Social Move                    |
| 0x430 - 0x438   | SocialMove_Struct | 0x8/9    | Kiss Social Move                         |
| 0x438 - 0x440   | SocialMove_Struct | 0x8/9    | Show Off Body Social Move                |
| 0x440 - 0x448   | SocialMove_Struct | 0x8/9    | Annoy Social Move                        |
| 0x448 - 0x450   | SocialMove_Struct | 0x8/9    | Insult Social Move                       |
| 0x450 - 0x458   | SocialMove_Struct | 0x8/9    | Threaten Social Move                     |
| 0x458 - 0x460   | SocialMove_Struct | 0x8/9    | Rude Gesture Social Move                 |
| 0x460 - 0x468   | SocialMove_Struct | 0x8/9    | Karate Moves Social Move                 |
| 0x469 - 0x46B   | uint8_t           | 0x2      | Unknown                                  |
| 0x46C - 0x475   | Cast_Structure    | 0xA      | Emperor Xizzle                           |
| 0x476 - 0x47F   | Cast_Structure    | 0xA      | Burple                                   |
| 0x480 - 0x489   | Cast_Structure    | 0xA      | Ara Fusilli                              |
| 0x48A - 0x493   | Cast_Structure    | 0xA      | Auda Sherif                              |
| 0x494 - 0x49D   | Cast_Structure    | 0xA      | Ava Cadavra                              |
| 0x49E - 0x4A7   | Cast_Structure    | 0xA      | Bigfoot                                  |
| 0x4A8 - 0x4B1   | Cast_Structure    | 0xA      | Frankie Fusilli                          |
| 0x4B2 - 0x4BB   | Cast_Structure    | 0xA      | Dusty Hogg                               |
| 0x4BC - 0x4C5   | Cast_Structure    | 0xA      | Giuseppi Mezzoalto                       |
| 0x4C6 - 0x4CF   | Cast_Structure    | 0xA      | Honest Jackson                           |
| 0x4D0 - 0x4D9   | Cast_Structure    | 0xA      | Jebediah Jerky                           |
| 0x4DA - 0x4E3   | Cast_Structure    | 0xA      | Jimmy the Neck                           |
| 0x4E4 - 0x4ED   | Cast_Structure    | 0xA      | Kayleigh Wintercrest                     |
| 0x4EE - 0x4F7   | Cast_Structure    | 0xA      | Luther L. Bigbucks                       |
| 0x4F8 - 0x501   | Cast_Structure    | 0xA      | Mamma Hogg                               |
| 0x502 - 0x50B   | Cast_Structure    | 0xA      | Misty Waters                             |
| 0x50C - 0x515   | Cast_Structure    | 0xA      | Lord Mole                                |
| 0x516 - 0x51F   | Cast_Structure    | 0xA      | Mummy                                    |
| 0x520 - 0x529   | Cast_Structure    | 0xA      | Optimum Alfred                           |
| 0x52A - 0x533   | Cast_Structure    | 0xA      | Penelope Redd                            |
| 0x534 - 0x53D   | Cast_Structure    | 0xA      | Pepper Pete                              |
| 0x53E - 0x547   | Cast_Structure    | 0xA      | Kent Hackett                             |
| 0x548 - 0x551   | Cast_Structure    | 0xA      | Sancho Paco Panza                        |
| 0x552 - 0x55B   | Cast_Structure    | 0xA      | Tank Grunt                               |
| 0x55C - 0x565   | Cast_Structure    | 0xA      | Tristan Legend                           |
| 0x566 - 0x56F   | Cast_Structure    | 0xA      | Yeti                                     |
| 0x570 - 0xFFD   | uint8_t           | 0xA8E    | Unknown                                  |
| 0xFFE - 0xFFF   | uint16_t          | 0x2      | Checksum                                 |
{% endcapture %}

{{ GBASlot | markdownify }}