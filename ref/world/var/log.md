[]{#/log var (world).md}    
## log var (world)    
**See also:**    
:   [file proc]/proc/file    
:   [startup proc]/proc/startup    
Sending output to world.log may be useful for debugging purposes. The    
output goes to the same place run-time proc errors are displayed.    
### Example:    
if(1+1 != 2) world.log \<\< \"Uh oh.\"    
You can assign world.log to a file name or file() object to redirect    
output to that file. (There is also a command-line option to Dream    
Daemon that does this.)    
### Example:    
world.log = file(\"mylog.txt\")  