## id parameter (skin)

<!-- -->
**Applies to:**
+   [All](/ref/%7Bskin%7D/control.md) 
<!-- -->
**Format:**
+   string


The name of this control. Read-only. 

If this is a
[Main control](/ref/%7Bskin%7D/control/main.md) , the name should always be
unique. For others, it is usually still a good idea to use a unique
name, but they can be referenced by *window*.*id* at runtime.
You can use a colon in front of the
[type](/ref/%7Bskin%7D/param/type.md) to refer to the default control
of a certain type, if one exists, e.g. `:map` is the default map.

> [!TIP] 
> **See also:**
> +   [parent parameter](/ref/%7Bskin%7D/param/parent.md) 
> +   [type parameter](/ref/%7Bskin%7D/param/type.md) 