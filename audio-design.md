---
description: >-
  This section will describe the background music of the game, atmosphere, and
  other sound effects including the visualization of environmental sound
  effects.
---

# Audio Design

## Background Music

The game will have a calm theme that changes depending on the current state of the game or the player. The music should tell the player what state they are in or what they should feel. It also is a subtle indicator for saying if there is a player that is hiding behind a bush or right behind their back \(like the sixth sense that humans have\).

The music will mainly change based on the following states

* Calm - default state. The player is finding a spot to hide or is already hiding safely \(keywords: calm, slow, chime, safe, warm, glad\)
* Calm Nervous - the other player is inside the player’s view \(keywords: slow, low, dark, doubt, shadow\)
* Nervous - `isCrawling && playerIsNear` \(keywords: nervus, increasing tempo, unsafe, wanting to run, trapped, hopeless\)
* Exciting - `isRunning && playeroIsNear` \(keywords: fast, nervus, unsafe, beat, escape, exciting, narrow, searching\)

The base music itself will not change, but instead, each state will add another instrument to the existing base music, making it flow naturally.

## Sound Effect

The sound effect is one of the most important aspects of the game as it is related to the balance and the atmosphere of the game. There will be too many sound effects to write in this document, so I will only focus on describing the types of sound effects that are required in this game.

* Player footsteps \(tile surface sound\) \(walking and running will only change the pitch of the sound\)
* Throwable object sounds
* Background sounds \(wind, fire crackle, leaf moving, etc.\)
* Catching other player sounds

