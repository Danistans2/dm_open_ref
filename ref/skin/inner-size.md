## inner-size parameter (skin) 
###### BYOND Version 513

<!-- -->
**Applies to:**
+   [Main](/ref/%7Bskin%7D/control/main.md) 
<!-- -->
**Format:**
+   *width*x*height*


Read-only. 

If the control is a window, this refers to
its current interior size: i.e., not counting titlebar, statusbar,
borders, etc. If it\'s maximized, this will be the true size of the
window interior, as opposed to `size` which is the interior size once
this window is no longer maximized. 

If this control is a pane
and [can-scroll](/ref/%7Bskin%7D/param/can-scroll.md) is true, this is
the size of the display area not including the scrollbars.

> [!TIP] 
> **See also:**
> +   [size parameter](/ref/%7Bskin%7D/param/size.md) 
> +   [outer-size parameter](/ref/%7Bskin%7D/param/outer-size.md) 
> +   [inner-pos parameter](/ref/%7Bskin%7D/param/inner-pos.md) 