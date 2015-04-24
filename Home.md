<p align="center"><img src="http://www.godotengine.org/wp/wp-content/uploads/2014/01/godot_logo_63px_alto-02-021.png"/></p>
# Introduction

Welcome to the Godot Engine documentation center. The aim of these pages is to provide centralized access to all documentation-related materials.

Items in ~~strikethrough~~ mean **the feature exists**, but documentation for it has not been written yet.

# Notice!

Some types and method names changed recently, please read this:
* [SceneMainLoop -> SceneTree Notes](devel_scene_tree)

# Roadmap

* [Development Roadmap](devel_roadmap)
* [Community Roadmap](community_roadmap)
* [Frequently Asked Questions](devel_faq)


# Contributing

Contributing to godot is always very appreciated by the developers and the community. 
Be it by fixing issues or taking one of the "fun" and "not so fun" tasks. Before getting to work on anything please talk with the developers in the recently created [Developer's Mailing List].(https://groups.google.com/forum/#!forum/godot-engine).

* [Fun!](devel_fun) Fun tasks to do!
* [Not so Fun](devel_notsofun) Not so fun tasks.
* [gsoc2015 Ideas](gsoc2015) Compiled ideas for GSOC 2015.

# Tutorials

####  Basic (Step by Step)

 1.  [Scenes and Nodes](tutorial_scene)
 2.  [Instancing](tutorial_instancing)
 3.  [Instancing (Continued)](tutorial_instancing_2)
 4.  [Scripting](tutorial_scripting)
 5.  [Scripting (Continued)](tutorial_scripting_2)
 6.  [Creating a 2D Game](tutorial_2d)
 7.  [GUI Introduction](tutorial_gui)
 8.  [Creating a Splash Screen](tutorial_splash)
 9.  [Animation](tutorial_animation)
 10.  [Resources](tutorial_resources)
 11.  [File System](tutorial_fs)
 12.  [SceneTree](tutorial_scene_main_loop)
 13.  [Singletons (Autoload)](tutorial_singletons)

#### Engine

*  [Viewports](tutorial_viewports)
*  [Multiple Screen Resolutions](tutorial_multires)
*  [Input Events & Actions](tutorial_input_events)
*  [Mouse & Input Coordinates](tutorial_mouse_coords)
*  [Version Control & Project Organization](tutorial_vercontrol)
*  [GUI Control Repositioning](tutorial_gui_repositioning)
*  [Background Loading](Background loading)
*  [Encrypting Save Games](tutorial_encrypting_savegames)
*  [Internationalizing a Game (Multiple Languages)](tutorial_localization)
*  [Handling Quit Request](tutorial_quit)
*  [Pausing The Game](tutorial_pause)
*  [SSL Certificates](tutorial_ssl)
*  [Changing Scenes (Advanced)](tutorial_changing_scenes)
*  ~~[Basic Networking (TCP&UDP)](tutorial_basic_networking)~~
*  ~~[GamePad/Keyboard-Controlled GUIs](tutorial_gp_gui)~~

#### 2D Tutorials
*  [Physics & Collision (2D)](tutorial_physics_2d)
*  [Tile Map](tutorial_tilemap)
*  [Kinematic Character (2D)](tutorial_kinematic_char)
*  [GUI Skinning](tutorial_gui_skinning)
*  [Particle Systems (2D)](tutorial_particles_2d)
*  [Canvas Layers](tutorial_canvas_layers)
*  [Viewport & Canvas Transforms](tutorial_canvas_transforms)
*  [Custom Drawing in Node2D/Control](tutorial_custom_draw_2d)
*  [Custom GUI Controls](tutorial_custom_controls)
*  [Screen-Reading Shaders (texscreen() & BackBufferCopy)](tutorial_texscreen)
*  [Ray-Casting](tutorial_raycasting) Raycasting From Code (2D and 3D).
*  ~~[GUI Containers](tutorial_containers)~~
*  [Cut-Out Animation](Cutout-Animation)
*  ~~[Physics Object Guide](tutorial_physics_objects_guide)~~

#### 3D Tutorials
*  [Creating a 3D game](tutorial_3d)
*  [Materials](tutorial_materials) 
*  [Fixed Materials](tutorial_fixed_materials) 
*  [Shader Materials](tutorial_shader_materials) 
*  [Lighting](tutorial_lighting) 
*  [Shadow Mapping](tutorial_shadow_mapping)
*  [High Dynamic Range](tutorial_hdr)
*  [3D Performance & Limitations](tutorial_3d_performance)
*  [Ray-Casting](tutorial_raycasting) Raycasting From Code (2D and 3D).
*  ~~[Procedural Geometry](tutorial_procgeom)~~ 
*  ~~[Light Baking](tutorial_light_baking)~~ 
*  ~~[3D Sprites](tutorial_3d_sprites)~~ 
*  ~~[Using the AnimationTreePlayer](tutorial_animation_tree)~~
*  ~~[Portals & Rooms](tutorial_portals_rooms)~~ 
*  ~~[Vehicle](tutorial_vehicle)~~ 
*  ~~[GridMap (3D TileMap)](tutorial_grid_map)~~ 
*  ~~[Spatial Audio](tutorial_spatial_audio)~~ 
*  ~~[Toon Shading](tutorial_toon_shading)~~

#### Math

*  [Vector Math](tutorial_vector_math)
*  [Matrices & Transforms](tutorial_transforms)

#### Advanced

*  [Paths](paths)
*  [HTTP](http_client) Example of using the HTTP Client class.
*  ~~[Thread Safety](thread_safety) Using Multiple Threads.~~

#### Editor Plug-Ins

*  ~~[Editor Plugin](editor_plugin) Writing an editor extension.~~
*  ~~[Editor Plugin](editor_res_node) Writing a Resource or Node editor extension.~~
*  ~~[Editor Import-Export](editor_import) Writing an editor import-export extension.~~
*  ~~[Editor Scene Loader](editor_scene_loader) Writing a scene format loader.~~
*  ~~[Editor 3D Import](editor_import_3d) Writing a script for customizing imported 3D scenes.~~

# Reference

#### Class List

*  [Alphabetical Class List](class_list) List of classes in alphabetical order.
*  ~~[Categorized Class List](class_category) List of classes organized by category.~~
*  ~~[Inheritance Class Tree](class_inheritance) List of classes organized by inheritance.~~
*  [Relevant Classes](relevant_classes) List of the most relevant classes to learn first.

#### Languages

*  [GDScript](gdscript) Built-in, simple, flexible and efficient scripting language.
*  [GDScript (More Efficiently)](tutorial_gdscript_efficiently) Tips and help migrating from other languages. 
*  [Shader](shader) Built-in, portable, shader language.
*  [Locales](locales) List of supported locale strings.
*  [RichTextLabel BBCode](richtext_bbcode) Reference for BBCode-like markup used for RichTextLabel.

#### Cheat Sheets

*  [2D & 3D Keybindings](tutorial_keycheat) List of main 2D and 3D editor keyboard and mouse shortcuts.


# Asset Pipeline
#### General

*  [Image Files](image_files) Managing image files (read first!).

#### Import

*  [Import Process](import_process) The import process described.
*  [Importing Textures](import_textures) Importing textures.
*  [Importing 3D Meshes](import_meshes) Importing 3D meshes.
*  [Importing 3D Scenes](import_3d) Importing 3D scenes.
*  [Importing Fonts](import_fonts) Importing fonts.
*  [Importing Audio Samples](import_samples) Importing audio samples.
*  [Importing Translations](import_translation) Importing translations.

#### Export

*  [Export](export) Exporting Projects.
*  [One Click Deploy](one_click_deploy) One Click Deploy.
*  [Exporting Images](export_images) Tools for converting image files and creating atlases on export.
*  [PC](export_pc) Exporting for PC (Mac, Windows, Linux).
*  [Android](export_android) Exporting for Android.
*  ~~[BlackBerry 10](export_bb10) Exporting for BlackBerry 10.~~
*  [iOS](export_ios) Exporting for iOS.
*  ~~[NaCL](export_nacl) Exporting for Google Native Client.~~
*  ~~[HTML5](export_html5) Exporting for HTML5 (using asm.js).~~
*  ~~[Consoles](export_consoles) Exporting for consoles (PS3, PSVita, etc).~~

# Advanced

[Advanced](advanced) Advanced Topics (C++ Programming, File Formats, Porting, etc).