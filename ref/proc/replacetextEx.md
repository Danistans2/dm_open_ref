## replacetextEx proc 
###### BYOND Version 510

<!-- -->
**Format:**
+   replacetextEx(Haystack,Needle,Replacement,Start=1,End=0)
<!-- -->
**Returns:**
+   The Haystack text with all cases of Needle replaced by Replacement
<!-- -->
**Args:**
+   Haystack: The text string to search.
+   Needle: The sub-text to search for. May be a regular expression
    (regex).
+   Replacement: The replacement text, or a proc.
+   Start: The text byte position in Haystack in which to begin the
    search.
+   End: The text byte position in Haystack immediately following the
    last character to search.


When Needle is text, this instruction is sensitive to the case
of Haystack and Needle. The case-insensitive version is replacetext().
### Example:

``` dm
 world \<\< replacetext(\"One on one\", \"one\", \"two\")

```
 

This outputs \"Two on two\", where the first case\'s
\"One\" is identified as uppercase. 

You may use a proc as the
Replacement value. In that case, the proc will be called with the found
text as an argument, and its return value will be the replacement. There
will be no automatic correction to uppercase or all caps in this case.


When the Needle value is a regular expression, this proc
behaves identically to the [regex Replace()](/ref/regex/proc/Replace.md)  proc.
Case-sensitivity, and whether one match or all are replaced, depend on
the regular expression. 

Note: In strings containing non-ASCII
characters, byte position and character position are not the same thing.
Use `replacetextEx_char()` to work with character counts instead of
bytes, at a performance cost. See the [Unicode](/ref/%7Bnotes%7D/Unicode.md) section for more information.

> [!TIP] 
> **See also:**
> +   [findtextEx proc](/ref/proc/findtextEx.md) 
> +   [replacetext proc](/ref/proc/replacetext.md) 
> +   [Regular expressions](/ref/%7Bnotes%7D/regex.md) 
> +   [Replace proc (regex)](/ref/regex/proc/Replace.md) 