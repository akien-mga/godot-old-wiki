#  NodePath  
####**Category:** Built-In Types

###  Brief Description  
Built-in type optimized for path traversing.

###  Member Functions 
  * [String](class_string)  **[get&#95;name](#get_name)**  **(** [int](class_int) idx  **)**
  * [int](class_int)  **[get&#95;name&#95;count](#get_name_count)**  **(** **)**
  * [String](class_string)  **[get&#95;property](#get_property)**  **(** **)**
  * [String](class_string)  **[get&#95;subname](#get_subname)**  **(** [int](class_int) idx  **)**
  * [int](class_int)  **[get&#95;subname&#95;count](#get_subname_count)**  **(** **)**
  * [bool](class_bool)  **[is&#95;absolute](#is_absolute)**  **(** **)**
  * [bool](class_bool)  **[is&#95;empty](#is_empty)**  **(** **)**
  * [NodePath](class_nodepath)  **[NodePath](#NodePath)**  **(** [String](class_string) from  **)**

###  Description  
Built-in type optimized for path traversing. A Node path is an optimized compiled path used for traversing the scene tree. 
        It references nodes and can reference properties in that node, or even reference properties inside the resources of the node.

###  Member Function Description  

#### <a name="get_name">get_name</a>
  * [String](class_string)  **get&#95;name**  **(** [int](class_int) idx  **)**

Return a path level name.

#### <a name="get_name_count">get_name_count</a>
  * [int](class_int)  **get&#95;name&#95;count**  **(** **)**

Return the path level count.

#### <a name="get_property">get_property</a>
  * [String](class_string)  **get&#95;property**  **(** **)**

Return the property associated (empty if none).

#### <a name="get_subname">get_subname</a>
  * [String](class_string)  **get&#95;subname**  **(** [int](class_int) idx  **)**

Return the subname level name.

#### <a name="get_subname_count">get_subname_count</a>
  * [int](class_int)  **get&#95;subname&#95;count**  **(** **)**

Return the subname count.

#### <a name="is_absolute">is_absolute</a>
  * [bool](class_bool)  **is&#95;absolute**  **(** **)**

Return true if the node path is absolute (not relative).

#### <a name="is_empty">is_empty</a>
  * [bool](class_bool)  **is&#95;empty**  **(** **)**

Return true if the node path is empty.
