## icon arithmetic

Note: The following \"arithmetical\" methods of icon manipulation are
being phased out in favor of the [/icon](/ref/icon.md)  object, which
can be directly manipulated and which provides a wider variety of
operations. Many of those in turn have been obviated by the
[color](/ref/atom/var/color.md)  and
[transform](/ref/atom/var/transform.md)  vars. 

There are
several ways in which icons can be manipulated at runtime. They can be
rotated, added together, and the colors components may be altered.


One purpose for such operations is to make players look
different. Other interesting uses (and abuses) will undoubtedly follow.
### Addition and Subtraction


The result of adding two icons is an arithmetic combination of
the color components of each individual pixel. At positions where either
icon is transparent, the result is also transparent. Subtraction,
instead of increasing the intensity, decreases it by the amount in each
pixel of the icon being subtracted. 

Suppose you wanted to add
together different bodies and heads. You could do that by making a few
of each type with black backgrounds. When these add together, the black
contributes nothing but prevents pixels in the other icon from getting
clipped.
### Example:

``` dm
 mob/verb addicon(I as icon) icon += I subicon(I as icon)
icon -= I 
```
 

If you need to add the same color to every
pixel, you can do so using a color value. Color values have the same
format as in HTML: \"#RRGGBB\" with two hexadecimal digits for each
color component. That gives you a range in color from 0 to FF (which is
255 in decimal). 

You can also specify a color value as
\"#RGB\". The single digit is automatically repeated, so \"#F00\" is the
same as \"#FF0000\", which is bright red. For certain pre-defined color
values, you can also specify a name, such as \"red\". See [HTML
colors](/ref/%7B%7Bappendix%7D%7D/html-colors.md) for a list of color names.


If you prefer base 10, you can create color values with the
rgb(R,G,B) instruction. Each parameter is in the range 0 to 255.
### Multiplication


To increase (or decrease) the intensity of an icon
multiplicatively, you can use the \'`*`\' operator.
### Example:

``` dm
 mob/verb/multicon(factor as num) icon \*= factor

```


> [!TIP] 
> **See also:**
> +   [icon proc](/ref/proc/icon.md) 
> +   [icon_states proc](/ref/proc/icon_states.md) 
> +   [icons](/ref/DM/icon.md) 
> +   [rgb proc](/ref/proc/rgb.md) 
> +   [turn proc (applied to an icon)](/ref/proc/turn/icon.md) 
> +   [icon object](/ref/icon.md) 