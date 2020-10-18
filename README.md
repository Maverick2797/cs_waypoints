minetest CSM which implements waypoints on top of the /teleport server side command.

requirements
------------

tested with minetest 0.4.17 and 5.0.

in 5.0, the server *must* have send_chat_message enabled, which is not the default.

additionally, this mod will *only* work if your account has the "teleport" privilege.
it will *not* let ordinary users teleport, unless that is a default privilege.

installation
------------

make sure the mod is installed at `~/.minetest/clientmods/cs_waypoints`

make sure `~/.minetest/clientmods/mods.conf` exists and contains:

```
load_mod_cs_waypoints = true
```

usage
-----

* .wp_list: list all waypoints
* .wp_set NAME: set a waypoint at your current location
* .wp_show NAME: shows the coords of NAME
* .wp_unset NAME: remove a waypoint

* .tp_pop: return to the last saved location
* .tp_push NAME: teleport to a waypoint and save current location
* .tp_shift AXIS DISTANCE: moves you on the given axis the given distance
* .tp_to NAME: teleport to a waypoint
* .tp_use NAME: like tp_pop, but doesn't remove the saved location from the stack


* .wp_dist NAME: shows the distance to NAME
* .wp_exch NAME1 NAME2: swaps the saved positions of the named waypoints
* .wp_grep NAME:  search for NAME in the waypoint names
* .wp_search DELTA: searches for saved waypoints near te current location with the given delta for all coordinates
* .wp_search: searches for saved waypoints near te current location with DELTA=10
* .wp_stack: shows the locations in the stack
* .wp_stack_clear: clears the stack
