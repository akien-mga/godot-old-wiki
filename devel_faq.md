## #1 GDScript? Why your own scripting language? Why not Lua, Javascript, C#, etc.

The short answer is, we'd rather a programmer does the small effort to learn GDScript so he or she later has a seamless experience, than attracting him or her with a familiar programming language that results in a worse experience. We are OK if you would rather not give Godot a chance because of this, but we strongly encourage you to try it and see the benefits yourself.

The official languges for Godot are GDScript and C++.

GDScript is designed to integrate from the ground to the way Godot works, more than any other language, and is very simple and easy to learn. Takes at much a day or two to get comfortable and it's very easy to see the benefits once you do.  Please do the effort to learn GDScript, you will not regret it.

Godot C++ API is also efficient and easy to use (the entire Godot editor is made with this API), and an excellent tool to optimize parts of a project, but trying to use it instead of GDScript for an entire game is, in most cases, a waste of time.

Yes, for more than a decade we tried in the past integrating several VMs (and even shipped games using them), such as Python, Squirrel and Lua (in fact we authored tolua++ in the past, one of the most popular C++ binders). None of them worked as well as GDScript does now.

More information about getting comfortable with GDScript or dynamically typed languages can be found [here](tutorial_gdscript_efficiently).

## #2 Why is FBX not supported for import?

FBX SDK has a very [restrictive license](http://www.blender.org/bf/Autodesk_FBX_License.rtf), that is incompatible with the [open license](http://opensource.org/licenses/MIT) provided by Godot.

That said, Godot Collada support is really good, please use the [OpenCollada](https://github.com/KhronosGroup/OpenCOLLADA/wiki/OpenCOLLADA-Tools) exporter for maximum compatibility if you are using Maya or 3DS Max. If you are use Blender, take a look at our own (Better Collada Exporter)[

## #3 Will [Insert closed SDK such as PhysX, Gameworks, etc] be supported in Godot?

No, the aim of Godot is to create a complete open source engine licensed under MIT, so you have complete control about over single piece of it. Open versions of functionality or features from such SDKs may be eventually added though.

That said, because it is open source, and modular, nothing prevents you or anyone else interested into adding those libraries as a module and ship your game using them, as either open or closed source. Everything is allowed.

## #4 How should assets be created to handle multiple resolutions and aspect ratios?

This question pops up often and it's probably thanks to the misunderstanding created by Apple when they originally doubled the resolution of their devices. It made people think that having the same assets in different resolutions was a good idea, so many continued towards that path. That originally worked to a point and only for Apple devices, but then several Android and Apple devices with different resolutions and aspect ratios were created, with a very wide range of sizes an DPIs.

The most common and proper way to this is to, instead, is to use a single base resolution for the game and only handle different screen aspects. This is mostly needed for 2D, as in 3D it's just a matter of Cameara XFov or YFov.

The proper steps to follow are:

1) Choose a single base resolution for your game. Even if there are devices that go up to 2K and devices that go down to 400p, regular hardware scaling in your device will take care of this at little or no performance cost. Most common choices are either near 1080p (1920x1080) or 720p (1280x720). Keep in mind the higher the resolution, the larger your assets, the more memory they will take and the longer the time it will take for loading.

2) Use the stretch options in Godot, 2D stretching with keeping aspect works best. Check the Mult-Resolution tutorial (tutorial_multires) on how to achieve this.

3) Determine a minimun resolution and then decide if you want your game to stretch vertically or horizontally for different aspect ratios, or whether there is a minimum one and you want black bars to appear instead. This is also explained in the previous step.

4) For user interfaces, use the [Anchoring](tutorial_gui_repositioning) to determine where controls should stay and move. If UIs are more complex, consider learning about Containers.

And that's it! your game should work in multiple resolutions. 

If there really is a desire to make your game also work on ancient devices with tiny screens (less than 300 pixels in width), you can use the [export option](export_images#image-export-options) to shrink images, and set that build to be used for certain screen sizes in the App Store or Google Play.

## #5 I have a great idea that will make Godot better, What do you think?

Your idea will most certainly be ignored. Examples of stuff that is ignored by the developers:

* Let's do this because it will make Godot better
* Let's do this in Godot because other game engine does it
* Let's remove this because I think it's not needed
* Let's remove clutter and bloat and make godot look nicer
* Let's add an alternative workflow for people that prefers it

Developers are always willing to talk to you and listen to your feedback very openly, to an extent rarely seen in open source projects, but they will care mostly about real issues you have while using Godot, not ideas solely based on personal belief. Developers are interested in (for example):

* Your experience using the software and the problems you have, (we care about this much more than ideas on how to improve it)
* The features you would like to see implemented because you need them for your project.
* The concepts that were difficult to understand in order to learn the software.
* The parts of your workflow you would like to see optimized.

Once one of the above points is stated, we can work together on a solution and this is where your ideas and suggestions are most valuable and welcome, they need to be in context of a real issue.

As such, please don't feel that your ideas for Godot are unwelcome. Instead, try to reformulate them as a problem first, so developers and the community have a base ground to discuss first.

(c) Juan Linietsky, Ariel Manzur, Distributed under the terms of the [CC By](https://creativecommons.org/licenses/by/3.0/legalcode) license.
