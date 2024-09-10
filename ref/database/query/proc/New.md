[]{#/New proc (database query).md}    
## New proc (database query) {#new-proc-database-query byondver="506"}    
**See also:**    
:   [database datum]/database    
:   [database query datum]/database/query    
:   [Add proc (database query)]/database/query/proc/Add    
<!-- -->    
**Format:**    
:   New(text, item1, item2, \...)    
<!-- -->    
**Args:**    
:   text: Text to add to the query    
:   item1, item2, etc.: Items that will replace question marks in text    
Creates a new query and adds text by automatically calling Add(). See    
the [Add proc]/database/query/proc/Add for more information.    
Call Execute() to run the query.  