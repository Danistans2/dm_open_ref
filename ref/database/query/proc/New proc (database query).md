[]{#/database/query/proc/New}    
## New proc (database query) {#new-proc-database-query byondver="506"}    
**See also:**    
:   [database datum](/ref/database.md)    
:   [database query datum](/ref/database/query.md)    
:   [Add proc (database query)](/ref/database/query/proc/Add.md)    
<!-- -->    
**Format:**    
:   New(text, item1, item2, \...)    
<!-- -->    
**Args:**    
:   text: Text to add to the query    
:   item1, item2, etc.: Items that will replace question marks in text    
Creates a new query and adds text by automatically calling Add(). See    
the [Add proc](/ref/database/query/proc/Add.md) for more information.    
Call Execute() to run the query.  