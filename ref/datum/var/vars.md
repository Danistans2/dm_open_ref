## vars list var (datum)


This is a list of all the variables belonging to an object. The
items in the list are the variable names. If the variable name is used
as an index into the list, the value of that variable is accessed.
### Example:

``` dm
 mob/verb/dump() var/V for(V in vars) usr \<\< \"\[V\] =
\[vars\[V\]\]\" 
```
 

This example displays all the
variables belonging to your mob.

> [!TIP] 
> **See also:**
> +   [initial proc](/ref/proc/initial.md) 
> +   [issaved proc](/ref/proc/issaved.md) 
> +   [list](/ref/list.md) 
> +   [list associations](/ref/list/associations.md) 
> +   [vars list var (global)](/ref/DM/vars.md) 