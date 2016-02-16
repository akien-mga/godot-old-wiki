**Important:** This wiki is soon going to be taken down, as the official documentation of the Godot project is now on http://docs.godotengine.org.

#  Input  
####**Inherits:** [Object](class_object)
####**Category:** Core

###  Brief Description  


###  Member Functions 
  * [bool](class_bool)  **[is&#95;key&#95;pressed](#is_key_pressed)**  **(** [int](class_int) scancode  **)**
  * [bool](class_bool)  **[is&#95;mouse&#95;button&#95;pressed](#is_mouse_button_pressed)**  **(** [int](class_int) button  **)**
  * [bool](class_bool)  **[is&#95;joy&#95;button&#95;pressed](#is_joy_button_pressed)**  **(** [int](class_int) device, [int](class_int) button  **)**
  * [bool](class_bool)  **[is&#95;action&#95;pressed](#is_action_pressed)**  **(** [String](class_string) action  **)**
  * [float](class_float)  **[get&#95;joy&#95;axis](#get_joy_axis)**  **(** [int](class_int) device, [int](class_int) axis  **)**
  * [String](class_string)  **[get&#95;joy&#95;name](#get_joy_name)**  **(** [int](class_int) device  **)**
  * [Vector3](class_vector3)  **[get&#95;accelerometer](#get_accelerometer)**  **(** **)**
  * [Vector2](class_vector2)  **[get&#95;mouse&#95;speed](#get_mouse_speed)**  **(** **)** const
  * [int](class_int)  **[get&#95;mouse&#95;button&#95;mask](#get_mouse_button_mask)**  **(** **)** const
  * void  **[set&#95;mouse&#95;mode](#set_mouse_mode)**  **(** [int](class_int) mode  **)**
  * [int](class_int)  **[get&#95;mouse&#95;mode](#get_mouse_mode)**  **(** **)** const
  * void  **[warp&#95;mouse&#95;pos](#warp_mouse_pos)**  **(** [Vector2](class_vector2) to  **)**
  * void  **[action&#95;press](#action_press)**  **(** [String](class_string) arg0  **)**
  * void  **[action&#95;release](#action_release)**  **(** [String](class_string) arg0  **)**

###  Signals  
  *  **joy&#95;connection&#95;changed**  **(** [int](class_int) index, [bool](class_bool) connected  **)**

###  Numeric Constants  
  * **MOUSE_MODE_VISIBLE** = **0**
  * **MOUSE_MODE_HIDDEN** = **1**
  * **MOUSE_MODE_CAPTURED** = **2**

###  Member Function Description  
