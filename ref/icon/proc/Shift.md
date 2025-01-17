## Shift proc (icon)

**Format:**
+   Shift(dir,offset,wrap=0)
<!-- -->
**Args:**
+   dir: direction in which to shift the icon
+   offset: distance to shift the pixels
+   wrap: if true, causes shifted pixels to wrap around to the other
    side


This moves all of the pixels by the specified amount in a
direction. For example, Shift(NORTH,1) would move everything one pixel
to the north. 

By default, pixels that move off the edge are not
wrapped around; transparent pixels are shifted onto the other side.
Calling with wrap=1 causes it to shift the pixels around to the other
side.

> [!TIP] 
> **See also:**
> +   [dir var (atom)](/ref/atom/var/dir.md) 
> +   [icon](/ref/icon.md) 
> +   [procs (icon)](/ref/icon/proc.md) <!-- -->