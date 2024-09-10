[]{#/REGEX_QUOTE proc.md}    
## REGEX_QUOTE proc {#regex_quote-proc byondver="510"}    
**See also:**    
:   [regex proc]/proc/regex    
:   [regex datum]/regex    
:   [stddef.dm file]/%7B%7Bappendix%7D%7D/stddef%2edm    
<!-- -->    
**Format:**    
:   REGEX_QUOTE(text)    
:   REGEX_QUOTE_REPLACEMENT(text)    
<!-- -->    
**Returns:**    
:   REGEX_QUOTE: A version of the text with any special regular    
    expression characters escaped by backslashes.    
:   REGEX_QUOTE_REPLACEMENT: A version of the text with \$ characters    
    escaped by a second \$.    
<!-- -->    
**Args:**    
:   text: The text to escape    
Quotes a piece of text so that it can be used inside a regular    
expression without fear of being treated as pattern instructions.    
### Example:    
proc/FindWord(text, word) // The \\b pattern is a word break, to search    
for the word // on its own instead of as part of another word.    
var/regex/R = regex(\"\\\\b\[REGEX_QUOTE(word)\]\\b\", \"i\") // find    
the pattern in the text return R.Find(text)  