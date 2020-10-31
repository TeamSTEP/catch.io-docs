# Development Timeline

## Milestones

Milestones are a major update to the build \(mostly 1.x.0\). Each milestone and its expected contents are as follows.

* 0.0.1a - The very first build of the game. This will mainly consist of
  * Implement a 2D orthogonal top-down perspective control scheme \(movement and view\)
  * Tilemap and visual components
    * Decide on a consistent tileset
    * Add basic 2D tilemap atlas and a test map
    * Implement rule tiles for ground and cliff tiles
    * Add building tilemap and rule tiles \(roof and walls\)
    * Implement tile elevation feature \(stairs and colliders\)
    * Add environmental objects like trees and rocks
    * Implement building wall transition effects
    * Create different stages with different biomes and surfaces
    * Implement player death ragdoll effect
    * Implement various weather system
    * Add player stun visual effect
  * Test-only HUD and GUI
    * Add object throw power bar
    * Add player inventory icon
  * The basic mobile control scheme
    * Add virtual joysticks that map to the player
    * Add craw button
    * Add throw button \(might need several adjustments\)
  * Core mechanics
    * Implement player movement modes \(walking, running, crawling\)
    * Add player movement sound
    * Implement a player tile detection method
    * Add game sound visualization feature
    * Implement throwable objects and throwing mechanic
    * Implement player stun mechanic
    * Implement stun stocking
    * Add character footprint feature
    * Add different surface tiles with different walking sounds
    * Add collectibles into the map
    * Implement last-minute crystal spawning
    * Add melee attack mechanic \(i.e. catch\)
    * Add basic sound effects
      * Walking sound \(for different surfaces\)
      * Object landing sound \(throwable objects\)
  * **Implement network feature**
    * Implement Mirror package https://github.com/vis2k/Mirror
    * Implement a local multiplayer system \(temporary\)
    * Implement sound effect for multiplayer
    * Implement sound visualization for multiplayer
    * Sync object pool for sound effect and footprints
    * Implement player stun mechanic
    * Ensure everything developed on 0.0.1a works in multiplayer
    * Implement RPC commands for player controls and syncing variables
    * Add simple multiplay menu for creating or joining a game session
* 0.1.0a - The first playable build of the game.
  * Network/Game optimization
    * Hide objects outside of the player’s view but make it work seamlessly with multiplayer syncing
    * Optimize for massive tilemaps in-game
    * Openworld optimization
    * DOTS implementation
    * Implement network collider rollback for an accurate collision between server and client
  * Game menus and settings
    * Add a title screen
    * Add the game settings menu
      * Graphics settings
      * Sound settings
      * Control settings
    * Add a simple test-only lobby system \(for local multiplayer\)
      * View local hosts
      * Join room
      * Create room
  * HUD finalization
    * Settle on a final UI design
    * Finalize mobile control UI
    * Add current player number display
    * Add game time left display
  * Music and sounds
    * Implement dynamic sound effect mechanic
    * Add BGM set
    * Add ambient sounds for each biome
    * Add more sound effects with randomized values for more variety

