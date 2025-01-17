## Interpolate proc (vector) 
###### BYOND Version 516

**Format:**
+   A.Interpolate(B, t)
<!-- -->
**Args:**
+   B: The other vector to interpolate with.
+   t: The interpolation factor: from 0 (A) to 1 (B). Usually this is a
    value between 0 and 1.
<!-- -->
**Returns:**
+   A new vector interpolated between A and B.


Returns the equivalent of `A + (B-A) * t`. 

There is
special handling for a case of `t=1` to avoid rounding errors.

> [!TIP] 
> **See also:**
> +   [vector](/ref/vector.md) 
> +   [vector proc](/ref/proc/vector.md) <!-- -->