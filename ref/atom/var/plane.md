## plane var (atom) 
###### BYOND Version 509

<!-- -->
**Default value:**
+   `FLOAT_PLANE`
<!-- -->
**Possible values:**
+   -10000 to 10000 (integers only), `FLOAT_PLANE+p`


The value of plane overrides layer, and is mainly used for
non-topdown map formats like isometric. Positive values are drawn on
top, and negative values are drawn below. This mostly deprecates
`EFFECTS_LAYER` and `BACKGROUND_LAYER`, but they can still be useful
when using `PLANE_MASTER` for effects (see
[appearance_flags](/ref/atom/var/appearance_flags.md)). 

The
special value `FLOAT_PLANE` can be used for images and overlays, to take
on the plane of the parent atom. Whenever an icon or icon_state is used
directly as an overlay, this is its plane. If there is no parent atom,
the plane is 0.
You can also use `FLOAT_PLANE` as a relative value, so `FLOAT_PLANE+1`
adds 1 to the parent atom\'s plane. This may be useful for some
applications where an object is included in visual contents. The added
value should still be kept in the range of -10000 to 10000, or
preferably much smaller.

> [!TIP] 
> **See also:**
> +   [layer var (atom)](/ref/atom/var/layer.md) 
> +   [appearance_flags var (atom)](/ref/atom/var/appearance_flags.md) 
> +   [vis_contents var (atom)](/ref/atom/var/vis_contents.md) 
> +   [map_format var (world)](/ref/world/var/map_format.md) 
> +   [Understanding the renderer](/ref/%7Bnotes%7D/renderer.md) 