# mob var (client)
**Default value:**
+   Determined in client.New(), by default world.mob.


This is the mob to which the client is connected. The client
and its connected mob have the following symmetry: 
``` dm
 client
== mob.client client.mob == mob client.key == mob.key 
```
