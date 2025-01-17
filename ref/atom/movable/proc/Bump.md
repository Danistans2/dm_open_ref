## Bump proc (movable atom)

**Format:**
+   Bump(atom/Obstacle)
<!-- -->
**When:**
+   Called when a movement fails due to a dense blockage.
<!-- -->
**Args:**
+   Obstacle: The blocking object.
<!-- -->
**Default action:**
+   If the obstacle is a mob and src is in its group, swap their
    positions. This is only done if the mobs both move by full tiles and
    do not use pixel movement, to preserve the behavior of older games.

> [!TIP] 
> **See also:**
> +   [Move proc (movable atom)](/ref/atom/movable/proc/Move.md) 
> +   [Pixel movement](/ref/%7Bnotes%7D/pixel-movement.md) <!-- -->