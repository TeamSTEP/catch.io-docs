# Introduction

{% hint style="warning" %}
## Disclaimer

This document will incrementally record the game’s development status and will change any of the contents depending on how the team thinks of the project. Because of this, some of the content in this document may be outdated from what the team will actually do with the project.

Everything written here is subject to change with each improvement coming to the project and by no means it’s comprehensive.

For on-going development progress, please check this Github repository [https://github.com/TeamSTEP/project-witch-one](https://github.com/TeamSTEP/project-witch-one).

For development references, please check our developer reference guide page [https://teamstep.github.io/catch.io-docs/index.html](https://teamstep.github.io/catch.io-docs/index.html).
{% endhint %}

## Project Description

**Witch One** is an online stealth-focused battle-royal. The game's objective is to be the last player standing by either catching other players or hide while they catch each other.

This project is internally code-named Catch.io, so you may find some of our resources calling this project as such.

This project takes inspiration from popular battle-royal games like PUBG or Fortnite but focused on stealthy gameplay and strategy. There are no guns or ranged weapons that can kill the other player. Instead, you can only catch another player by melee attacking them from the back. The player can do this by utilizing different tools and items that are scattered throughout the game map. Every movement that the player makes will create a visual soundwave that is visible to other players. Certain surfaces will leave a footprint that will last until that player is out of the game. And other environmental indicators like an open door or fallen stacks of books to announce your presence.

The game starts by randomly spawning players of 15 ~ 20 within a fixed spawn-point. Predefined spawn-points are done to ensure that no players will ever see each other at the very beginning of the game. Players are only given 6 item slots \(no item stacking\), and they will start with no items on hand. Players will have to be aware of two status values, sanity, and stamina. Stamina will decrease by a certain amount every 5 seconds. When your stamina hits 0, your sanity value will start to drop. And after a certain threshold in your sanity value, you will begin to see soundwaves coming from random places, and your vision will get darker. Players can only catch another player who's sanity level is below a certain amount. Attempting to catch a player with a high sanity value will only push them backward and decrease their sanity and stamina value by a considerable amount. From here, both players are given a tiny window of opportunity to either run away or try to catch them again.

The development will be done through _Unity 2019.4.8f1 LTS_ and it will stay there until released. The engine version can change if there is a critical bug that the later version addresses.

![\(Figure 2\) Sound visualization from Mark of the Ninja](.gitbook/assets/1.jpeg)

The overall visual theme will take inspiration from those of a typical medieval fantasy setting but the characters will be based on witches and sorceresses throughout different cultures. Players can choose from a set of classes with the visuals that fit these aesthetics and the map will also have the same feel to it. The game currently does not have any magic or skills, but we are planning on adding one-time magic items in a later update if it adds to the gameplay.

![\(Figure 3\) Sample game scene of current progress](.gitbook/assets/ezgif-7-8d61cffb887e.gif)

* No account base items \(no login required to play if possible\)
* No pay-to-win items
* Player strategies are determined by the map layout, hiding spots, and throwable objects
* Certain surfaces can either generate loud sound or footprints
* Only the player’s K/D stats are recorded on the server

