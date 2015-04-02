#  Physics2DDirectBodyState  
####**Inherits:** [Object](class_object)
####**Category:** Core

###  Brief Description  
Direct access object to a physics body in the [Physics2DServer](class_physics2dserver).

###  Member Functions 
  * [Vector2](class_vector2)  **[get&#95;total&#95;gravity](#get_total_gravity)**  **(** **)** const
  * [float](class_float)  **[get&#95;total&#95;linear&#95;damp](#get_total_linear_damp)**  **(** **)** const
  * [float](class_float)  **[get&#95;total&#95;angular&#95;damp](#get_total_angular_damp)**  **(** **)** const
  * [float](class_float)  **[get&#95;inverse&#95;mass](#get_inverse_mass)**  **(** **)** const
  * [float](class_float)  **[get&#95;inverse&#95;inertia](#get_inverse_inertia)**  **(** **)** const
  * void  **[set&#95;linear&#95;velocity](#set_linear_velocity)**  **(** [Vector2](class_vector2) velocity  **)**
  * [Vector2](class_vector2)  **[get&#95;linear&#95;velocity](#get_linear_velocity)**  **(** **)** const
  * void  **[set&#95;angular&#95;velocity](#set_angular_velocity)**  **(** [float](class_float) velocity  **)**
  * [float](class_float)  **[get&#95;angular&#95;velocity](#get_angular_velocity)**  **(** **)** const
  * void  **[set&#95;transform](#set_transform)**  **(** [Matrix32](class_matrix32) transform  **)**
  * [Matrix32](class_matrix32)  **[get&#95;transform](#get_transform)**  **(** **)** const
  * void  **[set&#95;sleep&#95;state](#set_sleep_state)**  **(** [bool](class_bool) enabled  **)**
  * [bool](class_bool)  **[is&#95;sleeping](#is_sleeping)**  **(** **)** const
  * [int](class_int)  **[get&#95;contact&#95;count](#get_contact_count)**  **(** **)** const
  * [Vector2](class_vector2)  **[get&#95;contact&#95;local&#95;pos](#get_contact_local_pos)**  **(** [int](class_int) contact_idx  **)** const
  * [Vector2](class_vector2)  **[get&#95;contact&#95;local&#95;normal](#get_contact_local_normal)**  **(** [int](class_int) contact_idx  **)** const
  * [int](class_int)  **[get&#95;contact&#95;local&#95;shape](#get_contact_local_shape)**  **(** [int](class_int) contact_idx  **)** const
  * [RID](class_rid)  **[get&#95;contact&#95;collider](#get_contact_collider)**  **(** [int](class_int) contact_idx  **)** const
  * [Vector2](class_vector2)  **[get&#95;contact&#95;collider&#95;pos](#get_contact_collider_pos)**  **(** [int](class_int) contact_idx  **)** const
  * [int](class_int)  **[get&#95;contact&#95;collider&#95;id](#get_contact_collider_id)**  **(** [int](class_int) contact_idx  **)** const
  * [Object](class_object)  **[get&#95;contact&#95;collider&#95;object](#get_contact_collider_object)**  **(** [int](class_int) contact_idx  **)** const
  * [int](class_int)  **[get&#95;contact&#95;collider&#95;shape](#get_contact_collider_shape)**  **(** [int](class_int) contact_idx  **)** const
  * void  **[get&#95;contact&#95;collider&#95;shape&#95;metadata](#get_contact_collider_shape_metadata)**  **(** [int](class_int) contact_idx  **)** const
  * [Vector2](class_vector2)  **[get&#95;contact&#95;collider&#95;velocity&#95;at&#95;pos](#get_contact_collider_velocity_at_pos)**  **(** [int](class_int) contact_idx  **)** const
  * [float](class_float)  **[get&#95;step](#get_step)**  **(** **)** const
  * void  **[integrate&#95;forces](#integrate_forces)**  **(** **)**
  * [Physics2DDirectSpaceState](class_physics2ddirectspacestate)  **[get&#95;space&#95;state](#get_space_state)**  **(** **)**

###  Description  
Direct access object to a physics body in the [Physics2DServer](class_physics2dserver). This object is passed via the direct state callback of rigid/character bodies, and is intended for changing the direct state of that body.

###  Member Function Description  

#### <a name="get_total_gravity">get_total_gravity</a>
  * [Vector2](class_vector2)  **get&#95;total&#95;gravity**  **(** **)** const

Return the total gravity vector being currently applied to this body.

#### <a name="get_inverse_mass">get_inverse_mass</a>
  * [float](class_float)  **get&#95;inverse&#95;mass**  **(** **)** const

Return the inverse of the mass of the body.

#### <a name="get_inverse_inertia">get_inverse_inertia</a>
  * [float](class_float)  **get&#95;inverse&#95;inertia**  **(** **)** const

Return the inverse of the inertia of the body.

#### <a name="set_linear_velocity">set_linear_velocity</a>
  * void  **set&#95;linear&#95;velocity**  **(** [Vector2](class_vector2) velocity  **)**

Change the linear velocity of the body.

#### <a name="get_linear_velocity">get_linear_velocity</a>
  * [Vector2](class_vector2)  **get&#95;linear&#95;velocity**  **(** **)** const

Return the current linear velocity of the body.

#### <a name="set_angular_velocity">set_angular_velocity</a>
  * void  **set&#95;angular&#95;velocity**  **(** [float](class_float) velocity  **)**

Change the angular velocity of the body.

#### <a name="get_angular_velocity">get_angular_velocity</a>
  * [float](class_float)  **get&#95;angular&#95;velocity**  **(** **)** const

Return the angular velocity of the body.

#### <a name="set_transform">set_transform</a>
  * void  **set&#95;transform**  **(** [Matrix32](class_matrix32) transform  **)**

Change the transform matrix of the body.

#### <a name="get_transform">get_transform</a>
  * [Matrix32](class_matrix32)  **get&#95;transform**  **(** **)** const

Return the transform matrix of the body.

#### <a name="set_sleep_state">set_sleep_state</a>
  * void  **set&#95;sleep&#95;state**  **(** [bool](class_bool) enabled  **)**

Set the sleeping state of the body, only affects character/rigid bodies.

#### <a name="is_sleeping">is_sleeping</a>
  * [bool](class_bool)  **is&#95;sleeping**  **(** **)** const

Return true if this body is currently sleeping (not active).

#### <a name="get_contact_count">get_contact_count</a>
  * [int](class_int)  **get&#95;contact&#95;count**  **(** **)** const

Return the amount of contacts this body has with other bodies. Note that by default this returns 0 unless bodies are configured to log contacts.

#### <a name="get_contact_local_pos">get_contact_local_pos</a>
  * [Vector2](class_vector2)  **get&#95;contact&#95;local&#95;pos**  **(** [int](class_int) contact_idx  **)** const

Return the local position (of this body) of the contact point.

#### <a name="get_contact_local_shape">get_contact_local_shape</a>
  * [int](class_int)  **get&#95;contact&#95;local&#95;shape**  **(** [int](class_int) contact_idx  **)** const

Return the local shape index of the collision.

#### <a name="get_contact_collider">get_contact_collider</a>
  * [RID](class_rid)  **get&#95;contact&#95;collider**  **(** [int](class_int) contact_idx  **)** const

Return the RID of the collider.

#### <a name="get_contact_collider_pos">get_contact_collider_pos</a>
  * [Vector2](class_vector2)  **get&#95;contact&#95;collider&#95;pos**  **(** [int](class_int) contact_idx  **)** const

Return the contact position in the collider.

#### <a name="get_contact_collider_id">get_contact_collider_id</a>
  * [int](class_int)  **get&#95;contact&#95;collider&#95;id**  **(** [int](class_int) contact_idx  **)** const

Return the object id of the collider.

#### <a name="get_contact_collider_object">get_contact_collider_object</a>
  * [Object](class_object)  **get&#95;contact&#95;collider&#95;object**  **(** [int](class_int) contact_idx  **)** const

Return the collider object, this depends on how it was created (will return a scene node if such was used to create it).

#### <a name="get_contact_collider_shape">get_contact_collider_shape</a>
  * [int](class_int)  **get&#95;contact&#95;collider&#95;shape**  **(** [int](class_int) contact_idx  **)** const

Return the collider shape index.

#### <a name="get_contact_collider_velocity_at_pos">get_contact_collider_velocity_at_pos</a>
  * [Vector2](class_vector2)  **get&#95;contact&#95;collider&#95;velocity&#95;at&#95;pos**  **(** [int](class_int) contact_idx  **)** const

Return the linear velocity vector at contact point of the collider.

#### <a name="get_step">get_step</a>
  * [float](class_float)  **get&#95;step**  **(** **)** const

Return the timestep (delta) used for the simulation.

#### <a name="integrate_forces">integrate_forces</a>
  * void  **integrate&#95;forces**  **(** **)**

Call the built-in force integration code.

#### <a name="get_space_state">get_space_state</a>
  * [Physics2DDirectSpaceState](class_physics2ddirectspacestate)  **get&#95;space&#95;state**  **(** **)**

Return the current state of space, useful for queries.
