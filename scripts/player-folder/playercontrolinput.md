# PlayerControlInput

### Description

The class for handling user input to player behavior actions.

Inherits from [MonoBehaviour](https://docs.unity3d.com/ScriptReference/MonoBehaviour.html)

Requires:

* Player

### Properties

| type | name | description |
| :--- | :--- | :--- |
| ObserverPattern.Subject | CatchButtonSubject | observes catch button changes |
| Joystick | RotateJoystick | the joystick instance for mobile controls |
| bool | ThrowMode | the player is in throw mode or not |
| bool | CanCatch | the player can catch other player or not |

### Public Methods

| return type | name | description |
| :--- | :--- | :--- |
| void | PlayerCatch | calls the player catch method when the player can catch other players and is pressing the catch key |
| void | MobileCursorPosition | translates joystick position information to PC curser information |

