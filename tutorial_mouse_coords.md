**Important:** This wiki is soon going to be taken down, as the official documentation of the Godot project is now on http://docs.godotengine.org.

# Mouse & Input Coordinates

## About

The reason for this small tutorial is to clear up many common mistakes about input coordinates, obtaining mouse position and screen resolution, etc.

## Hardware Display Coordinates

Using hardware coordinates makes sense in the case of writing complex UIs meant to run on PC, such as editors, MMOs, tools, etc. Yet, make not as much sense outside of that scope. 

~~The only way to reliably obtain this information is by using functions such as:~~

**This method is no longer supported:** It was too confusing and caused errors for users making 2D games. Screen would stretch to different resolutions and input would stop making sense. Please use the ``_input`` function

```python
OS.get_video_mode_size()
Input.get_mouse_pos()
```

However, this is discouraged for pretty much any situation. Please do not use these functions unless you really know what you are doing.

## Viewport Display Coordinates

Godot uses viewports to display content, and viewports can be scaled by several options (see [Multiple Screen Resolutions](tutorial_multires) tutorial). Use, then, the functions in nodes to obtain the mouse coordinates and viewport size, for example:


```python

func _input(ev):
   # Mouse in viewport coordinates

   if (ev.type==InputEvent.MOUSE_BUTTON):
       print("Mouse Click/Unclick at: ",ev.pos)
   elif (ev.type==InputEvent.MOUSE_MOTION):
       print("Mouse Motion at: ",ev.pos)

   # Print the size of the viewport

   print("Viewport Resolution is: ",get_viewport_rect().size)

func _ready():
   set_process_input(true)

```

Alternatively it's possible to ask the viewport for the mouse position

```python
get_viewport().get_mouse_pos()
```


(c) Juan Linietsky, Ariel Manzur, Distributed under the terms of the [CC By](https://creativecommons.org/licenses/by/3.0/legalcode) license.
