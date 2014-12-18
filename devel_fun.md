# Fun tasks!

The following is a list of fun tasks to do. If you want to work on any of them, let the developers know on the [Developer's Mailing List](https://groups.google.com/forum/#!forum/godot-engine).

Do you have a task in mind not present here? Please let us know!

### Terrain Support

Godot lacks a terrain engine. Most modern engines have this. Be it based on height-map or marching-cubes like. If you have experience with these kind of tools (either creating them or using them), Proposals Welcome!

### Demos on Mobile

Many Godot demos do not work well on mobile because touchscreen input methods are not supported. If you want to give it a try implementing this, let us know!

### Windows Installer

Are you familiar with Windows installers? We are looking for someone that might be interested in making one for Windows, that can install Godot, latest templates and latest demos. 
Templates and binaries are built under Linux currently, so the install system used should be able to execute and generate the packages from either Linux or Wine on linux, on command line. As far as we know, NSIS supports this.

### Binding GDScript to Java

Are you a capable Android developer and a master of Java? Godot has some code for binding Android API directly to GDScript, so the need to write native Java code for special features or integrating SDKs is reduced. This feature is done, but needs testing and making sure it's usable.

### Binding GDScript to Objective C

Are you a capable iOS developer? We would love to be able to make the Objective C iOS API available to GDScript. This should be possible given the dynamic nature of Objective C, but the main Godot developers are not that familiar with the language.

### Optimization

Are you good at optimization? If you love vtune or valgrind, know your simd and know the cache levels better than your neighbourhood, you could help us enormously. Godot is fast and has been written with most common optimizations in consideration, but not every part of it is as optimal as it can be and we are also not experts on the matter. If you believe this is for you, this task would consist of:

* Defining and creating common case scenarios for stress testing.
* Find ways to best optimize, either making the code faster or using more efficient algorithms.

### Size Optimization

Do you know what ELF and COFF means, and are familiar with how compiler tweaking works? We would like to make Godot binary smaller, but we don't have much experience with this. We know it's possible though, so if you have this kind of experience, please help us!

### RTL text support

Right-To-Left text support is missing (Arabic, Hebrew). If you are familiar with this (the main developers are not), please lend us a hand.

### IME Support

Input methods for complex non-latin character sets such as Chinese, Japanese or Korean is missing. If you are familiar with this, please lend us a hand.

### Keyboard Layout Mapping

Godot is missing keyboard layout tables to remap the scancodes, this makes working in some keyboard layouts a little inconvenient. Again, if you are familiar with these layouts, please lend us a hand.