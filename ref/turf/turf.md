## turf


Turfs cover the surface of the map. They are derived from
`/turf` which derives from `/atom`. 

This example defines the
turf prototype `/turf/floor` and `/turf/wall`.
### Example:

``` dm
 turf floor desc = \"A wood plank floor.\" wall desc = \"A
stone wall.\" density = 1 
```
 

Turfs cannot be moved.
They can only be created or destroyed by changing `world.maxx`,
`world.maxy`, or `world.maxz`. When you create a new turf with `new()`,
it always replaces the old one.
### Example:

``` dm
 // replace old_turf with a wall var/turf/wall/T =
new(old_turf) 
```


> [!TIP] 
> **See also:**
> +   [atom](/ref/atom.md) 
> +   [procs (turf)](/ref/turf/proc.md) 
> +   [vars (turf)](/ref/turf/var.md) 
> +   [Map](/ref/map.md) 