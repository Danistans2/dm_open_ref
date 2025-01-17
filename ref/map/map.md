## map

**Format:**
+   #include \"mapname.dmm\"


One or more map files may be loaded into the world\'s map.
These are loaded into successive z-levels. If no map files are
specified, the default project map file will be used. This file has the
same name as the project but has the extension .dmm. 

If no map
files are loaded, the world\'s map size is determined by the world
variables maxx, maxy, and maxz. The default content of this map is
determined by the world variables turf and area.
### Example:

``` dm
 #include \"level1.dmm\" #include \"level2.dmm\" #include
\"level3.dmm\" 
```


> [!TIP] 
> **See also:**
> +   [#include directive](/ref/DM/preprocessor/include.md) 
> +   [area var (world)](/ref/world/var/area.md) 
> +   [maxx var (world)](/ref/world/var/maxx.md) 
> +   [turf var (world)](/ref/world/var/turf.md) <!-- -->