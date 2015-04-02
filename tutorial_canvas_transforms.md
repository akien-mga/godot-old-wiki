# Viewport & Canvas Transforms

### Introduction

This tutorial is created after a topic that is a little dark for most users, and explains all the 2D transforms going on for nodes from the moment they draw their content locally to the time they are drawn into the screen.

### Canvas Transform

As mentioned in the [previous tutorial](tutorial_canvas_layers), every CanvasItem node (remember that Node2D and Control based nodes use CanvasItem as their common root) will reside in a _Canvas Layer_. Every canvas layer has a transform (translation, rotation, scale, etc) that can be accessed as a [Matrix32](class_matrix32).

By default, nodes are drawn in Layer 0, in the built-in canvas. To put nodes in a different layer, a  [CanvasLayer](class_canvaslayer) node can be used. This was covered in the previous tutorial anyway, just refreshing.

### Global Canvas Transform

Viewports also have a Global Canvas transform (also a [Matrix32](class_matrix32) ). This is the master transform and affects all individual _Canvas Layer_ transforms. Generally this transform is not of much use, but is used in the CanvasItem Editor in Godot's editor.

### Stretch Transform

Finally, viewports have a _Stretch Transform_, which is used when resizing or stretching the screen. This transform is used internally by the [stretch modes](tutorial_multires), but can also be requested to the viewport. 

Input events received in the [Node._input_event(ev)](class_node#_input_event) callback are multiplied by this transform, but lack the ones above. To convert InputEvent coordinates to local CanvasItem coordinates, the [CanvasItem.make_input_local(ev)](class_canvasitem#make_input_local) function was added for convenience.

### Transform Order

For a coordinate in CanvasItem local properties to become an actual screen coordinate, the following chain of transforms must be applied:

<p align="center"><img src="images/viewport_transforms.png"></p>

### Transform Functions

Obtaining each transform can be achieved with the following functions:

Type: | Transform  
------|-----------
CanvasItem | [CanvasItem.get_global_transform()](class_canvasitem#get_global_transform) 
CanvasLayer| [CanvasItem.get_canvas_transform()](class_canvasitem#get_canvas_transform) 
CanvasLayer+GlobalCanvas+Stretch | [CanvasItem.get_viewport_transform()](class_canvasitem#get_viewport_transform) 

Finally then, to convert a CanvasItem local coordinates to screen coordinates, just multiply in the following order:

```python
var screen_coord = get_viewport_transform() * ( get_global_transform() * local_pos )
```

Keep in mind, however, that it is generally not desired to work with screen coordinates. The recommended approach is to simply work in Canvas coordinates (CanvasItem.get_global_transform()), to allow automatic screen resolution resizing to work properly.