# Physics Ray Casting and Queries (2D and 3D)

### Introduction

One of the most common tasks in game development is casting a ray (or custom shaped object) and see what it hits. This enables complex behaviors, AI, etc. to take place.
This tutorial will explain how to do this 2D, but it's pretty much the same for 3D.

Godot stores all the low level game information in servers, while the scene is just a frontend. As such, ray casting is generally a lower-level task. For simple raycasts, node such as [RayCast](class_raycast) and [RayCast2D](class_raycast2d) will work, as they will return every frame what the result of a raycast is.

Many times, though, ray-casting needs to be a more interactive process so a way to do this by code must exist.

### Space

In the physics world, Godot stores all the low level collision and physics information in a _space_. The current 2d space (for 2D Physics) can be obtained by calling [CanvasItem.get_world_2d().get_space()](class_canvasitem#get_world_2d). For 3D, it's [Spatial.get_world().get_space()](class_spatial#get_world).

The resulting space [RID](class_rid) can be used in [PhysicsServer](class_physicsserver) and [Physics2DServer](class_physics2dserver) respectively for 3D and 2D.

### Acessing Space

Godot physics runs by default in the same thread as game logic, but may be set to run on a separate thread to work more efficiently. Due to this, the only time accessing space is safe is during the [Node._fixed_process(delta)](class_node#_fixed_process) callback. Accessing it from outside this function may result in an error due to space being _locked_.

To perform queries into physics space, the [Physics2DDirectSpaceState](class_physics2ddirectspacestate) and [PhysicsDirectSpaceState](class_physicsdirectspacestate) must be used. 

In code, for 2D spacestate, this code must be used:

```python
func _fixed_process(delta):
    var space_rid = get_world_2d().get_space()
    var space_state = Physics2DServer.space_get_direct_state(space_rid)
```

Of course, there is a simpler shortcut:

```python
func _fixed_process(delta):
    var space_state = get_world_2d().get_direct_space_state()
```

For 3D:

```python
func _fixed_process(delta):
    var space_state = get_world().get_direct_space_state()
```

### Raycast Query
