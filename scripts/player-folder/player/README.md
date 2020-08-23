# Player

### Description

The main player class that contains all the player attributes, actions, settings, and more. This class does not care about the controls, only the high-level behavior of the player. Controls are handled from a separate class.

Inherits from [MonoBehaviour](https://docs.unity3d.com/ScriptReference/MonoBehaviour.html), IHitable

Requires:

* Rigidbody2D
* PlayerControlInput
* CharacterRenderer
* Inventory
* SortingGroup
* FootprintGenerator

### Properties

| type | name | description |
| :--- | :--- | :--- |
| bool | IsLocalPlayer | a placeholder value for changing player client status |
| float | MoveSpeed | default player walking speed |
| float | RunSpeed | default player running speed |
| float | CrouchingSpeed | default player crouch movement speed |
| float | Speed | current player speed |
| MoveState | PlayerMoveState | movement state that the player is in now |
| float | CatchRadius | catchable distance |
| float | CatchAngle | catchable angle \(area of effect\) |
| TileBase | StandingTile | the tile object that the player is standing on right now |
| Utils.Surface.SurfaceType | CurrentSurface | the surface type that the player is standing now |
| int | LookAngle | the angle in which the player is looking at. This is used for the FOV light |
| int | MoveDirectionAngle | the angle in which the player is heading to. This is different from the view angle |
| Vector2 | LookDirection | where the player is looking at. This is also used for throwing objects and checking if the other player can be caught |
| ProjectileValues | ProjectileValues | used to calculate the projectile motion from other classes |
| int | Elevation | the player elevation level based on their current tile layer |
| PlayerControlInput | PlayerControl | used to disable player controls if the player is caught |
| Inventory | Inventory | inventory instance used to handle item usage system |
| bool | IsStun | player's stun state |
| WaitForSecondsRealtime | StunDelayTime | the duration that the player will stay stunned in seconds |
| bool | IsCaught | if the player is caught or not |
| List&lt;Vector2&gt; | MovePoints | movement points that are used to calculate the projectile motion |
| List&lt;Sequence&gt; | MoveSequences | movement sequences used to execute the projectile motion |
| bool | IsGround | check if the thrown projectile is on the ground or not |

### Public Methods

| return type | name | description |
| :--- | :--- | :--- |
| void | [Move](move.md) | move the player's rigidbody2D instance to the given movement vector |
| void | [LookAt](lookat.md) | sets the player view direction with the given vector. This method is used to set the player sprite direction and the FOV light |
| void | CalculateObjectProjectileMotion | calculates the simulated throw arc from the given landing point |
| void | ThrowObject | throws a projectile in the inventory queue with the given power and direction |
| void | SelectItem | selects the item from the inventory instance with the given index |
| bool | CanCatch | checks if the player can catch another player with the given direction |
| void | Catch | catches the player in the given view direction |
| IEnumerator | RotCoroutine | a test function that will make the player view into different directions |
| void | UpdateCurrentTileInfo | obtains the current tile information from the utility class based on the player's current transform position |
| void | ResetSubject | used to clear observer pattern subjects |
| bool | CanThrow | checks if the player's inventory is empty or not |
| void | SetTrajectoryActive | set if the throwing trajectory preview should be visible or not |
| void | OnHit | invoke the passed action if the player is hit by a projectile |
| void | OnCaught | changes player value when the player is caught |
| void | ProjectileMotion | calculates the simulated projectile arc |

