---
category: GBA
lang: en-US
layout: wiki
section: sims2-research
title: Episodes
---

## Notes
The Episodes don't seem to have the same Structures. Some have a distance of `0x5`, some of `0xA`, one of `0xF` and even one of `0x1E`. So this page will be a bit different probably compared to the other ones.

Below, there is a `Episode Names` table listed with The base offset, which can be calculated like: `(Slot * 0x1000) + Offset` (While Slot is the SAVSlot ( 1 - 4 )). Then it also lists the size for the episodes, the episode name, it's season and additional notes, if exist.

Below that one are all episodes listed into their own tables from Season 1, Season 2 until Season 3.

## Episodes

### Episode Names
{% capture EpisodeNames %}
| Offset | Size | Episode Name           | Season | Notes                                                         |
| ------ | ---- | ---------------------- | ------ | ------------------------------------------------------------- |
| 0x10A  | 0xA  | Buried By the Mob      | 1      | None                                                          |
| 0x114  | 0xA  | What Digs Beneath      | 1      | None                                                          |
| 0x11E  | 0x5  | The Doomed Earth       | 3      | None                                                          |
| 0x123  | 0x5  | Blackout!              | 2      | None                                                          |
| 0x128  | 0x5  | Aliens Arrived         | 1      | None                                                          |
| 0x12D  | 0xA  | The New Cola           | 2      | None                                                          |
| 0x137  | 0xF  | A Brand New Scent      | 2      | None                                                          |
| 0x146  | 0xA  | Triassic Trouble       | 3      | None                                                          |
| 0x150  | 0x1E | There Was This Mummy   | 2      | None                                                          |
| 0x16E  | 0x5  | A Very Special Reunion | 3      | Unlockable by connecting 2 GBA's with 2 The Sims 2 GBA cards. |
| 0x173  | 0x5? | It All Came to an End  | 3      | None                                                          |
{% endcapture %}

{{ EpisodeNames | markdownify }}


### Buried By the Mob
{% capture BuriedByTheMob %}
| Offset    | DataType | Size | Content                         |
| --------- | ---------| ---- | ------------------------------- |
| 0x0 - 0x9 | uint8_t  | 0xA  | Episode Size                    |
|           |          |      |                                 |
| 0x0 - 0x0 | uint8_t  | 0x1  | Plot Points Completed Rating    |
| 0x1 - 0x1 | uint8_t  | 0x1  | Aspiration Conversations Rating |
| 0x2 - 0x2 | uint8_t  | 0x1  | Hidden Want Completed Rating    |
| 0x3 - 0x3 | uint8_t  | 0x1  | Errand Completed Rating         |
| 0x4 - 0x4 | boolean  | 0x1  | Episode Unlocked State          |
| 0x5 - 0x9 | uint8_t  | 0x5  | Unknown                         |
{% endcapture %}

{{ BuriedByTheMob | markdownify }}

### What Digs Beneath
{% capture WhatDigsBeneath %}
| Offset    | DataType | Size | Content                         |
| --------- | ---------| ---- | ------------------------------- |
| 0x0 - 0x9 | uint8_t  | 0xA  | Episode Size                    |
|           |          |      |                                 |
| 0x0 - 0x0 | uint8_t  | 0x1  | Plot Points Completed Rating    |
| 0x1 - 0x1 | uint8_t  | 0x1  | Aspiration Conversations Rating |
| 0x2 - 0x2 | uint8_t  | 0x1  | Hidden Want Completed Rating    |
| 0x3 - 0x3 | uint8_t  | 0x1  | Errand Completed Rating         |
| 0x4 - 0x4 | boolean  | 0x1  | Episode Unlocked State          |
| 0x5 - 0x9 | uint8_t  | 0x5  | Unknown                         |
{% endcapture %}

{{ WhatDigsBeneath | markdownify }}

### Aliens Arrived
{% capture AliensArrived %}
| Offset    | DataType | Size | Content                         |
| --------- | ---------| ---- | ------------------------------- |
| 0x0 - 0x4 | uint8_t  | 0x5  | Episode Size                    |
|           |          |      |                                 |
| 0x0 - 0x0 | uint8_t  | 0x1  | Plot Points Completed Rating    |
| 0x1 - 0x1 | uint8_t  | 0x1  | Aspiration Conversations Rating |
| 0x2 - 0x2 | uint8_t  | 0x1  | Hidden Want Completed Rating    |
| 0x3 - 0x3 | uint8_t  | 0x1  | Errand Completed Rating         |
| 0x4 - 0x4 | boolean  | 0x1  | Episode Unlocked State          |
{% endcapture %}

{{ AliensArrived | markdownify }}


### Blackout!
{% capture Blackout %}
| Offset    | DataType | Size | Content                         |
| --------- | ---------| ---- | ------------------------------- |
| 0x0 - 0x4 | uint8_t  | 0x5  | Episode Size                    |
|           |          |      |                                 |
| 0x0 - 0x0 | uint8_t  | 0x1  | Plot Points Completed Rating    |
| 0x1 - 0x1 | uint8_t  | 0x1  | Aspiration Conversations Rating |
| 0x2 - 0x2 | uint8_t  | 0x1  | Hidden Want Completed Rating    |
| 0x3 - 0x3 | uint8_t  | 0x1  | Errand Completed Rating         |
| 0x4 - 0x4 | boolean  | 0x1  | Episode Unlocked State          |
{% endcapture %}

{{ Blackout | markdownify }}


### A Brand New Scent
{% capture ABrandNewScent %}
| Offset    | DataType | Size | Content                         |
| --------- | ---------| ---- | ------------------------------- |
| 0x0 - 0xE | uint8_t  | 0xF  | Episode Size                    |
|           |          |      |                                 |
| 0x0 - 0x0 | uint8_t  | 0x1  | Plot Points Completed Rating    |
| 0x1 - 0x1 | uint8_t  | 0x1  | Aspiration Conversations Rating |
| 0x2 - 0x2 | uint8_t  | 0x1  | Hidden Want Completed Rating    |
| 0x3 - 0x3 | uint8_t  | 0x1  | Errand Completed Rating         |
| 0x4 - 0x4 | boolean  | 0x1  | Episode Unlocked State          |
| 0x5 - 0xE | uint8_t  | 0xA  | Unknown                         |
{% endcapture %}

{{ ABrandNewScent | markdownify }}


### The New Cola
{% capture TheNewCola %}
| Offset    | DataType | Size | Content                         |
| --------- | ---------| ---- | ------------------------------- |
| 0x0 - 0x9 | uint8_t  | 0xA  | Episode Size                    |
|           |          |      |                                 |
| 0x0 - 0x0 | uint8_t  | 0x1  | Plot Points Completed Rating    |
| 0x1 - 0x1 | uint8_t  | 0x1  | Aspiration Conversations Rating |
| 0x2 - 0x2 | uint8_t  | 0x1  | Hidden Want Completed Rating    |
| 0x3 - 0x3 | uint8_t  | 0x1  | Errand Completed Rating         |
| 0x4 - 0x4 | boolean  | 0x1  | Episode Unlocked State          |
| 0x5 - 0x9 | uint8_t  | 0x5  | Unknown                         |
{% endcapture %}

{{ TheNewCola | markdownify }}


### There Was This Mummy
{% capture ThereWasThisMummy %}
| Offset     | DataType | Size | Content                         |
| ---------- | ---------| ---- | ------------------------------- |
| 0x0 - 0x1D | uint8_t  | 0x1E | Episode Size                    |
|            |          |      |                                 |
| 0x0 - 0x0  | uint8_t  | 0x1  | Plot Points Completed Rating    |
| 0x1 - 0x1  | uint8_t  | 0x1  | Aspiration Conversations Rating |
| 0x2 - 0x2  | uint8_t  | 0x1  | Hidden Want Completed Rating    |
| 0x3 - 0x3  | uint8_t  | 0x1  | Errand Completed Rating         |
| 0x4 - 0x4  | boolean  | 0x1  | Episode Unlocked State          |
| 0x5 - 0x1D | uint8_t  | 0x19 | Unknown                         |
{% endcapture %}

{{ ThereWasThisMummy | markdownify }}


### Triassic Trouble
{% capture TriassicTrouble %}
| Offset    | DataType | Size | Content                         |
| --------- | ---------| ---- | ------------------------------- |
| 0x0 - 0x9 | uint8_t  | 0xA  | Episode Size                    |
|           |          |      |                                 |
| 0x0 - 0x0 | uint8_t  | 0x1  | Plot Points Completed Rating    |
| 0x1 - 0x1 | uint8_t  | 0x1  | Aspiration Conversations Rating |
| 0x2 - 0x2 | uint8_t  | 0x1  | Hidden Want Completed Rating    |
| 0x3 - 0x3 | uint8_t  | 0x1  | Errand Completed Rating         |
| 0x4 - 0x4 | boolean  | 0x1  | Episode Unlocked State          |
| 0x5 - 0x9 | uint8_t  | 0x5  | Unknown                         |
{% endcapture %}

{{ TriassicTrouble | markdownify }}


### The Doomed Earth
{% capture TheDoomedEarth %}
| Offset    | DataType | Size | Content                         |
| --------- | ---------| ---- | ------------------------------- |
| 0x0 - 0x4 | uint8_t  | 0x5  | Episode Size                    |
|           |          |      |                                 |
| 0x0 - 0x0 | uint8_t  | 0x1  | Plot Points Completed Rating    |
| 0x1 - 0x1 | uint8_t  | 0x1  | Aspiration Conversations Rating |
| 0x2 - 0x2 | uint8_t  | 0x1  | Hidden Want Completed Rating    |
| 0x3 - 0x3 | uint8_t  | 0x1  | Errand Completed Rating         |
| 0x4 - 0x4 | boolean  | 0x1  | Episode Unlocked State          |
{% endcapture %}

{{ TheDoomedEarth | markdownify }}


### It All Came to an End
{% capture ItAllCameToAnEnd %}
| Offset     | DataType | Size | Content                         |
| ---------- | ---------| ---- | ------------------------------- |
| 0x0 - 0x4? | uint8_t  | 0x5? | Episode Size                    |
|            |          |      |                                 |
| 0x0 - 0x0  | uint8_t  | 0x1  | Plot Points Completed Rating    |
| 0x1 - 0x1  | uint8_t  | 0x1  | Aspiration Conversations Rating |
| 0x2 - 0x2  | uint8_t  | 0x1  | Hidden Want Completed Rating    |
| 0x3 - 0x3  | uint8_t  | 0x1  | Errand Completed Rating         |
| 0x4 - 0x4  | boolean  | 0x1  | Episode Unlocked State          |
{% endcapture %}

{{ ItAllCameToAnEnd | markdownify }}


### A Very Special Reunion
{% capture AVerySpecialReunion %}
| Offset    | DataType | Size | Content                         |
| --------- | ---------| ---- | ------------------------------- |
| 0x0 - 0x4 | uint8_t  | 0x5  | Episode Size                    |
|           |          |      |                                 |
| 0x0 - 0x0 | uint8_t  | 0x1  | Plot Points Completed Rating    |
| 0x1 - 0x1 | uint8_t  | 0x1  | Aspiration Conversations Rating |
| 0x2 - 0x2 | uint8_t  | 0x1  | Hidden Want Completed Rating    |
| 0x3 - 0x3 | uint8_t  | 0x1  | Errand Completed Rating         |
| 0x4 - 0x4 | boolean  | 0x1  | Episode Unlocked State          |
{% endcapture %}

{{ AVerySpecialReunion | markdownify }}