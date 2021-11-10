---
description: >-
  This section describes the overall game mechanic, features, and different
  categories of in-game items
---

# Game Mechanics and Features

## Core Game Mechanics

* Cursed One
  * At the start of the game, a random player will be chosen as the Cursed One.
  * The Cursed One must kill a player before the timer runs out. If the Cursed One kills another player, a different player will be randomly chosen as the new Cursed One, and the previous one will turn into a normal player. If the Cursed One fails to kill a player before the timer runs out, that player will be killed and a new player will be randomly chosen as the new Cursed One.
  * The game will last until there is only one player left.
  * Only the Cursed One will know if she is the Cursed One. Other players will not be able to tell who is the Cursed One.
  * Cursed One will always deal bleeding damage to other players. Meaning that even if the Cursed One fails to kill a player in one hit, it will still gradually deal damage to the other player for 5 seconds unless the dying player drinks a healing potion.
  * Cursed One has twice the amount of health and stamina points. Their health points will gradually replenish by 10 points per second after staying idle for 3 seconds.
  * A clean backstab by any players will kill the Cursed One in one hit.
  * A player who has been chosen as the Cursed One will not be chosen as the next Cursed One unless everyone in the game has already become one at least once.
* Line of sight (player view cone)
  * The player will have a visual representation of their character's line of sight via the view cone, which looks like a flashlight, but it's just a visual indicator of what the player can see.
  * Only the view area will be visible. Although the rest of the area is still visually shown, dynamic objects and other interests like other players or items will only be visible within the player's line of sight.
  * There will be other objects that create light around a specified area that work similarly to the character's line of sight.
  * The character's line of sight will not be visible to the other players.
  * The radius of the area light will gradually increase if the player is in a crouching state for more than 5 seconds.
* Health-meter
  * Health is the main player status that determines how much more damage the player can take.
  * Every player has a maximum health of 100.
  * Normal players can only recover their health by using a healing potion.
  * Melee attacks, being hit by a throwable object, and other damage effects can reduce the player's health.
  * If the health value is 0 or less, the player will die.
* Stamina-meter
  * Stamina represents the number of actions the player can do. Certain actions will cost a certain amount of stamina.
  * Every player has maximum stamina of 100.
  * If the player stands in a single location for more than 3 seconds, the stamina value will gradually recover (5 points per second). Players can also recover their stamina by using the healing potion.
  * Running will decrease stamina by 10 points per second.
  * Attacking will cost 40 stamina points.
  * Throwing will cost 20 stamina points.
* Player movement
  * Players can either walk, crouch, or run.
  * Crouching can reduce noise.
  * Running and walking can emit noise.
* Melee attack
  * Players can attack by pressing the attack (throw/use) button.
  * Attacking a player in the back will trigger a "Backstab" which will kill the player in one hit.
  * Attacking the player who is also attacking you will deflect the attack and push both players away by 5 tiles.
  * Players cannot move or perform other actions while the attack animation is playing.
* Consumable items and throwable items
  * The game will have different types of items scattered throughout the map.
  * Players can pick up items by getting close to them. Inventory slots will be limited (6 slots) and players cannot stack items with each other.
  * Throwable items are categorized into Evasive throwables and Offensive throwables. Evasive items generally do not deal damage to other players and it is mainly used to support the player to run away or set traps. Offensive items are focused on dealing damage to other players.
  * Currently, there is only one consumable item which is the healing potion. Consuming the healing potion will completely heal the player's health and stamina.
  * Players can aim or consume the item by pressing the use button (right mouse button on PC).
  * Using the consumable item will consume it immediately. Using the throwable item will enter in aim mode. Pressing the action button (attack) while in aim mode will throw the item.
* Surface types
  * All tiles in the game will have a surface property attached to them. These properties will be read by the player character or the throwable item when it gets in contact with the tile.
  * The surface property includes; surface sound, surface volume (sound wave lifespan), and check if it leaves a footprint or not.
  * The surface sound effect will be different from type to type. Every surface that emits a sound will also emit a visible sound wave, including throwable objects.
  * Some surfaces can leave footprints by the player. Footprints will last forever in the game until the owner of the footprint is dead. In other words, players will only see footprints of players that are still in the game.
* Environmental objects and hiding spots
  * The game will have many environmental objects, props, and hiding spots throughout the map. These objects are meant to blend in with the map environment and it's treated as part of the map that the player can interact with.
  * Hiding spots are environmental objects that the player can hide behind by pressing crouch. If the player stands behind these objects, there will be an icon on top of the player to let them know that they can hide by crouching. Crouching behind this object will make the player invisible to other players until it collides with another player.
* Character class
  * The game will allow the player to choose between multiple classes before the game starts.
  * We will have 3 classes in the beginning, but we will gradually add more playable characters and class skin variants.
  * Different character classes will have different visual effects. Examples include footprints, trap rune effects, teleport effects, etc. However, there won't be any class-based special abilities or other mechanics that affect the gameplay. Characters with different classes will mostly play the same.

## Detailed Mechanics

{% hint style="warning" %}
The content in this section is outdated and will be updated to reflect the latest changes.
{% endhint %}

### "Soul Energy" meter behavior

The player's entire soul energy meter will have a maximum of X, and the default movement degradation will be 5 in n seconds for movement state Y. The countdown will start before the stamina value is reduced.

* Walking -> decreases "Soul Energy" by 5 for every 3 seconds.
* Running -> decreases "Soul Energy" by 5 for every second.
* Sneaking -> decreases "Soul Energy" by 5 for every 5 seconds.

The degradation timer will not reset when the player's state changes. Instead, the new decrease rate will apply to the existing counter. For example, suppose the player was sneaking for 4 seconds and started to walk before the 5-second mark. In that case, the timer will not reset, but instead, check if the current countdown is above the current state's degradation rate and decrease it accordingly. The timer will reset after when the player's stamina has been reduced. Staying idle for 5 seconds will start to increase their "Soul Energy" by 5 every second. However, the "Soul Energy" meter won't passively regenerate if it gets below Z (second part of the meter). However, the player can still run or walk even if it's 0. Every throwable object (or its bonus effects) will have an attack value to it. Being in the area of effect will decrease the player's "Soul Energy" meter by the object's attack value.The character's Soul Energy will also slowly degrade, in a rate equivalent to the player's movement state. The main intention is to encourage players to find more potions, while not incentivizing them to start running arround whenever their Soul Energy level is high. When the sanity-meter is low, it will affect what the player sees and hear. The following are the "Energy meter" values and their debuffs: Below X (second part of the meter) -> Reduce the player's field of view and visually makes the ambient darker. Below Y-> spawn random footstep sound effect with the soundwave outside of the player's view. Below Z (almost empty)-> The player cannot run, and the screen visually gets even darker. Killing another player or drinking a potion can replenish the player's "Soul Energy" meter. After a certain amount of time since the match has started, more potions will start spawning in locations far from the players.

### Melee attack

Attack action and collision: When a player presses the attack button, an attack animation will play throughout the entire attack duration. The attack motion should not be longer than 2 seconds. The attack collider will be set to follow the crystal as the attack animation plays. In terms of system mechanics, this is similar to that of swinging a sword. Players can walk while attacking. However, they won't be able to run or crouch in this state.

Cooldown: At the end of an attack, the player will have 0.7 seconds (adjustable) of action cooldown. Players will not be able to trigger an attack during this interval.

Attack and block: When a player presses the attack button, either an attack or a block will occur, depending on the following circumstances:

1 - Blocking attack

* Condition: both characters are facing each other, and they attack at around the same time (time limit of 1.5).
* Effect: no damage to either of the players. Instead, both of them are pushed back 4 \~ 5 tiles away from each other.

2 - Sneak attack

* Condition: the player attacks an enemy character outside of the enemy's view angle.
* Effect: heavy damage plus pushes the receiving player.

Sneaking and then attacking other players from behind will be a core feature of the game, therefore, it requires rigid balancing. Attacking or blocking should feel natural and satisfying, meaning there shouldn’t be a moment where you are close to a player and nothing happens.

### Throwable objects

There will be multiple throwable objects that can be collected throughout the game. This will be categorized into two major types of throwables:

1 - Offensive:

* Rock: the most basic and common kind of throwable object. This will generate a small amount of noise when landed. If it hits another player; damage = 25.
* Exploding Egg: a rare item that generates an area of effect around where it lands, damaging players who stay inside each second; damage <= 40.

2 - Evasive:

* Slime Egg: When the player throws this item, the egg will crack on the landed area and create a slimy surface that spans through 4 tile radius. Players who walk on this surface cannot run, and their movement speed will be decreased by 50%.
* Trap rune: When this item is thrown, a huge trap object with 4 tiles of space inside will spawn on the area where it was landed. The visual effect of this object will be different depending on the player's class. The trap will have 200 points of health and it can be attacked from both inside and outside of the object. Once the object's health hits 0, the object will be destroyed.
* Teleport Rune: When this item is thrown, the player will be teleported to where the rune lands. it will generate a sound (with sound waves) when the player is teleported. When thrown, the player will turn into light particles, and those particles will move to where the runestone has landed.

Every throwable object that can be thrown by a player and can hit a player will have the following properties:

* bool canStun - if true, players who are hit by this object will be slowed and unable to attack for a small period of time.
* float damage - the amount it will decrease the opponent's "Soul Energy" meter.
* Additional effects - other effects may include splash damage or changing the surface type. This part should be flexible.

## Environmental objects

These are static objects that are part of the map’s environment. Most of them will act as a hiding spot for the player. There will be two major types of environmental objects:

1 - Static:

* Trees
* Large furniture (sofas, beds, bookshelf, etc)
* Buildings
* Campfires

2 - Dynamic (Interactive):

* Stack of books
* Doors

Static objects are game field objects that will be constant throughout the client application. Players can hide behind them but players will not be able to change the state of these objects. Dynamic objects are game field objects with their own state that is synced across different clients in the same stage. For example, if a player opens a door, he will be transported to the house's inside.

### Buildings

The game map will contain several buildings that the players can go inside without a loading screen. The buildings should be walled when the player is outside, but when the player is inside the walls will be hiden and the house interior shown. This process should happen dynamically and prevent buildings from having a loading screen. This can be achieved by placing the roof tileset in a separate grid and toggle them during runtime. All buildings will have only one accesible floor, and within it usually there will be with many obstacles that block the player’s line of sight (usually furniture), providing a certain sense of security. Most buildings will only have one entrance, which makes it the perfect camping spot for other players, also potentially being a good hiding spot too.

![(Figure 1) Building before transition](.gitbook/assets/print7.png)

![(Figure 2) Building after transition](.gitbook/assets/print6.png)

When the player enters a building, the game view will be slightly zoomed into the structure and all the outside environment will be darkened, out which will prevent the player from seeing the exterior while being inside a building. To allow space for the player to move, walls must need to be at least 3 tiles tall, since the character sprites occupy almost 2 tiles in height.
