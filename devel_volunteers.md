# Volunteers Needed!

## Want to Contribute?

Every contribution is welcome, be it new features or bug-fixes. Even a single issue reported can be a vital contribution. In most cases, developers add new functionality or fix issues based on the requirements of their  own projects, but many times individuals have approached with the generous will to help improve Godot. 

This is a difficult situation, because fixing bugs it not often a very fun or interesting proposal and adding new features might need planning or can overlap with current work in progress.

The goal is this page is to list tasks that are stalled and would benefit enormously from a helping hand, organized by category.

## Porting

### Flash Platform

This platform is stalled. The code in the repository was never tested. Adobe released Cross Bridge, which enables C++ code to run on the flash VM at pretty decent performance. The status of cross bridge is not clear and flash seems to be fading out as a platform, but support for it is still really strong.

### HTML5 Platform

The EMScripten backend (javascript) generally works well in Firefox, Chrome and Safari. It seems to be not working in Internet Explorer 11. Unfortunately, Godot authors are not very experienced in this platform, so further work is stalled. Help with this from someone experienced in EMScripten and HTML5 would be very appreciated.

### X11 Platform

A PulseAudio backend might be needed too, as some users have problems with ALSA backend while PulseAudio runs. If you have experience with this platform help is appreciated! 

## Signing

### Jarsigner

We would like to replace the dependency on jarsigner by our own signing process for Android, this way we can remove the dependency on JDK, but we don't completely understand how this signing process works, so help is appreciated!

### Codesign

Generating our own IPAs seems easy and there are tools to install them on iOS devices even under Linux or Windows, but we don't know much how the signature process works. Can you help us implement this on the iOS exporter, so Godot can do one click deploy to iOS devices under any OS?



## REST APIs

Making commercial games on mobile devices very often requires access to specific platform APIs such as ADs, analytcs, payments, monetization, install tracking, leaderboards, social networks, etc. From the most hippie-indie to the most unscrupulous-commercial of games always needs some interaction with these. Integrating these APIs to Godot is often very annoying because it requires to integrate SDKs written in different languages (Java/ObjC) to each platform and making custom binaries or templates. 

These APIs however (such as ADMob, Facebook, Play Services, etc) are in most of the cases available as REST, which enables them to function in all platforms with a single implementation, by just using HTTP, SSL and JSON (all well supported by Godot). 

## Assets

### Demo Content

If you are a capable artist and want to contribute some scenes as demo content, that would be very welcome.

### Asset Workflow

If you are an artist with industry experience, help would be very appreciated on improving the asset workflow.

## AI

### General AI

What kind of AI APIS are the most useful in the industry? Help defining this would, again, be appreciated.

## Editor Plugins

### Documenting Plugins

Most of the plug-in API is undocumented and it's not obvious how it works. Help with this would be very appreciated.

### Example Plugins

Godot supports plugins in the editor, but none exists yet. Example plugins for simple features might be a nice starting point.

### Terrain Plugin

The engine lacks support for an editable terrain, this could be done easily with a plugin. A terrain engine would be a very appreciated contribution.

## Contacting developers

Godot developers can be most easily reached via forum or irc (see http://www.godotengine.org for links).

