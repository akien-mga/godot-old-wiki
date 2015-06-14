# Requirements

For compiling under Windows, the following is requiered:

*  [Visual C++](http://www.microsoft.com/visualstudio) Visual C++ or Visual C++ Express compiler.
*  [Python 2.7+](http://www.python.org/getit/releases/2.7/) Python 2.7+ (3.0 is untested as of now). Using the 32-bits installer is recommended.
*  [SCons](http://www.scons.org) SCons build system.

# Setting Up SCons

Python adds the interpreter (python.exe) to the path. It usually installs in C:\Python (or C:\Python[Version]). SCons installs inside the python install and provides a .bat file called "scons.bat". The location of this file can be added to the path or it can simply be copied to C:\Python together with the interpreter executable.


# Compiling

Start a Visual Studio command prompt (it sets up environment variables needed by SCons to locate the compiler and SDK), go to the root dir of the engine source code and type:
```
C:\godot> scons platform=windows
```

If all goes well, the resulting binary executable will be placed in C:\godot\bin\godot_win.exe. This executable file contains the whole engine and runs without any dependencies. Executing it will bring up the project manager.

# Development in Visual Studio or other IDEs

For most projects, using only scripting is enough but when development in C++ is needed, for creating modules or extending the engine, working with an IDE is usually desirable. The visual studio command prompt calls a .bat file that sets up environment variables (vcvarsall.bat). To build the whole engine from a single command outside the command prompt, the following should be called in a .bat file:
```
C:\path_to_sdk\vcvarsall.bat &&  scons bin/godot_win.exe
```

**NOTE:** It seems the latest Visual Studio does not include a desktop command prompt (No, Native tools for x86 is not it). The only way to build it seems to be by running:

```
"C:\Program Files (x86)\Microsoft Visual Studio 12.0\VC\vcvarsall.bat" && c:\python27\scons p=windows
```

(or however your VS and Scons are installed)


# Cross Compiling

If you are a Linux or Mac user, you need to install mingw32 and mingw-w64. Under Ubuntu or Debian, just run the following commands:

```
apt-get install mingw32 mingw-w64
```

If you are using other distro, scons will check for the following binaries:

```
i586-mingw32msvc-gcc
i686-w64-mingw32-gcc
```

If the binaries are named or located somewhere else, export the following env variables:

```
export MINGW32_PREFIX="/path/to/i586-mingw32msvc-"
export MINGW64_PREFIX="/path/to/i686-w64-mingw32-"
```

To make sure you are doing things correctly, executing the following in the shell should result in a working compiler:

```
user@host:~$ ${MINGW32_PREFIX}gcc
gcc: fatal error: no input files
```

# Creating Windows Export Templates

Windows export templates are created by compiling Godot as release, with the following flags:

(for 32 bits, using Mingw32 command prompt or Visual Studio command prompt)
```
C:\godot> scons platform=windows tools=no target=release bits=32
C:\godot> scons platform=windows tools=no target=release_debug bits=32
```
(for 64 bits, using Mingw-w64 or Visual Studio command prompt)
```
C:\godot> scons platform=windows tools=no target=release bits=64
C:\godot> scons platform=windows tools=no target=release_debug bits=64
```

If you plan on replacing the standard templates, copy these to:
```
C:\USERS\YOURUSER\AppData\Roaming\Godot\Templates
```
With the following names:
```
windows_32_debug.exe
windows_32_release.exe
windows_64_debug.exe
windows_64_release.exe
```

However, if you are writing your custom modules or custom C++ code, you might instead want to configure your binaries as custom export templates here:

<p align="center"><img src="images/wintemplates.png"></p>

You don't even need to copy them, you can just reference the resulting files in the bin\ directory of your Godot source folder, so the next time you build you automatically have the custom templates referenced.




(c) Juan Linietsky, Ariel Manzur, Distributed under the terms of the [CC By](https://creativecommons.org/licenses/by/3.0/legalcode) license.