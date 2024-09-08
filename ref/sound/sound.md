[]{#/sound}
## sound datum
**See also:**
:   [vars (sound)](#/sound/var)
:   [sound proc](#/proc/sound)
:   [stddef.dm file](#/%7B%7Bappendix%7D%7D/stddef%2edm)
:   [load_resource proc](#/proc/load_resource)
A `/sound` datum is created by the `sound()` proc or by `new/sound()`.
It can be used to change the way a sound file will play. When you\'re
ready to play the sound, just send it to a player like so: var/sound/S =
sound(\'bubbles.wav\') usr \<\< S
The sound file can be supplied as a list of choices, in which case the
client will play the first compatible sound in the list.