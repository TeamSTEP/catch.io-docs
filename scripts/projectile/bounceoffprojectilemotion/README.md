# BounceOffProjectileMotion

## Description

This class covers everything related to Bounce-Off-projectile-motion expect the Bounce-Off-ProjectileMotion.

## Properties

| type | name | description |
| :--- | :--- | :--- |
| List&lt;Vector2&gt; | MovePoints | Calculated bounce-off-projectile-motion move-points |

## Constructors Parameters

| type | name | description |
| :--- | :--- | :--- |
| [ProjectileMotion](../projectilemotion/) | projectileMotion | Used when you calcualted bounce-off-projectile-motion \(For example the projectile is used to determine whether it cross a wall\) |
| [BoxCollider2D](https://docs.unity3d.com/ScriptReference/BoxCollider2D.html) | collider2D | Used determine the direction of the hit point when projectile hit the wall |
| int | hitMovePointsIndex | Current Index move-points when projectile hit the wall |

## Public Methods

| return type | name | description |
| :--- | :--- | :--- |
| List&lt;Vector2&gt; | [CalculateMovePoints](calculatemovepoints.md) | Used when you calculate bounce-off-projectile-motion move-points |
| List&lt;Sequence&gt; | [PlayMoveSequences](playmovesequences.md) | Used when you play calculated bounce-off-projectile-motion |

