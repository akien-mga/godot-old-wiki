**Important:** This wiki is soon going to be taken down, as the official documentation of the Godot project is now on http://docs.godotengine.org.

#  Reference  
####**Inherits:** [Object](class_object)
####**Category:** Core

###  Brief Description  
Base class for anything refcounted.

###  Member Functions 
  * [bool](class_bool)  **[init&#95;ref](#init_ref)**  **(** **)**
  * void  **[reference](#reference)**  **(** **)**
  * [bool](class_bool)  **[unreference](#unreference)**  **(** **)**

###  Description  
Base class for anything refcounted. Resource and many other helper objects inherit this. References keep an internal reference counter so they are only released when no longer in use.

###  Member Function Description  

#### <a name="reference">reference</a>
  * void  **reference**  **(** **)**

Increase the internal reference counter. Use this only if you really know what you are doing.

#### <a name="unreference">unreference</a>
  * [bool](class_bool)  **unreference**  **(** **)**

Decrease the internal reference counter. Use this only if you really know what you are doing.
