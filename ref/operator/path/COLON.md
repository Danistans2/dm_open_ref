## : path operator


The colon operator may be used as a short-cut when specifying a
path in the DM code tree. Instead of specifying the full path, you can
insert a colon and the compiler will search down in the tree with the
node you specify. This is known as a \"downward\" search. You should
only use it when the target node is unique. 

The following
example demonstrates the principle but it obviously doesn\'t save much
typing!
### Example:

``` dm
 world mob = :player //short-cut to /mob/player mob/player
Login() src \<\< \"Welcome, \[name\].\" 
```


> [!TIP] 
> **See also:**
> +   [. path operator](/ref/operator/path/%2e.md) 
> +   [/ path operator](/ref/operator/path//.md) 