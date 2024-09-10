[]{#/turn proc (applied to a matrix).md}    
## turn proc (applied to a matrix)    
**See also:**    
:   [turn proc]/proc/turn    
:   [matrix]/matrix    
<!-- -->    
**Format:**    
:   turn(Matrix, Angle)    
<!-- -->    
**Returns:**    
:   A new matrix which has been rotated.    
<!-- -->    
**Args:**    
:   Matrix: a matrix to rotate    
:   Angle: An angle in degrees (clockwise rotation).    
### Example:    
mob/verb/drink() //this effect is very confusing! usr.transform =    
turn(usr.transform, 90) usr \<\< \"Woah! That stuff is powerful!\"    
sleep(200) usr.transform = null  