[]{#/MouseEntered proc (client).md}    
## MouseEntered proc (client)    
**See also:**    
:   [Click proc (client)]/client/proc/Click    
:   [DblClick proc (client)]/client/proc/DblClick    
:   [MouseDrag proc (client)]/client/proc/MouseDrag    
:   [MouseDrop proc (client)]/client/proc/MouseDrop    
:   [MouseEntered proc (atom)]/atom/proc/MouseEntered    
:   [MouseExited proc (client)]/client/proc/MouseExited    
:   [MouseMove proc (client)]/client/proc/MouseMove    
:   [MouseUp proc (client)]/client/proc/MouseUp    
:   [MouseWheel proc (client)]/client/proc/MouseWheel    
:   [mouse_opacity var (atom)]/atom/var/mouse_opacity    
:   [mouse_pointer_icon var (client)]/client/var/mouse_pointer_icon    
:   [show_popup_menus var (client)]/client/var/show_popup_menus    
<!-- -->    
**Format:**    
:   MouseEntered(object,location,control,params)    
<!-- -->    
**Args:**    
:   object: the object under the mouse pointer    
:   location: the turf, stat panel, grid cell, etc. containing the    
    object where it was clicked    
:   control: the name of the skin control involved    
:   params: other parameters including mouse/keyboard flags, icon    
    offsets, etc.; see [mouse handling]/DM/mouse    
<!-- -->    
**Default action:**    
:   Call object.MouseEntered(location,control,params).    
This is called when no mouse buttons are pressed while pointing to the    
object.    
Don\'t define this unless you need it, because it generates extra    
communication that is otherwise avoided. Defining it on only the objects    
that require it reduces overhead.    
The argument format for this verb is: MouseEntered(object as null\|atom    
in usr.client,\\ location as null\|turf\|text in usr.client,\\ control    
as text, params as text)  