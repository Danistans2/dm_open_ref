## on-change parameter (skin)

<!-- -->
**Applies to:**
+   [Bar](/ref/%7Bskin%7D/control/bar.md) 
<!-- -->
**Format:**
+   string


[Command](/ref/%7Bskin%7D/commands.md)  executed when the
[value](/ref/%7Bskin%7D/param/value.md)  of the bar/slider is changed.
If you drag the slider around, the command will not run until you let
go. 

If you include `[[*]]` in the command, it will be replaced
by the control\'s new `value`. (See \"Embedded Winget\" in [client
commands](/ref/%7Bskin%7D/commands.md) for more details on the `[[...]]`
format.)

> [!TIP] 
> **See also:**
> +   [value parameter](/ref/%7Bskin%7D/param/value.md) 