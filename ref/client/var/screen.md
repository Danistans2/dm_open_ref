## screen var (client)


This is a list of objects that are displayed on the user\'s
screen. The object\'s screen_loc variable controls where it appears (if
it appears at all). This allows one to create the elements of a
graphical user interface, with such features as buttons, drag/drop
areas, and stat monitors. 

Screen objects (visible or otherwise)
may also be used to make verbs available to users. To make them
accessible, define verbs on the screen object like this: 
``` dm

set src in usr.client.screen 
```


> [!TIP] 
> **See also:**
> +   [HUD / screen objects](/ref/%7Bnotes%7D/HUD.md) 
> +   [screen_loc var (movable atoms)](/ref/atom/movable/var/screen_loc.md) 