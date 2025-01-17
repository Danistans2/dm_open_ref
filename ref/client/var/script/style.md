## style sheets (in scripts)



Style sheets may be included in DM Script by putting the style
sheet inside the HTML tags `<STYLE>` and `</STYLE>`. In general, any
text enclosed in start and end tags will be sent to the player\'s
terminal, so you could use `client.script` to output a welcome message
as well as loading a style sheet. 


### Example:

``` dm
 client/script = \"
\" 
```
 

This example style sheet makes the player\'s
terminal have a black background and aqua colored text. When changing
the background color, it is important to change the color of system and
link text as well. See the section on [style sheets](/ref/DM/text/style.md) for an example.

> [!TIP] 
> **See also:**
> +   [script var (client)](/ref/client/var/script.md) 
> +   [style sheets](/ref/DM/text/style.md) 