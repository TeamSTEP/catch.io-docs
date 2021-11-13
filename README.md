# Introduction

{% hint style="warning" %}
## Disclaimer

This document will incrementally record the game’s development status and will change any of the contents depending on how the team thinks of the project. Because of this, some of the content in this document may be outdated from what the team will actually do with the project.

Everything written here is subject to change with each improvement coming to the project and by no means it’s comprehensive.

For developer reference docs, please check our [developer reference guide](https://devdocs.witchone.io) page.
{% endhint %}

{% hint style="info" %}
## Supporting the Team

If you are interested in this project and want to hear more from us, please consider following our team's [Twitter account](https://twitter.com/teamstepgames).

For people who want to directly support this project or are interested in joining the team, please send us your portfolio to info@teamstep.io, alternatively, you can refer to our [Patreon page](https://www.patreon.com/teamstep) to support our team!
{% endhint %}

## Project Description

![](.gitbook/assets/title-cover.jpg)

**Witch One** (internal project alias: `Catch.io`) is an indie online rotative asymmetric hide-and-seek game. The objective of the game is to be the last player standing from a 15 player randomized round of hide-and-seek. Players can find various items like stones, teleport runes, slime eggs, and others that can help them incapacitate other players or escape from a sticky situation.

The game will randomly choose a "Cursed One" who has to catch a player before the timer runs out. Once the Cursed One catches a player, the caught player will get a game over and a different player will be chosen as the new Cursed One. This process of killing and randomly choosing the Cursed One will repeat until there is only one player left in the game.

Witch One can be broken down into the following game mechanics:

* Melee attack
* Health & stamina
* Throwable items
* Consumable items
* Footprints
* Footstep & sound waves
* FOV & dynamic lights
* Cursed One

Witch One puts the player in a dark environment where every movement will announce your location or allow others to look at your tracks to find you.

Certain surfaces in the game can leave a footprint when the player walks on top of it. This footprint will be in the game until the player gets a game over. Depending on your movement state such as running or walking, your movement can generate a visible sound wave that is visible to players.

But you can also use the tools and items scattered throughout the world to your advantage. You can throw a rock to create a sound wave, you can use a teleport rune to escape from sticky situations, or you can make a sticky situation by throwing a slime egg which will create a slimy surface that will slow down anyone on top.

The items scattered throughout the map can help the player to weaken or trap other players, but none of them will be strong enough to kill another player in one hit. Furthermore, every movement that the player makes will create a visual soundwave that is visible to other players. Certain surfaces will emit a visible sound wave or leave a footprint that will last until that player is out of the game. A single match will consist of 10 \~ 15 players, that will be randomly spawned at a fixed location. Predefined spawn points are used to ensure that no players will ever see each other at the very beginning of the game. Players are only given 6 item slots (with no item stacking), and they will not start with any items.

The development will be done through _Unity 2021.2.2_ and it will stay there until released. The engine version can change if there is a critical bug that the later version addresses.

![(Figure 2) Sound visualization from Mark of the Ninja](.gitbook/assets/1.jpeg)

The overall visual theme will take inspiration from those of a typical medieval fantasy setting but the characters will be based on witches and sorceresses throughout different cultures. Players can choose from a set of classes with visuals that fit these aesthetics and the map will also have the same feel to it. The game currently does not have any magic or skills, but we are planning on adding one-time magic items in a later update if it adds to the gameplay.

![(Figure 3) Sample game scene of current progress](.gitbook/assets/gameplay-demo.gif)

* No account base items (no login required to play if possible)
* No pay-to-win items
* No crunch
* Players are encouraged to hide
* Certain surfaces will generate a visible sound wave or footprints
* Only the player’s K/D stats are recorded on the server
