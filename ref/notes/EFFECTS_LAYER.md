## EFFECTS_LAYER



This is mostly no longer needed. A negative value for plane is
the preferred way to do show objects in the background. It can still be
used however when you want to rearrange objects in the same plane when
using [PLANE_MASTER](/ref/atom/var/appearance_flags.md) for visual
effects. 

`EFFECTS_LAYER` is a special high value that can be
added to the regular layer of any atom. 

The purpose of this
value is to make an atom appear above any regular atoms. For instance,
in an isometric map if you want to display a character\'s name below
them, it does not make much sense to have nearer objects cover up that
name, so you can tell the name overlay to use
`EFFECTS_LAYER + MOB_LAYER` and it will show up on top of all the normal
icons on the map. This has been somewhat obviated by `plane` but may
still be useful in some cases. 

When using this special layer,
it should be added to the layer an atom normally uses. For instance an
obj should have a layer of `EFFECTS_LAYER + OBJ_LAYER`. 

This
can be mixed with `TOPDOWN_LAYER`, in non-topdown map formats. Anything
in `TOPDOWN_LAYER` will display on top of `EFFECTS_LAYER`, and
`TOPDOWN_LAYER + EFFECTS_LAYER` will be above both. 

This can
also be mixed with `BACKGROUND_LAYER`, which takes priority over
everything else. 

Images or overlays with `FLOAT_LAYER` can be
left alone. They will automatically have the same layer as whatever atom
they are attached to.

> [!TIP] 
> **See also:**
> +   [layer var (atom)](/ref/atom/var/layer.md) 
> +   [plane var (atom)](/ref/atom/var/plane.md) 
> +   [map_format var (world)](/ref/world/var/map_format.md) 
> +   [BACKGROUND_LAYER](/ref/%7Bnotes%7D/BACKGROUND_LAYER.md) 
> +   [TOPDOWN_LAYER](/ref/%7Bnotes%7D/TOPDOWN_LAYER.md) 
> +   [stddef.dm file](/ref/%7B%7Bappendix%7D%7D/stddef%2edm.md) 
> +   [Understanding the renderer](/ref/%7Bnotes%7D/renderer.md) 