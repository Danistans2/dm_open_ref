## underlays var (atom)

<!-- -->
**Default value:**
+   empty list


This is a list of icons which are displayed underneath the
object\'s main icon. Since these are basically the same as overlays, see
[overlays](/ref/atom/var/overlays.md) for more detailed information.


The only real differences between items in the underlays list
vs. the overlays list is that they\'re processed first, and if they use
`FLOAT_LAYER` (or any other negative layer value) they\'ll appear below
the object instead of above it. For this reason, the underlays list
isn\'t used nearly as much as overlays since it\'s easier to throw most
things into the overlays list. 

When multiple turfs are stacked
on top of one another in the map editor, there is actually only one turf
(the topmost) and the rest are all underlays.

> [!TIP] 
> **See also:**
> +   [icon var (atom)](/ref/atom/var/icon.md) 
> +   [list](/ref/list.md) 
> +   [overlays var (atom)](/ref/atom/var/overlays.md) 
> +   [Understanding the renderer](/ref/%7Bnotes%7D/renderer.md) 