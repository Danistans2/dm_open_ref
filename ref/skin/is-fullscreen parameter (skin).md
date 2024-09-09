[]{#/{skin}/param/is-fullscreen}    
## is-fullscreen parameter (skin) {#is-fullscreen-parameter-skin byondver="515"}    
**See also:**    
:   [can-resize parameter](/ref/%7Bskin%7D/param/can-resize.md)    
:   [titlebar parameter](/ref/%7Bskin%7D/param/titlebar.md)    
:   [is-maximized parameter](/ref/%7Bskin%7D/param/is-maximized.md)    
:   [is-minimized parameter](/ref/%7Bskin%7D/param/is-minimized.md)    
:   [size parameter](/ref/%7Bskin%7D/param/size.md)    
:   [outer-size parameter](/ref/%7Bskin%7D/param/outer-size.md)    
:   [screen-pos parameter](/ref/%7Bskin%7D/param/screen-pos.md)    
:   [screen-size parameter](/ref/%7Bskin%7D/param/screen-size.md)    
<!-- -->    
**Applies to:**    
:   [Main](/ref/%7Bskin%7D/control/main.md) (window only)    
<!-- -->    
**Format:**    
:   true/false    
<!-- -->    
**Default value:**    
:   false    
True if the window should be in fullscreen mode. This suppresses    
`can-resize`, `titlebar`, `is-maximized`, and `is-minimized`. They will    
continue to return the values that would apply if fullscreen mode were    
turned off.  