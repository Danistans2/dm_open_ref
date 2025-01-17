## step_y var (movable atom) 
###### BYOND Version 490

**Default value:**
+   0


This var defines the position of the atom (in pixels) relative
to its tile, on the y axis. A step_y of 5 means the atom actually is
shown 5 pixels north of the tile\'s southern edge. 

The atom\'s
actual bounding box may not begin at step_y, but can be set even further
in via bound_y. 

Example: A 16×16 smiley face centered in a
32×32 icon should have the following bounds:
-   bound_x = 8
-   bound_y = 8
-   bound_width = 16
-   bound_height = 16


For the smiley to appear at the bottom edge of the tile it is
standing on, it would need a step_y value of -8. A step_y value of 8
takes it all the way to the top edge of the tile. Anything outside of
the range -8 to 8 will have the atom straddling multiple turfs.

> [!TIP] 
> **See also:**
> +   [step_x var (movable atom)](/ref/atom/movable/var/step_x.md) 
> +   [step_size var (movable atom)](/ref/atom/movable/var/step_size.md) 
> +   [bound_y var (movable atom)](/ref/atom/movable/var/bound_x.md) 
> +   [Move proc (movable atom)](/ref/atom/movable/proc/Move.md) 
> +   [locs list var (movable atom)](/ref/atom/movable/var/locs.md) 
> +   [Pixel movement](/ref/%7Bnotes%7D/pixel-movement.md) <!-- -->