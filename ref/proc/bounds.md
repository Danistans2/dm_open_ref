## bounds proc

<!-- -->
**Format:**
+   bounds(Ref=src, Dist=0)
+   bounds(Ref, x_offset, y_offset, extra_width=0, extra_height=0)
+   bounds(x, y, width, height, z)
<!-- -->
**Returns:**
+   A list of atoms (except areas) within the given bounding box.
<!-- -->
**Args:**
+   Ref: A turf, obj, mob, pixloc, or a pair of pixlocs as two
    arguments.
+   Dist: A number (distance in pixels).
+   x_offset, y_offset: Shifts bounding box position
+   extra_width, extra_height: Adjusts bounding box size
+   x, y, z: Lower left corner of bounding box in absolute coords;
    x=1,y=1 is lower left of map
+   width, height: Size of bounding box in absolute coords


To leave Ref out of the results, use obounds() instead.


Calling bounds() will default to bounds(src,0), if src is a
turf, obj, or mob. This returns all turfs, objs, and mobs (including
src) within src\'s bounding box. If a single pixloc is used for Ref, it
will have no width or height; you can use a pair of pixlocs instead to
get a block between two pixlocs. 

Changing the distance will
return all objects within that distance from the bounding box. E.g.,
bounds(turf,12) will show you everything within 12 pixels of that turf.


An object\'s bounding box can also be offset. bounds(src,-6,0)
shows what src would touching if it moved 6 pixels west.
bounds(turf,-12,-12,24,24) is equivalent to bounds(turf,12). 

In
the final form, bounds() can use absolute coordinates and does not need
an object to be Ref. Absolute coordinates start at 1,1 at the lower left
corner of the map, by tradition. 

Note: A [vector](/ref/vector.md) may
be used in place of any x/y or width/height pair.

> [!TIP] 
> **See also:**
> +   [obounds proc](/ref/proc/obounds.md) 
> +   [pixloc](/ref/pixloc.md) 
> +   [bound_x var (movable atom)](/ref/atom/movable/var/bound_x.md) 
> +   [bound_y var (movable atom)](/ref/atom/movable/var/bound_y.md) 
> +   [bound_width var (movable atom)](/ref/atom/movable/var/bound_width.md) 
> +   [bound_height var (movable atom)](/ref/atom/movable/var/bound_height.md) 
> +   [icon_w var (atom)](/ref/atom/var/icon_w.md) 
> +   [icon_z var (atom)](/ref/atom/var/icon_z.md) 
> +   [step_x var (movable atom)](/ref/atom/movable/var/step_x.md) 
> +   [step_y var (movable atom)](/ref/atom/movable/var/step_y.md) 
> +   [locs list var (movable atom)](/ref/atom/movable/var/locs.md) 
> +   [Pixel movement](/ref/%7Bnotes%7D/pixel-movement.md) 
> +   [bounds var (client)](/ref/client/var/bounds.md) 