## TOPDOWN_LAYER


TOPDOWN_LAYER is a special high value that can be added to the
regular layer of any atom. This is only available when using a
non-topdown world.map_format, such as isometric mapping. 

The
purpose of this value is to make an atom appear as if it belongs in a
top-down map, when using a map_format other than TOPDOWN_MAP or
TILED_ICON_MAP. This can be handy for title screens, or for special
battle maps or the inside of a building in an RPG. 

When using
this special layer, it should be added to the layer an atom normally
uses. For instance a turf should have a layer of TOPDOWN_LAYER +
TURF_LAYER. Usually you will want one part of the map to have
TOPDOWN_LAYER, and for players to be unable to walk to there from the
regular map. Mixing topdown icons and icons in the normal map_format in
view of each other could look very strange. For safety\'s sake, the
easiest thing to do is to keep them on separate z layers. 

This
can be mixed with EFFECTS_LAYER. Anything in TOPDOWN_LAYER will display
on top of EFFECTS_LAYER, and TOPDOWN_LAYER + EFFECTS_LAYER will be above
both. 

This can also be mixed with BACKGROUND_LAYER, which takes
priority over everything else. 

Images or overlays with
FLOAT_LAYER can be left alone. They will automatically have the same
layer as whatever atom they are attached to.

> [!TIP] 
> **See also:**
> +   [layer var (atom)](/ref/atom/var/layer.md) 
> +   [map_format var (world)](/ref/world/var/map_format.md) 
> +   [BACKGROUND_LAYER](/ref/%7Bnotes%7D/BACKGROUND_LAYER.md) 
> +   [EFFECTS_LAYER](/ref/%7Bnotes%7D/EFFECTS_LAYER.md) 
> +   [stddef.dm file](/ref/%7B%7Bappendix%7D%7D/stddef%2edm.md) 