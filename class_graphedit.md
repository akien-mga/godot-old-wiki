**Important:** This wiki is soon going to be taken down, as the official documentation of the Godot project is now on http://docs.godotengine.org.

#  GraphEdit  
####**Inherits:** [Control](class_control)
####**Category:** Core

###  Brief Description  


###  Member Functions 
  * Error  **[connect&#95;node](#connect_node)**  **(** [String](class_string) from, [int](class_int) from_port, [String](class_string) to, [int](class_int) to_port  **)**
  * [bool](class_bool)  **[is&#95;node&#95;connected](#is_node_connected)**  **(** [String](class_string) from, [int](class_int) from_port, [String](class_string) to, [int](class_int) to_port  **)**
  * void  **[disconnect&#95;node](#disconnect_node)**  **(** [String](class_string) from, [int](class_int) from_port, [String](class_string) to, [int](class_int) to_port  **)**
  * [Array](class_array)  **[get&#95;connection&#95;list](#get_connection_list)**  **(** **)** const
  * void  **[set&#95;right&#95;disconnects](#set_right_disconnects)**  **(** [bool](class_bool) enable  **)**
  * [bool](class_bool)  **[is&#95;right&#95;disconnects&#95;enabled](#is_right_disconnects_enabled)**  **(** **)** const

###  Signals  
  *  **disconnection&#95;request**  **(** [String](class_string) from, [int](class_int) from_slot, [String](class_string) to, [int](class_int) to_slot  **)**
  *  **connection&#95;request**  **(** [String](class_string) from, [int](class_int) from_slot, [String](class_string) to, [int](class_int) to_slot  **)**

###  Member Function Description  
