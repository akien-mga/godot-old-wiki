## Exporting for Android

Exporting for android has much less requirements than compiling Godot for it. As follows are the steps to setup the SDK and the engine.

#### Download the Android SDK

Download and install the Android SDK from http://developer.android.com/sdk/index.html

#### Download the Java 6 or OpenJDK6

Download and install Java 6 or OpenJDK 6, Android needs this version and it seems that jarsigner (what is used to sign APKs) from greater versions do not work.

#### Create a debug.keystore

Android needs a debug keystore file to install to devices and distribute non-release APKs. If you have used the SDK before and have built projects, ant or eclipse probably generated one for you (In Linux and OSX, you can find it in the ~/.android folder).

If you can't find it or need to generate one, the keytool command from the JDK can be used for this purpose:

```
keytool -keyalg RSA -genkeypair -alias androiddebugkey -keypass android -keystore debug.keystore -storepass android -dname "CN=Android Debug,O=Android,C=US" -validity 9999
```

#### Make sure you have adb

ADB is the command line tool used to communicate with Android devices. It's installed with the SDK, but you may need to install one (any) of the Android API levels for it to be installed in the SDK directory.

#### Setting it up in Godot

Enter the Editor Settings screen. This screens contains the editor settings for the user account in the computer (It's independent from the project).

<p align="center"><img src="images/editorsettings.png"></p>

Scroll down to the section where the Android settings are located:

<p align="center"><img src="images/androidsdk.png"></p>

In that screen, the path to 3 files needs to be set:

*  The adb executable (adb.exe on Windows)
*  The jarsigner executable (from JDK6)
*  The debug keystore

Once that is configured, everything is ready to export to Android!



(c) Juan Linietsky, Ariel Manzur, Distributed under the terms of the [CC By](https://creativecommons.org/licenses/by/3.0/legalcode) license.
