# Creating Android Modules

### Introduction

Making videogames portable is all fine and dandy, until mobile gaming monetization shows up.
This area is complex, usually a mobile game that monetizes needs special connections to a server for stuff such as:

* Analytics
* In-App Purchases
* Receipt Validation
* Install Tracking
* ADs
* Video ADs
* Cross Promotion
* In-Game Soft & Hard Currencies
* Promo Codes
* A/B Testing
* Login
* Cloud Saves
* Leaderboards and Scores
* User Support & Feedback
* Posting to Facebook, Twitter, Etc.
* Push Notifications

Oh yeah, developing for mobile is a lot of work. On iOS, you can just write a C++ module and take advantage of the C++/ObjC intercommunication, so this is rather easy.

But Android uses Java. Yes, I know your pain.. if it wasn't for Google, ironically, Java would be dead in anything related to frontend. Thanks Google (not).

for C++ developers Java is a pain, the build system is severely bloated and interfacing it with C++ through JNI (Java Native Interface) is more pain that you don't want even for your worst enemy.

### Maybe REST?

Most of these APIs allow communication via REST+JSON APIs. Godot has great support for HTTP, HTTPS and JSON, so consider this as an option that works in every platform. Only write the code once and you are set to go.

Popular engines that have half the share of apps published on mobile get special plugins written just for them. Godot does not have that luxury yet. So, if you write a REST implementation of a SDK for Godot, please share it with the community.

### Android Module

Writing an Android module is similar to [writing a C++ module](custom_modules), but needs a few more steps.

#### config.py

In the config.py for the module, some extra functions are provided for convenience. First, it's often wise to detect if android is being built and only enable building in this case:

```python
def can_build(plat):
        return plat=="android"
```

If more than one platform can be built (typical if implementing the module also for iOS), check manually for Android in the configure functions:

```python
def can_build(plat):
        return plat=="android" or plat=="iphone"

def configure(env):
        if env['platform'] == 'android':
                 #androd specific code
  
```

### Java Singleton

An android module will usually have a singleton class that will load it, this class inherits from Godot.SingletonBase. A singleton object template follows

```java

//namespace is wrong, will eventually change
package com.android.godot;

public class MySingleton extends Godot.SingletonBase {


    public int myFunction(String p_str) {
          // a function to bind
    }

    static public Godot.SingletonBase initialize(Activity p_activity) {

                return new MySingleton(p_activity);
    } 

    public MySingleton(Activity p_activity) {
          //register class name and functions to bind
          registerClass("MySingleton", new String[]{"myFunction"});

          // you might want to try initializing your singleton here, but android
          // threads are weird and this runs in another thread, so you usually have to do
          activity.runOnUiThread(new Runnable() {
               public void run() {
                    //useful way to get config info from engine.cfg
                    String key = GodotLib.getGlobal("plugin/api_key");
                    SDK.initializeHere();
               }
          });

    }

     // forwarded callbacks you can reimplement, as SDKs often need them

     protected void onMainActivityResult(int requestCode, int resultCode, Intent data) {}

     protected void onMainPause() {}
     protected void onMainResume() {}
     protected void onMainDestroy() {}

     protected void onGLDrawFrame(GL10 gl) {}
     protected void onGLSurfaceChanged(GL10 gl, int width, int height) {} // singletons will always miss first onGLSurfaceChanged call
     
}
```

Add this singleton to the build of the project by adding the following to config.py

```python
def can_build(plat):
        return plat=="android" or plat=="iphone"

def configure(env):
        if env['platform'] == 'android':
              # will copy this to the java folder
              env.android_module_file("MySingleton.java")
              #env.android_module_file("MySingleton2.java") call again for more files

  
```
### AndroidManifest

Some SDKs need custom values in AndroidManifest.xml. Permissions can be edited from the godot exporter so there is no need to add those, but maybe other functionalities are needed. 

Create the custom chunk of android manifest and put it inside the module, add it like this:

```python
def can_build(plat):
        return plat=="android" or plat=="iphone"

def configure(env):
        if env['platform'] == 'android':
              # will copy this to the java folder
              env.android_module_file("MySingleton.java") 
              env.android_module_manifest("AndroidManifestChunk.xml")
 
```

### SDK Library

So, finally it's time to add the SDK library. Many times the library will 

