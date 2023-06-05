# coordinated_return

WIP for Minecraft ComputerCraft mod - Lua code for turtles and a server to communicate via rednet messages so that turtles away from their docking stations to be called back to NEAREST docking point (thus coordinated by server)

- Turtle(s) require GPS to be set up for finding location. Tutorial here: https://computercraft.info/wiki/Gps_(API)

When programming turtle movements, implement orientSelf for initial forward movement and oturn for subsequent turns so that the turtle will be able to keep track of which way it is facing in terms of +-x, +-y so that finding a docking station is much more easily coordinated via the server and does not require that, in the event of some kind of emergency, each turtle does not need to orient themselves only upon receiving message to return to dock.

Note for next update:
update messages from turtle to new style with {message, coordinates}
update turtle to be more like a server and resend messages as needed
change turtle movement to attempt different axis when failing to return and include z in closeLargestGap()
