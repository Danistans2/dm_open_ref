## Translate proc (matrix)

**Format:**
+   Translate(x,y)
<!-- -->
**Args:**
+   x: The amount of scaling to do in the x direction
+   y: The amount of scaling to do in the y direction
<!-- -->
**Returns:**
+   src


The matrix is translated (moved) by the appropriate amounts.
The x and y offsets applied by translation are in pixels. 

If y
is omitted, x is used for both. E.g., Translate(2) is equivalent to
Translate(2,2).

> [!TIP] 
> **See also:**
> +   [matrix](/ref/matrix.md) 
> +   [matrix operators](/ref/matrix/operators.md) 
> +   [matrix procs](/ref/matrix/proc.md) <!-- -->