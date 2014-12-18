
# Not so Fun tasks!

The following is a list of not so fun tasks to do. We believe they are still fun for the right people, but require a noticeable higher degree of technical expertise. If you want to work on any of them, let the developers know on the [Developer's Mailing List](https://groups.google.com/forum/#!forum/godot-engine).

### Flash Platform

This platform is stalled. The code in the repository was never tested. Adobe released Cross Bridge, which enables C++ code to run on the flash VM at pretty decent performance. The status of cross bridge is not clear and flash seems to be fading out as a platform, but support for it is still really strong.

### HTML5 Platform Maintainer

The EMScripten backend (javascript) generally works well in Firefox, Chrome and Safari. It seems to be not working in Internet Explorer 11. Unfortunately, Godot authors are not very experienced in this platform, so further work is stalled. 

If you are knowledgeable in HTML5 (and have some idea of emscripten and/or believe you can learn it), we need you to help make this platform work smoothly!

### X11 Platform

A PulseAudio backend might be needed for audio, as some users have problems with ALSA backend while PulseAudio runs. If you have experience with PA, help is appreciated! 

### Android Signing and Jarsigner

We would like to replace the dependency on jarsigner by our own signing process for Android, this way we can remove the dependency on JDK, but we don't completely understand how this signing process works, so help is appreciated!

### iOS Signing and Codesign

Generating our own IPAs seems easy and there are tools to install them on iOS devices even under Linux or Windows, but we don't know much how the signature process works. Can you help us implement this on the iOS exporter, so Godot can do one click deploy to iOS devices under any OS?

### REST APIs

Making commercial games on mobile devices very often requires access to specific platform APIs such as ADs, analytcs, payments, monetization, install tracking, leaderboards, social networks, etc. From the most hippie-indie to the most unscrupulous-commercial of games always needs some interaction with these. Integrating these APIs to Godot is often very annoying because it requires to integrate SDKs written in different languages (Java/ObjC) to each platform and making custom binaries or templates. 

These APIs however (such as ADMob, Facebook, Play Services, etc) are in most of the cases available as REST, which enables them to function in all platforms with a single implementation, by just using HTTP, SSL and JSON (all well supported by Godot). 

If you want to write support for popular web APIs (Such as Google Play Services) as REST, please let us know!

### General AI

What kind of AI APIS are the most useful in the industry? Help defining this would, again, be appreciated.

### Windows Phone / Windows 8

The current "winrt" platform is mostly ready, but needs a couple of key features to become a proper "first class citizen" supported platform. On the code side, the main one is an Audio driver, and a few minor issues with the threading classes (Thread is implemented using std::thread, we'd prefer using native winrt APIs, semaphores are not implemented). There's also the usual "app lifecycle" stuff missing (dealing with screen rotation, events like focus lost, back button, etc), and keyboard input (and possibly dealing with the on-screen keyboard). On the "workflow" side, we need to add "one click deploy" from the editor, which means packaging the app and launching it to a connected device (or launching as a "windows store app" from a local directory on the local machine), and eventually packaging for submission to Windows Store.