# FootprintGenerator

### Description

A script that will generate the footprint object from the Object Pooler class. Footprints are only generated if the player is moving, and if the player is walking on a proper surface type. This class will play the proper sound effect as well. For everything to work properly, the `FootprintGenerato`r must have the `Player` class as its sibling and have the `ObjectPooler`singleton on the game scene.

Inherits from [MonoBehaviour](https://docs.unity3d.com/ScriptReference/MonoBehaviour.html)

### Properties

| type | name | description |
| :--- | :--- | :--- |
| float | GeneratorTime | the time interval for spawning the footprints in seconds |

