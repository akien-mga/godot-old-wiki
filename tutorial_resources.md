**Important:** This wiki is soon going to be taken down, as the official documentation of the Godot project is now on http://docs.godotengine.org.

# Resources

### Nodes AND Resources

So far, [Node](class_node) have been the most important datatype in Godot, as most of the behaviors and features of the engine are implemented through them. There is, though, another datatype that is equally as important. That is [Resource](class_resource)..

Where *Nodes* focus on behaviors, such as drawing a sprite, drawing a 3D model, physics, GUI controls, etc, 
*Resources* are mere *data containers*. This means that they don't do any action nor process any information. Resources just contain data.

Examples of resources are [Texture](class_texture), [Script](class_script), [Mesh](class_mesh), [Animation](class_animation), [Sample](class_sample), [AudioStream](class_audiostream), [Font](class_font), [Translation](class_translation), etc.

When Godot saves or loads (from disk) a scene (.scn or .xml), an image (png, jpg), a scrit (.gd) or pretty much anything, that file is considered a resource.

When a resource is loaded from disk, **it is always loaded once**. That means, if there is a copy of that resource already loaded in memory, trying to load the resource again will just return the same copy again and again. This corresponds with the fact that resources are just data containers, so there is no need to have them duplicated.

Typically, every object in Godot (Node, Resource, or anything else) can export properties, properties can be of many types (like a string, integer, Vector2, etc) and one of those types can be a resource. This means that both nodes and resources can contain resources as properties. To make it a litle more visual:

<p align="center"><img src="images/nodes_resources.png"></p>

### External vs Built-In

The resource properties can reference resources in two ways, *external* (on disk) or *built-in*. 
To be more specific, here's a [Texture](class_texture) in a [Sprite](class_sprite) node:

<p align="center"><img src="images/spriteprop.png"></p>

Pressing the the ">" button the right side of the preview, allows to view and edit the resources properties. One of the properties (path) shows where did it come from. In this case, it came from a png image.

<p align="center"><img src="images/resourcerobi.png"></p>

When the resource comes from a file, it is considered an *external* resource. If the path property is erased (or never had a path o begin with), it is then considered a built-in resource. 

For example, if the path `"res://robi.png"` is erased from the "path" property in the above example, and then the scene is saved, the resource will be saved inside the .scn scene file, no longer referencing the external "robi.png". However, even if saved as built-in, and even though the scene can be instanced multiple times, the resource will still always be loaded once. That means, different Robi robot scenes instanced at the same time will still share the same image.

### Loading Resources from Code


Loading resources from code is easy, there are two ways to do it. The first is to use load(), like this:

```python

func _ready():

        var res = load("res://robi.png") # resource is loaded when line is executed
        get_node("sprite").set_texture(res)
```

The second way is more optimal, but only works with a string constant parameter, because it loads the resource at compile-time.

```python

func _ready():

        var res = preload("res://robi.png") # resource is loaded at compile time
        get_node("sprite").set_texture(res)
```

### Loading Scenes

Scenes are also resources, but there is a catch. Scenes saved to disk are resources of type [PackedScene](class_packedscene), this means that the scene is packed inside a resource.

To obtain an instance of the scene, the method  [instance](class_packedscene#instance)() must be used. 
```python
func _on_shoot():

        var bullet = preload("res://bullet.scn").instance()
        add_child(bullet)                  
```

This method creates the nodes in hierarchy, configures them (sets all the properties) and returns the root node of the scene, which can be added to any other node.
The approach has several advantages. As the [instance](class_packedscene#instance)() function is pretty fast, adding extra content to the scene can be done efficiently. New enemies, bullets, effects, etc can be added or removed quickly, without having to load them again from disk each time. It is important to remember that, as always, images, meshes, etc are all shared between the scene instances.

### Freeing Resources

Resource extends from [Reference](class_reference). As such, when a resource is no longer in use, it will automatically free itelf. Since, in most cases, Resources are contained in Nodes, scripts or other resources, when a node is removed or freed, all the children resources are freed too.

### Scripting

Like any object in Godot, not just nodes, Resources can be scripted too. However, there isn't generally much of a win, as resources are just data containers.






(c) Juan Linietsky, Ariel Manzur, Distributed under the terms of the [CC By](https://creativecommons.org/licenses/by/3.0/legalcode) license.
