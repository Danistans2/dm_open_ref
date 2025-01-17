## Columns proc (database query) 
###### BYOND Version 506

**Format:**
+   Columns()\
    *or*\
    Columns(column)
<!-- -->
**Args:**
+   column: The Nth column whose name should be read


Returns a list of column names for the current query, or the
name of the Nth column. 

You must call Execute() before calling
Columns().

> [!TIP] 
> **See also:**
> +   [database query datum](/ref/database/query.md) 
> +   [Execute proc (database query)](/ref/database/query/proc/Execute.md) 
> +   [GetColumn proc (database query)](/ref/database/query/proc/GetColumn.md) 
> +   [GetRowData proc (database query)](/ref/database/query/proc/GetRowData.md) 
> +   [NextRow proc (database query)](/ref/database/query/proc/NextRow.md) <!-- -->