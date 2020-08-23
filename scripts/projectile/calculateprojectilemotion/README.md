# CalculateProjectileMotion

### Description

This class to use when i need calculate projectile-motion and projectile bounce off the wall. Just calculate and show trajectory projectile-motion.

Inherits from [MonoBehaviour](https://docs.unity3d.com/ScriptReference/MonoBehaviour.html)

Requires:

* SpriteRenderer \(InChild\)
* BoxCollider2D \(InChild\)
* Player \(InParent\)

### Properties

| type | name | description |
| :--- | :--- | :--- |
| ThrowableObject | CurrentThrowableObject | Current throwable object information |
| ProjectileValues | ProjectileValues | Player Projectile Value |
| ProjectileMotion | CurrentProjectileMotion | Current Projectile motion to calculate move-points |
| List&lt;Vector2&gt; | MovePoints | Calculated move-points \(This value must be calculate before you use this\) |

### Public Methods

| return type | name | description |
| :--- | :--- | :--- |
| void | [CalculateObjectMovePoints](CalculateObjectMovePoints.md) | Calculate object projectile-motion move-points |
| void | [ShowTrajectory](ShowTrajectory.md) | Show projectile-motion move-points trajectory |
| void | [CalculatePlayerMovePoints](CalculatePlayerMovePoints.md) | Calculate Player projectile-motion move-points |

