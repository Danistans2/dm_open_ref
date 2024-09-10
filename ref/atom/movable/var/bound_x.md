[]{#/bound_x var (movable atom).md}    
## bound_x var (movable atom) {#bound_x-var-movable-atom byondver="490" deprecated="516"}    
**See also:**    
:   [icon_w var (atom)]/atom/var/icon_w    
:   [bound_y var (movable atom)]/atom/movable/var/bound_y    
:   [bound_width var (movable atom)]/atom/movable/var/bound_width    
:   [bound_height var (movable atom)]/atom/movable/var/bound_height    
:   [step_x var (movable atom)]/atom/movable/var/step_x    
:   [step_y var (movable atom)]/atom/movable/var/step_y    
:   [locs list var (movable atom)]/atom/movable/var/locs    
:   [Pixel movement]/%7Bnotes%7D/pixel-movement    
<!-- -->    
**Default value:**    
:   0    
Note: The bound_x/y vars have been deprecated in favor of icon_w/z and    
pixel_w/z. It\'s now preferred to use bound_width/height alone to define    
a bounding box. New behavior simply subtracts bound_x/y from pixel_w/z    
to mimic the old usage.    
This var defines the left side of the physical atom\'s bounding box, in    
pixels. By default all atoms are assumed to be one tile in physical    
size.    
The left edge of the bounding box starts bound_x pixels inward from the    
left edge of the atom\'s icon (as affected by step_x). A bound_x value    
of 4 means the atom has 4 pixels of empty space to its left.    
Example: A 16×16 smiley face centered in a 32×32 icon should have a    
bound_x value of 8, since there are 8 pixels of empty space to the left.  