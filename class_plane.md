#  Plane  
####**Category:** Built-In Types

###  Brief Description  
Plane in hessian form.

###  Member Functions 
  * [Vector3](class_vector3)  **[center](#center)**  **(** **)**
  * [float](class_float)  **[distance&#95;to](#distance_to)**  **(** [Vector3](class_vector3) point  **)**
  * [Vector3](class_vector3)  **[get&#95;any&#95;point](#get_any_point)**  **(** **)**
  * [bool](class_bool)  **[has&#95;point](#has_point)**  **(** [Vector3](class_vector3) point, [float](class_float) epsilon=0.00001  **)**
  * [Vector3](class_vector3)  **[intersect&#95;3](#intersect_3)**  **(** [Plane](class_plane) b, [Plane](class_plane) c  **)**
  * [Vector3](class_vector3)  **[intersects&#95;ray](#intersects_ray)**  **(** [Vector3](class_vector3) from, [Vector3](class_vector3) dir  **)**
  * [Vector3](class_vector3)  **[intersects&#95;segment](#intersects_segment)**  **(** [Vector3](class_vector3) begin, [Vector3](class_vector3) end  **)**
  * [bool](class_bool)  **[is&#95;point&#95;over](#is_point_over)**  **(** [Vector3](class_vector3) point  **)**
  * [Plane](class_plane)  **[normalized](#normalized)**  **(** **)**
  * [Vector3](class_vector3)  **[project](#project)**  **(** [Vector3](class_vector3) point  **)**
  * [Plane](class_plane)  **[Plane](#Plane)**  **(** [float](class_float) a, [float](class_float) b, [float](class_float) c, [float](class_float) d  **)**
  * [Plane](class_plane)  **[Plane](#Plane)**  **(** [Vector3](class_vector3) v1, [Vector3](class_vector3) v2, [Vector3](class_vector3) v3  **)**
  * [Plane](class_plane)  **[Plane](#Plane)**  **(** [Vector3](class_vector3) normal, [float](class_float) d  **)**

###  Member Variables  
  * [Vector3](class_vector3) **normal**
  * [float](class_float) **x**
  * [float](class_float) **y**
  * [float](class_float) **z**
  * [float](class_float) **d**

###  Description  
Plane represents a normalized plane equation. Basically, "normal" is the normal of the plane (a,b,c normalized), and "d" is the distance from the origin to the plane (in the direction of "normal"). "Over" or "Above" the plane is considered the side of the plane towards where the normal is pointing.

###  Member Function Description  

#### <a name="center">center</a>
  * [Vector3](class_vector3)  **center**  **(** **)**

Returns the center of the plane.

#### <a name="distance_to">distance_to</a>
  * [float](class_float)  **distance&#95;to**  **(** [Vector3](class_vector3) point  **)**

Returns the shortest distance from the plane to the position "point".

#### <a name="get_any_point">get_any_point</a>
  * [Vector3](class_vector3)  **get&#95;any&#95;point**  **(** **)**

Returns a point on the plane.

#### <a name="has_point">has_point</a>
  * [bool](class_bool)  **has&#95;point**  **(** [Vector3](class_vector3) point, [float](class_float) epsilon=0.00001  **)**

Returns true if "point" is inside the plane (by a very minimum treshold).

#### <a name="intersect_3">intersect_3</a>
  * [Vector3](class_vector3)  **intersect&#95;3**  **(** [Plane](class_plane) b, [Plane](class_plane) c  **)**

Returns the intersection point of the three planes "b", "c" and this plane. If no intersection is found null is returned.

#### <a name="intersects_ray">intersects_ray</a>
  * [Vector3](class_vector3)  **intersects&#95;ray**  **(** [Vector3](class_vector3) from, [Vector3](class_vector3) dir  **)**

Returns the intersection point of a ray consisting of the position "from" and the direction normal "dir" with this plane. If no intersection is found null is returned.

#### <a name="intersects_segment">intersects_segment</a>
  * [Vector3](class_vector3)  **intersects&#95;segment**  **(** [Vector3](class_vector3) begin, [Vector3](class_vector3) end  **)**

Returns the intersection point of a segment from position "begin" to position "end" with this plane. If no intersection is found null is returned.

#### <a name="is_point_over">is_point_over</a>
  * [bool](class_bool)  **is&#95;point&#95;over**  **(** [Vector3](class_vector3) point  **)**

Returns true if "point" is located above the plane.

#### <a name="normalized">normalized</a>
  * [Plane](class_plane)  **normalized**  **(** **)**

Returns a copy of the plane, normalized.

#### <a name="project">project</a>
  * [Vector3](class_vector3)  **project**  **(** [Vector3](class_vector3) point  **)**

Returns the orthogonal projection of point "p" into a point in the plane.

#### <a name="Plane">Plane</a>
  * [Plane](class_plane)  **Plane**  **(** [float](class_float) a, [float](class_float) b, [float](class_float) c, [float](class_float) d  **)**

Creates a plane from the three parameters "a", "b", "c" and "d".

#### <a name="Plane">Plane</a>
  * [Plane](class_plane)  **Plane**  **(** [Vector3](class_vector3) v1, [Vector3](class_vector3) v2, [Vector3](class_vector3) v3  **)**

Creates a plane from three points.

#### <a name="Plane">Plane</a>
  * [Plane](class_plane)  **Plane**  **(** [Vector3](class_vector3) normal, [float](class_float) d  **)**

Creates a plane from the normal and the plane's distance to the origin.


(c) Juan Linietsky, Ariel Manzur, Distributed under the terms of the [CC By](https://creativecommons.org/licenses/by/3.0/legalcode) license.
