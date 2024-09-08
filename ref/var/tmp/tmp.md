[]{#/var/tmp}
## tmp vars
**See also:**
:   [savefile](#/savefile)
:   [vars](#/var)
The tmp type modifier indicates that an object variable should not be
automatically written to the save file. This could mean that the
variable is transient---that is, it is calculated at run-time and need
not be saved. It could also indicated that the designer will handle
saving of that variable specially and wishes to bypass the automated
routine.
It is especially important to use tmp when you have references to
external objects that should not be saved along with the object. For
example, suppose players have a `leader`{.variable} variable which
indicates who or what they are following. You would not necessarily want
the leader to be saved in the player\'s savefile. Therefore, you would
need to use `tmp` when defining the variable.
### Example:
mob var/tmp leader verb follow(mob/M) leader = M
::: {.sidebar .note}
Accidentally saving another mob in your savefile can be disastrous. This
can happen if you save a turf that the mob is standing on, or if you
save an obj with a non-tmp var that points to that mob, and many other
ways.
The reason this is a problem is that another player\'s mob will have the
`key` var set already. When that mob is loaded, if they are already
logged into the game they will be immediately reassigned to that
just-loaded, older mob with a `Login()` call, while the mob they\'re
supposed to be using will have `Logout()` called. Thus they\'ll appear
to \"rollback\" to an earlier state.
If your game accidentally falls into this trap, don\'t panic! You can
look at your savefiles via [ImportText()](#/savefile/ImportText){.code}
or in an editor to see which var is the problem. Once you change that
var to `/tmp`, you can override [Read()](#/datum/proc/Read){.code} so if
that var is present, you can remove it before calling `..()` to finish
loading.
:::
The following built-in variables are defined as tmp vars:
:   [type](#/datum/var/type)
:   [parent_type](#/datum/var/parent_type)
:   [vars](#/datum/var/vars)
:   [verbs](#/atom/var/verbs)
:   [group](#/mob/var/group)
:   [loc](#/atom/var/loc)
:   [locs](#/atom/var/locs)
:   [vis_locs](#/atom/var/vis_locs)
:   [x](#/atom/var/x)
:   [y](#/atom/var/y)
:   [z](#/atom/var/z)
:   [ckey](#/mob/var/ckey)
:   [visibility](#/atom/var/visibility)
:   [bound_x](#/atom/movable/var/bound_x)
:   [bound_y](#/atom/movable/var/bound_y)
:   [bound_width](#/atom/movable/var/bound_width)
:   [bound_height](#/atom/movable/var/bound_height)
:   [mouse_over_pointer](#/atom/var/mouse_over_pointer)
:   [mouse_drag_pointer](#/atom/var/mouse_drag_pointer)
:   [mouse_drop_pointer](#/atom/var/mouse_drop_pointer)