## usr var (proc)



This is a mob variable (var/mob/usr) containing the mob of the
player who executed the current verb, or whose action ultimately called
the current proc.
### Example:

``` dm
 obj/bread verb/eat() world \<\< \"\[usr\] eats \[src\]\"

```
 

If a player named \"Bob\" calls \"eat bread\", the
output will be \"Bob eats the bread.\" 

Essentially, `usr` is an
implicit parameter that is passed to every proc or verb. Each procedure
inherits the value from its caller. While it can simplify your code in
some situations, it can also lead to subtle problems if you are assuming
that `usr` is automatically assigned the value of `src` when you call a
verb programmatically. It is not. 

The only time `usr` is
assigned for you is when a player executes a verb, clicks something with
the mouse, clicks a link (see [Topic](/ref/client/proc/Topic.md) ), or
any other such action.
Note: **A good rule of thumb is to never put usr in a proc, only
verbs.** Typically `usr` in a proc is an unsafe programming practice. If
`src` would not be the correct choice, it is better to send another
argument to your proc with the information it needs. 

Certain
built-in procs such as [atom/Click()](/ref/atom/proc/Click.md)  are
called automatically by a client counterpart like
[client/Click()](/ref/client/proc/Click.md) ; usually
[atom/Stat()](/ref/atom/proc/Click.md)  is called by
[client/Stat()](/ref/client/proc/Click.md) ; and so on. It is mostly
safe to apply `usr` as directed in those situations, because these procs
are pseudo-verbs. It is mostly *not* safe to apply `usr` in a movement
proc such as [Move()](/ref/atom/movable/proc/Move.md)  or
[Enter()](/ref/atom/proc/Enter.md) , because objs and non-player mobs
may move autonomously without setting `usr`. 

Although `usr` is
often set in [mob/Login()](/ref/mob/proc/Login.md)  when a client first
connects, you should not assume it is valid if `Login()` is called any
other way. Common cases occur when creating a new character, loading a
player\'s mob from a savefile; or explicitly when setting a mob\'s key
or changing the value of [client.mob](/ref/client/var/mob.md) . It is
safest to use `src` in `mob/Login()`, which is always correct, rather
than `usr`. 

`usr` is the default point of reference for several
procs like [view()](/ref/proc/view.md)  and
[range()](/ref/proc/range.md) , because of their common use in verbs. It
is also the default recipient for [input()](/ref/proc/input.md)  and
[alert()](/ref/proc/alert.md) messages. When using these in procs, be
aware of that so you can change the default reference value to something
more appropriate.

> [!TIP] 
> **See also:**
> +   [src var (proc)](/ref/proc/var/src.md) 
> +   [verbs](/ref/verb.md) 
> +   [Topic proc (client)](/ref/client/proc/Topic.md) 
> +   [range proc](/ref/proc/range.md) 
> +   [view proc](/ref/proc/view.md) 
> +   [alert proc](/ref/proc/alert.md) 
> +   [input proc](/ref/proc/input.md) 