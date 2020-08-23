# Inventory

### Description

The class that handles the player inventory system for carrying throwable objects and potions that can be collected throughout the game world.

Item information is stored as Unity Scriptable Objects and referenced in this class as a `ThrowableType` enum.

Inherits from [MonoBehaviour](https://docs.unity3d.com/ScriptReference/MonoBehaviour.html)

Requires:

* Player

### Properties

| type | name | description |
| :--- | :--- | :--- |
| ObserverPattern.Subject | InventorySubject | the inventory subject that is being observed |
| int | MaxInventorySlot | the max number of items the player can carry |

### Public Methods

| return type | name | description |
| :--- | :--- | :--- |
| void | AddObject | adds the throwable object to the inventory list |
| void | RemoveObject | removes the currently selected item from the inventory |
| void | SetSelectIndex | sets the current item the player can is holding with the given inventory index |
| bool | IsEmpty | checks if the inventory is empty or not |
| bool | IsFull | checks if the inventory is full or not |
| List&lt;ThrowableObject&gt; | GetInventoryObjects | list of all the items that are inside the inventory |
| System.Action | GetThrowableObjectEffect | returns the custom effect of the holding object |
| ThrowableType | GetThrowableObjectType | returns the type of throwable the player is holding right now |
| ThrowableObject | GetThrowableObject | returns the throwable object class of the object that the player is currently holding |
| int | GetSelectedIndex | returns the index of the item that the player is holding |

