[]{#/proc/tan}    
## tan proc {#tan-proc byondver="513"}    
**See also:**    
:   [arctan proc](/ref/proc/arctan.md)    
:   [cos proc](/ref/proc/cos.md)    
:   [sin proc](/ref/proc/sin.md)    
:   [turn proc](/ref/proc/turn.md)    
<!-- -->    
**Format:**    
:   tan(X)    
<!-- -->    
**Returns:**    
:   The tangent of X, where X is in degrees.    
### Example:    
mob/verb/test() usr \<\< tan(0) // 0 usr \<\< tan(45) // 1 usr \<\<    
tan(90) // infinity (or close enough)  