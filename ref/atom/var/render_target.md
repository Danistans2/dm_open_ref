## render_target var (atom)

<!-- -->
**Default value:**
+   null
<!-- -->
**Possible values:**
+   Any non-empty text string


If any icon uses `render_target`, and another icon in the scene
has a matching `render_source`, this icon will be drawn to a temporary
image called a \"slate\", which can be reused mutiple times for faster
drawing and for special effects. 

If the `render_target` value
starts with an asterisk (`"*"`), it will not be drawn on the map, but
will still be drawn to a slate for reuse. 

Other vars that would
normally affect the appearance of this icon, such as `color`,
`transform`, `filters`, `appearance_flags`, etc. are all applied when
drawing to the slate. Additionally, if this object has overlays,
underlays, or visual contents and uses the
[`KEEP_TOGETHER`](/ref/atom/var/appearance_flags.md)  flag to group all of the
icons together, those will also be included in the slate. 

If
the render target is a [`PLANE_MASTER`](/ref/atom/var/appearance_flags.md) 
vars like `pixel_x/y/w/z` will not apply when it is re-drawn as a
`render_source`.
::: note


To use a `render_target`, the object it belongs to must be
within the visible part of the map, or in the HUD, etc., so that it
would be visible to the user under normal circumstances. If not, it will
not be included in the render process and therefore it can\'t be reused
as a `render_source`. 

Additionally, if you use multiple map
controls, a given render target can only be used as a source on the same
map control where it appears. This is because each map is rendered
separately.
:::

> [!TIP] 
> **See also:**
> +   [render_source var (atom)](/ref/atom/var/render_source.md) 
> +   [appearance_flags var (atom)](/ref/atom/var/appearance_flags.md) 
> +   [color var (atom)](/ref/atom/var/color.md) 
> +   [filters var (atom)](/ref/atom/var/filters.md) 
> +   [transform var (atom)](/ref/atom/var/transform.md) 