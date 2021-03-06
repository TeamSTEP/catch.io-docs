# ProjectileMotion

### Description

This class covers everything related to projectile-motion except the Bounce-projectile-motion.

### Properties

| type | name | description |
| :--- | :--- | :--- |
| List | MovePoints | Calculated projectile-motion move-points |
| [ProjectileValues](projectilevalues.md) | ProjectileValues | To calculate projectile-motion values |
| Vector2 | Direction | Direction of startPosition to endPosition |
| float | CurrentPower | Power to calculate move points of projectile-motion \(Maximum is ProjectileValues.MaxRadius\) |
| delegate | FunctionHandler\(float = 1.0f\) | When projectile is OnGround or OnBounceGround call this function |

### Constructors

| type | name | description |
| :--- | :--- | :--- |
| CalculateProjectileMotion | calculateProjectileMotion | Used when you have calculated projectile-motion |
| [ProjectileValues](projectilevalues.md) | projectileValues | Used when you calculate projectile-motion |

### Public Methods

| return type | name | description |
| :--- | :--- | :--- |
| List&lt;Vector2&gt; | [CalculateMovePoints](calculatemovepoints.md) | Used when you calculate projectile-motion move-points |
| void | [ShowTrajectory](showtrajectory.md) | Used when you show projectile-motion trajectory |
| List&lt;Sequence&gt; | [PlayMoveSequences](playmovesequences.md) | Used when you play calculated projectile-motion |



