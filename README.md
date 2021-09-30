# Introduction

{% hint style="warning" %}
## Disclaimer

This document will incrementally record the game’s development status and will change any of the contents depending on how the team thinks of the project. Because of this, some of the content in this document may be outdated from what the team will actually do with the project.

Everything written here is subject to change with each improvement coming to the project and by no means it’s comprehensive.

For developer reference docs, please check our [developer reference guide](https://devdocs.witchone.io/) page.
{% endhint %}

{% hint style="info" %}
## Supporting the Team

If you are interested in this project and want to hear more from us, please consider following our team's [Twitter account](https://twitter.com/teamstepgames).

For people who want to directly support this project or are interested in joining the team, please send us your portfolio to info@teamstep.io, alternatively, you can refer to our [Patreon page](https://www.patreon.com/teamstep) to support our team!
{% endhint %}

## Project Description

![](.gitbook/assets/title-cover.jpg)

**Witch One** \(internal project alias: `Catch.io`\) is an online top-down PvP stealth action game. The objective of the game is to be the last player standing by sneaking up on other players, use the items you find throughout the map, and go for the fatal blow.

Witch One is inspired by popular battle royale games like PUBG or Fortnite with a twist of stealth and strategy like those from Monster Hunter or Hitman. _There are no guns or high damage weapons that will give other players a winning edge, and there are no closing rings for the stage at the endgame_. Instead, players will gain an advantage based on their strategy. Players should always be aware of their surroundings, as every movement the player makes will alert your location to others. But at the same time, you can track the other player's location by following their footprints.

Witch One can be broken down into the following game mechanics:

* Melee attack
* Soul energy
* Throwable items
* Consumable items
* Footprints
* Footstep & sound waves
* FOV & dynamic lights

The items scattered throughout the map can help the player to weaken or trap other players, but none of them will be strong enough to kill another player in one hit. Furthermore, every movement that the player makes will create a visual soundwave that is visible to other players. Certain surfaces will emit a visible sound wave or leave a footprint that will last until that player is out of the game. A single match will consist of 10 ~ 15 players, that will be randomly spawned at a fixed location. Predefined spawn points are used to ensure that no players will ever see each other at the very beginning of the game. Players are only given 6 item slots \(with no item stacking\), and they will not start with any items.

The development will be done through _Unity 2021.1.19_ and it will stay there until released. The engine version can change if there is a critical bug that the later version addresses.

![\(Figure 2\) Sound visualization from Mark of the Ninja](.gitbook/assets/1.jpeg)

The overall visual theme will take inspiration from those of a typical medieval fantasy setting but the characters will be based on witches and sorceresses throughout different cultures. Players can choose from a set of classes with visuals that fit these aesthetics and the map will also have the same feel to it. The game currently does not have any magic or skills, but we are planning on adding one-time magic items in a later update if it adds to the gameplay.

![\(Figure 3\) Sample game scene of current progress](.gitbook/assets/ezgif-7-8d61cffb887e.gif)

* No account base items \(no login required to play if possible\)
* No pay-to-win items
* No crunch
* Players are encouraged to hide
* Certain surfaces will generate a visible sound wave or footprints
* Only the player’s K/D stats are recorded on the server

