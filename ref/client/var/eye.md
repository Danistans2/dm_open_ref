## eye var (client)

**Default value:**
+   The connected mob, client.mob.


This value determines the center of the player\'s map. The
default value simply means that the visible region is normally centered
on the player\'s mob. Effects such as setting `perspective` to
`EDGE_PERSPECTIVE` or using `lazy_eye` can move the map off-center
temporarily. The eye is the *ideal* center, not necessarily the actual
center; to find the actual center, use `virtual_eye`. 

The
eye\'s step_x/y vars, if present, are also used to allow smooth
scrolling of the map. These also obey lazy_eye and edge_limit.


Note that the visibility of objects is still computed from the
point of view of the mob rather than the eye. This allows the use of
`lazy_eye` or similar effects that control the panning of the map while
still having the player see only what the mob can see. To determine
visibility from the eye, you can change the value of
`client.perspective`. 

If a player connects to a new mob M,
client.eye automatically changes to M.
### Example:

``` dm
 client eye = locate(5,5,1) 
```
 

This fixes
the center of the player\'s map at the turf coordinate (5,5,1). Since
the eye is fixed, the map will not scroll even as the player\'s mob
moves out of the visible range.

> [!TIP] 
> **See also:**
> +   [edge_limit var (client)](/ref/client/var/edge_limit.md) 
> +   [lazy_eye var (client)](/ref/client/var/lazy_eye.md) 
> +   [mob var (client)](/ref/client/var/mob.md) 
> +   [perspective var (client)](/ref/client/var/perspective.md) 
> +   [glide_size var (client)](/ref/client/var/glide_size.md) 
> +   [view var (client)](/ref/client/var/view.md) 
> +   [virtual_eye var (client)](/ref/client/var/virtual_eye.md) 
> +   [view var (world)](/ref/world/var/view.md) 
> +   [step_x var (movable atom)](/ref/atom/movable/var/step_x.md) 
> +   [step_y var (movable atom)](/ref/atom/movable/var/step_y.md) <!-- -->