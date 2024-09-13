## global var (proc)


This is not really a variable but is used to force treatment of
the following variable or proc as global. This may be necessary if a
local or src-level variable has the same name.
### Example:

``` dm
 var/myvar = \"global\" mob verb/test() var/myvar =
\"local\" usr \<\< myvar usr \<\< global.myvar 
```
 

This
example outputs \"local\" and then \"global\".

> [!TIP] 
> **See also:**
> +   [src var (proc)](/ref/proc/var/src.md) 