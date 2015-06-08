#Compiling for Linux
### Requirements

For compiling under Linux or other Unix variants, the following is requiered:

*  GCC or LLVM 
*  Python 2.7+ (3.0 is untested as of now).
*  SCons build system.
*  X11 and MESA development Libraries
*  Xinerama Libraries
*  ALSA development libraries
*  Freetype (for the editor)
*  OpenSSL (for HTTPS and TLS)
*  pkg-config (used to detect the above three)
*  **Ubuntu Users:** apt-get install scons pkg-config libx11-dev libxcursor-dev build-essential libasound2-dev libfreetype6-dev libgl1-mesa-dev libglu-dev libssl-dev libxinerama-dev

### Compiling

Start a terminal, go to the root dir of the engine source code and type:
```
user@host:~/godot$ scons platform=x11
```

If all goes well, the resulting binary executable will be placed in the "bin" subdirectory. This executable file contains the whole engine and runs without any dependencies. Executing it will bring up the project manager.

### Building Export Templates

To build Linux export templates, run the build system with the following parameters:

(32 bits)
```
user@host:~/godot$ scons platform=x11 tools=no target=release bits=32
user@host:~/godot$ scons platform=x11 tools=no target=release_debug bits=32
```
(64 bits)
```
user@host:~/godot$ scons platform=x11 tools=no target=release bits=64
user@host:~/godot$ scons platform=x11 tools=no target=release_debug bits=64
```

Note that cross compiling for the opposite bits (64/32) as your host platform in linux is quite difficult and might need a chroot environment. 

In Ubuntu, compilation works without a chroot but some libraries (.so) might be missing from /usr/lib32. Sym-linking the missing .so files from /usr/lib results in a working build.

To create standard export templates, the resulting files must be copiled to:

```
/home/youruser/.godot/templates
```

and named like this:

```
linux_x11_32_debug
linux_x11_32_release
linux_x11_64_debug
linux_x11_64_release
```

However, if you are writing your custom modules or custom C++ code, you might instead want to configure your binaries as custom export templates here:

<p align="center"><img src="images/lintemplates.png"></p>

You don't even need to copy them, you can just reference the resulting files in the bin/ directory of your Godot source folder, so the next time you build you automatically have the custom templates referenced.



(c) Juan Linietsky, Ariel Manzur, Distributed under the terms of the [CC By](https://creativecommons.org/licenses/by/3.0/legalcode) license.
