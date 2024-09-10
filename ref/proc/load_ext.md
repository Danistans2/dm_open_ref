[]{#/load_ext proc.md}    
## load_ext proc {#load_ext-proc byondver="516"}    
**See also:**    
:   [call_ext proc]/proc/call_ext    
:   [Byondapi]/%7B%7Bappendix%7D%7D/Byondapi    
<!-- -->    
**Format:**    
:   load_ext(LibName,FuncName)    
<!-- -->    
**Args:**    
:   LibName: name of external library (\"test.DLL\") (note: the .dll or    
    .so suffix is not required)    
:   FuncName: name of function in external library (\"func\"), which may    
    have prefixes to describe the type of function    
<!-- -->    
**Returns:**    
:   A reference to a function in an external library, for use with    
    `call_ext()`.    
Use `load_ext()` to pre-load external library functions you intend to    
use often, when maximum performance is required. (See    
[call_ext()]/proc/call_ext{.code} for the rules for loading    
libraries.)    
The result of this proc can be passed to `call_ext()` as a single    
argument in lieu of the normal LibName and FuncName.    
If the lookup fails for any reason, a runtime error will be thrown.    
### Example:    
var/logfunc proc/LogLine(msg) logfunc \|\|= load_ext(\"my_lib\",    
\"byond:OutputToLog\") call_ext(logfunc)(msg)  