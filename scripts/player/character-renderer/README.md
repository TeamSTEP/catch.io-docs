# CharacterRenderer

## Description

Player prefab sprite and animation control script. Everything about the player sprite is handled from this class.

Inherits from [MonoBehaviour](https://docs.unity3d.com/ScriptReference/MonoBehaviour.html)

## Properties

| type | name | description |
| :--- | :--- | :--- |
| string\[\] | staticDirections | static animation clip names |
| string\[\] | runDirections | running animation clip names |
| string\[\] | walkDirections | walking animation clip names |
| string\[\] | crouchDirections | crouching animation clip names |
| string\[\] | crouchStaticDirections | static crouching animation clip names |

## Public Methods

| return type | name | description |
| :--- | :--- | :--- |
| void | [SetDirection](setdirection.md) | changes the animation clip the sprite renderer should play  |
| int | [DirectionToIndex](directiontoindex.md) | converts a Vector2 direction to an index to a slice around a circle |
| int\[\] | AnimatorStringArrayToHashArray | converts a string array to an int \(animator hash\) array |



