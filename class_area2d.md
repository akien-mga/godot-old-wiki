#  Area2D  
####**Inherits:** [CollisionObject2D](class_collisionobject2d)
####**Category:** Core

###  Brief Description  
General purpose area detection and influence for 2D Phisics.

###  Member Functions 
  * void  **[set&#95;space&#95;override&#95;mode](#set_space_override_mode)**  **(** [int](class_int) enable  **)**
  * [int](class_int)  **[get&#95;space&#95;override&#95;mode](#get_space_override_mode)**  **(** **)** const
  * void  **[set&#95;gravity&#95;is&#95;point](#set_gravity_is_point)**  **(** [bool](class_bool) enable  **)**
  * [bool](class_bool)  **[is&#95;gravity&#95;a&#95;point](#is_gravity_a_point)**  **(** **)** const
  * void  **[set&#95;gravity&#95;vector](#set_gravity_vector)**  **(** [Vector2](class_vector2) vector  **)**
  * [Vector2](class_vector2)  **[get&#95;gravity&#95;vector](#get_gravity_vector)**  **(** **)** const
  * void  **[set&#95;gravity](#set_gravity)**  **(** [float](class_float) gravity  **)**
  * [float](class_float)  **[get&#95;gravity](#get_gravity)**  **(** **)** const
  * void  **[set&#95;linear&#95;damp](#set_linear_damp)**  **(** [float](class_float) linear_damp  **)**
  * [float](class_float)  **[get&#95;linear&#95;damp](#get_linear_damp)**  **(** **)** const
  * void  **[set&#95;angular&#95;damp](#set_angular_damp)**  **(** [float](class_float) angular_damp  **)**
  * [float](class_float)  **[get&#95;angular&#95;damp](#get_angular_damp)**  **(** **)** const
  * void  **[set&#95;priority](#set_priority)**  **(** [float](class_float) priority  **)**
  * [float](class_float)  **[get&#95;priority](#get_priority)**  **(** **)** const
  * void  **[set&#95;collision&#95;mask](#set_collision_mask)**  **(** [int](class_int) collision_mask  **)**
  * [int](class_int)  **[get&#95;collision&#95;mask](#get_collision_mask)**  **(** **)** const
  * void  **[set&#95;layer&#95;mask](#set_layer_mask)**  **(** [int](class_int) layer_mask  **)**
  * [int](class_int)  **[get&#95;layer&#95;mask](#get_layer_mask)**  **(** **)** const
  * void  **[set&#95;enable&#95;monitoring](#set_enable_monitoring)**  **(** [bool](class_bool) enable  **)**
  * [bool](class_bool)  **[is&#95;monitoring&#95;enabled](#is_monitoring_enabled)**  **(** **)** const
  * void  **[set&#95;monitorable](#set_monitorable)**  **(** [bool](class_bool) enable  **)**
  * [bool](class_bool)  **[is&#95;monitorable](#is_monitorable)**  **(** **)** const
  * [Array](class_array)  **[get&#95;overlapping&#95;bodies](#get_overlapping_bodies)**  **(** **)** const
  * [Array](class_array)  **[get&#95;overlapping&#95;areas](#get_overlapping_areas)**  **(** **)** const
  * [PhysicsBody2D](class_physicsbody2d)  **[overlaps&#95;body](#overlaps_body)**  **(** [Object](class_object) body  **)** const
  * [Area2D](class_area2d)  **[overlaps&#95;area](#overlaps_area)**  **(** [Object](class_object) area  **)** const

###  Signals  
  *  **body&#95;enter**  **(** [Object](class_object) body  **)**
  *  **body&#95;enter&#95;shape**  **(** [int](class_int) body_id, [Object](class_object) body, [int](class_int) body_shape, [int](class_int) area_shape  **)**
  *  **area&#95;enter**  **(** [Object](class_object) area  **)**
  *  **area&#95;enter&#95;shape**  **(** [int](class_int) area_id, [Object](class_object) area, [int](class_int) area_shape, [int](class_int) area_shape  **)**
  *  **body&#95;exit**  **(** [Object](class_object) body  **)**
  *  **body&#95;exit&#95;shape**  **(** [int](class_int) body_id, [Object](class_object) body, [int](class_int) body_shape, [int](class_int) area_shape  **)**
  *  **area&#95;exit**  **(** [Object](class_object) area  **)**
  *  **area&#95;exit&#95;shape**  **(** [int](class_int) area_id, [Object](class_object) area, [int](class_int) area_shape, [int](class_int) area_shape  **)**

###  Description  
General purpose area detection for 2D Phisics. Areas can be used for detection of objects that enter/exit them, as well as overriding space parameters (changing gravity, damping, etc). An Area2D can be set as a children to a RigidBody2D to generate a custom gravity field. For this, use SPACE_OVERRIDE_COMBINE and point gravity at the center of mass.

###  Member Function Description  

#### <a name="set_gravity_is_point">set_gravity_is_point</a>
  * void  **set&#95;gravity&#95;is&#95;point**  **(** [bool](class_bool) enable  **)**

When overriding space parameters, areas can have a center of gravity as a point.

#### <a name="is_gravity_a_point">is_gravity_a_point</a>
  * [bool](class_bool)  **is&#95;gravity&#95;a&#95;point**  **(** **)** const

Return if gravity is a point. When overriding space parameters, areas can have a center of gravity as a point.

#### <a name="set_gravity_vector">set_gravity_vector</a>
  * void  **set&#95;gravity&#95;vector**  **(** [Vector2](class_vector2) vector  **)**

Set gravity vector. If gravity is a point, this will be the attraction center


(c) Juan Linietsky, Ariel Manzur, Distributed under the terms of the [CC By](https://creativecommons.org/licenses/by/3.0/legalcode) license.
