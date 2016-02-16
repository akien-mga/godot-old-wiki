**Important:** This wiki is soon going to be taken down, as the official documentation of the Godot project is now on http://docs.godotengine.org.

# Pausing a Game

### Pause?

In most games, it is always desirable to, at some point, interrupt the game to do something else. Be it taking a break, to changing options. However this is not as simple as it seems. The game might be stopped, but it might be desirable that some menus and animations continue working. 

Implementing a fine-grained control for what can be paused (and what not) is a lot of work, so a simple framework for pausing is provided in Godot.

### How Pausing Works

To set pause mode, the pause state must be set. This is done by calling [SceneTree.set_pause](class_scenetree#set_pause) with a "true" argument:

```python
get_tree().set_pause(true)
```

Doing so will have the following behavior:

* 2D and 3D Physics will be stopped.
* _process and _fixed_process will not be called anymore in nodes.
* _input and _input_event will not be called anymore either.

This effectively stops the whole game. Calling this function from a script, by default, will result in an unrecoverable state (nothing will work anymore!).

### White-Listing Nodes

Before enabling pause, make sure that nodes that must keep working during pause are white-listed. This is done by editing the "Pause Mode" property in a node:

<p align="center"><img src="images/pausemode.png"></p>

By default all nodes have this property in the "Inherit" state. This means, that they will only process (or not) depending on what this same property is set on the parent node. If the parent is set to "Inherit" , then the grandparent will be checked and so on. Ultimately, if a state can't be found in any of the grandparents, the pause state in SceneTree is used. This means that, by default, when the game is paused every node will be paused.

So the three possible states for a node are:

* **Inherit**: Process depending on the state of the parent, grandparent, etc. The first parent that has a non-Inherit state.
* **Stop**: Stop the node no matter what (and children in Inherit mode). Paused or not this node will not process.
* **Process**: Process the node no matter what (and children in Inherit mode). Paused or not this node will process.

### Example

An example of this is creating a popup or panel with controls inside, and set it's pause mode to "Process" then just hide it:

<p align="center"><img src="images/pause_popup.png"></p>

Just by setting the root of the pause popup to "Process", all children and grandchildren will inherit that state. This way, this branch of the scene tree will continue working when paused.

Finally, make it so when a pause button is pressed (any button will do), enable the pause and show the pause screen.

```python
func _on_pause_button_pressed():
    get_tree().set_pause(true)
    get_node("pause_popup").show()
```

To remove the pause, just do the opposite when the pause screen is closed:

```python
func _on_pause_popup_close_pressed():
    get_node("pause_popup").hide()
    get_tree().set_pause(false)
```

And that should be all!


(c) Juan Linietsky, Ariel Manzur, Distributed under the terms of the [CC By](https://creativecommons.org/licenses/by/3.0/legalcode) license.
