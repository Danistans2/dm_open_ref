## MouseDrop proc (client)

<!-- -->
**Format:**
+   MouseDrop(src_object,over_object,src_location,over_location,src_control,over_control,params)
<!-- -->
**Args:**
+   src_object: the object being dropped
+   over_object: the object under the mouse pointer
+   src_location: the turf, stat panel, grid cell, etc. from where the
    src object was dragged
+   over_location: the turf, stat panel, grid cell, etc. containing the
    object under the mouse pointer
+   src_control: The id of the skin control the object was dragged from
+   over_control: The id of the skin control the object was dropped onto
+   params: other parameters including mouse/keyboard flags, icon
    offsets, etc.; see [mouse handling](/ref/DM/mouse.md) <!-- -->
**Default action:**
+   Call
    object.MouseDrop(over_object,src_location,over_location,src_control,over_control,params).


This is called when a mouse button is released after dragging
an object. The over_object may be null if dropping over a stat panel or
over other empty space. 

The argument format for this verb is:

``` dm
 MouseDrag(src_object as null\|atom in usr.client,\\
over_object as null\|atom in usr.client,\\ src_location as
null\|turf\|text in usr.client,\\ over_location as null\|turf\|text in
usr.client,\\ src_control as text, over_control as text, params as text)

```


> [!TIP] 
> **See also:**
> +   [Click proc (client)](/ref/client/proc/Click.md) 
> +   [DblClick proc (client)](/ref/client/proc/DblClick.md) 
> +   [MouseDown proc (client)](/ref/client/proc/MouseDown.md) 
> +   [MouseDrag proc (client)](/ref/client/proc/MouseDrag.md) 
> +   [MouseDrop proc (atom)](/ref/atom/proc/MouseDrop.md) 
> +   [MouseEntered proc (client)](/ref/client/proc/MouseEntered.md) 
> +   [MouseExited proc (client)](/ref/client/proc/MouseExited.md) 
> +   [MouseMove proc (client)](/ref/client/proc/MouseMove.md) 
> +   [MouseUp proc (client)](/ref/client/proc/MouseUp.md) 
> +   [MouseWheel proc (client)](/ref/client/proc/MouseWheel.md) 
> +   [mouse_pointer_icon var (client)](/ref/client/var/mouse_pointer_icon.md) 
> +   [show_popup_menus var (client)](/ref/client/var/show_popup_menus.md) 