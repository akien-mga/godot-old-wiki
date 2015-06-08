# Requirements

For compiling under Linux or other Unix variants, the following is requiered:

*  Python 2.7+ (3.0 is untested as of now).
*  SCons build system.
*  XCode

# Compiling

Start a terminal, go to the root dir of the engine source code and type:
```
user@host:~/godot$ scons platform=osx
```

If all goes well, the resulting binary executable will be placed in the "bin" subdirectory. This executable file contains the whole engine and runs without any dependencies. Executing it will bring up the project manager. There is a .app template to put the binary into in tools/Godot.app.



(c) Juan Linietsky, Ariel Manzur, Distributed under the terms of the [CC By](https://creativecommons.org/licenses/by/3.0/legalcode) license.
