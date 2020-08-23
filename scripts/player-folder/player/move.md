# Move

`public void Move(Vector2 inputVector, MoveState moveState)`

### Description

moves the player game object to the given direction with the given speed. This will set the player's movement angle as well which is used for the catch function. Moving the object is done by using the `MovePosition` method in the RigidBody2D.

### Parameters

| type | name | description |
| :--- | :--- | :--- |
| Vector2 | inputVector | the movement vector for where the player will move to |
| MoveState | moveState | the movement state the player is in |

