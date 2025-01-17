## walk_rand proc

**Format:**
+   walk_rand(Ref,Lag=0,Speed=0)
<!-- -->
**Args:**
+   Ref: A mob or obj.
+   Lag: Delay in world ticks between movement.
+   Speed: Speed to move, in pixels. 0 uses Ref.step_size.


Moves Ref randomly. Each step will be preceded by Lag time of
inactivity. 

A call to a walking function aborts any previous
walking function called on Ref. To halt walking, call walk(Ref,0).


This function returns immediately, but continues to process in
the background.

> [!TIP] 
> **See also:**
> +   [get_step_rand proc](/ref/proc/get_step_rand.md) 
> +   [step_rand proc](/ref/proc/step_rand.md) 
> +   [step_size var (movable atom)](/ref/atom/movable/var/step_size.md) <!-- -->