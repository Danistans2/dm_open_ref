[]{#/proc/ismovable}    
## ismovable proc {#ismovable-proc byondver="513"}    
**See also:**    
:   [isloc proc](/ref/proc/isloc.md)    
:   [isobj proc](/ref/proc/isobj.md)    
:   [ismob proc](/ref/proc/ismob.md)    
<!-- -->    
**Format:**    
:   ismovable(Loc1, Loc2 \...)    
<!-- -->    
**Args:**    
:   Any number of locations to test.    
<!-- -->    
**Returns:**    
:   1 if all args are valid objs or mobs; 0 otherwise    
Movable atoms are either objs or mobs, so this combines the `isobj` and    
`ismob` tests into a single proc.  