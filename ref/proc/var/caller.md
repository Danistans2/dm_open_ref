## caller var (proc) 
###### BYOND Version 516



Returns a [callee object](/ref/callee.md) representing the current
proc\'s caller, which can be used to access information like the proc
name, line number (if compiled with debug information), arguments, and
more. 

The main purpose of this is to make it possible to trace
the call stack when handling errors.
### Example:

``` dm
 world/Error(err) world.log \<\< \"Error \[err\]:\"
for(var/callee/p = caller, p, p = p.caller) world.log \<\< \" \[p.type\]
(src=\[p.src\], usr=\[p.usr\])\" if(p.file) world.log \<\< \" at
\[p.file\]:\[p.line\]\" 
```


> [!TIP] 
> **See also:**
> +   [callee](/ref/callee.md) 
> +   [callee var (proc)](/ref/proc/var/callee.md) 