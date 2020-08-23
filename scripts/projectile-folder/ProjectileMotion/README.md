# ProjectileMotion

## Description

This class covers everything related to projectile-motion except the Bounce-projectile-motion.

## Properties

| type | name | description |
| :--- | :--- | :--- |
| List<Vector2> | MovePoints | Calculated projectile-motion move-points |
| [ProjectileValues](ProjectileValues.md) | ProjectileValues | To calculate projectile-motion values |
| Vector2 | Direction | Direction of startPosition to endPosition |
| float | CurrentPower | Power to calculate movepoints of projectile-motion (Maximum is ProjectileValues.MaxRadius) |
| delegate | FunctionHandler(float = 1.0f) | When projectile is OnGround or OnBounceGround call this function |

## Constructors

| type | name | description |
| :--- | :--- | :--- |
| [CalculateProjectileMotion](CalculateProjectileMotion.md) | calculateProjectileMotion | Used when you have calculated projectile-motion |
| [ProjectileValues](ProjectileValues.md) | projectileValues | Used when you calculate projectile-motion |

## Public Methods

| return type | name | description |
| :--- | :--- | :--- |
| List&lt;Vector2&gt; | [CalculateMovePoints](CalculateMovePoints.md) | Used when you calculate projetile-motion move-points |
| void | [ShowTrajectory](CalculateMovePoints.md) | Used when you show projectile-motion trajectory |
| List&lt;Sequence&gt; | [PlayMoveSequences](CalculateMovePoints.md) | Used when you play calculated projectile-motion |
