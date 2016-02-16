**Important:** This wiki is soon going to be taken down, as the official documentation of the Godot project is now on http://docs.godotengine.org.

#  Matrix3  
####**Category:** Built-In Types

###  Brief Description  
3x3 matrix datatype.

###  Member Functions 
  * [float](class_float)  **[determinant](#determinant)**  **(** **)**
  * [Vector3](class_vector3)  **[get&#95;euler](#get_euler)**  **(** **)**
  * [int](class_int)  **[get&#95;orthogonal&#95;index](#get_orthogonal_index)**  **(** **)**
  * [Vector3](class_vector3)  **[get&#95;scale](#get_scale)**  **(** **)**
  * [Matrix3](class_matrix3)  **[inverse](#inverse)**  **(** **)**
  * [Matrix3](class_matrix3)  **[orthonormalized](#orthonormalized)**  **(** **)**
  * [Matrix3](class_matrix3)  **[rotated](#rotated)**  **(** [Vector3](class_vector3) axis, [float](class_float) phi  **)**
  * [Matrix3](class_matrix3)  **[scaled](#scaled)**  **(** [Vector3](class_vector3) scale  **)**
  * [float](class_float)  **[tdotx](#tdotx)**  **(** [Vector3](class_vector3) with  **)**
  * [float](class_float)  **[tdoty](#tdoty)**  **(** [Vector3](class_vector3) with  **)**
  * [float](class_float)  **[tdotz](#tdotz)**  **(** [Vector3](class_vector3) with  **)**
  * [Matrix3](class_matrix3)  **[transposed](#transposed)**  **(** **)**
  * [Vector3](class_vector3)  **[xform](#xform)**  **(** [Vector3](class_vector3) v  **)**
  * [Vector3](class_vector3)  **[xform&#95;inv](#xform_inv)**  **(** [Vector3](class_vector3) v  **)**
  * [Matrix3](class_matrix3)  **[Matrix3](#Matrix3)**  **(** [Vector3](class_vector3) x_axis, [Vector3](class_vector3) y_axis, [Vector3](class_vector3) z_axis  **)**
  * [Matrix3](class_matrix3)  **[Matrix3](#Matrix3)**  **(** [Vector3](class_vector3) axis, [float](class_float) phi  **)**
  * [Matrix3](class_matrix3)  **[Matrix3](#Matrix3)**  **(** [Quat](class_quat) from  **)**

###  Member Variables  
  * [Vector3](class_vector3) **x**
  * [Vector3](class_vector3) **y**
  * [Vector3](class_vector3) **z**

###  Description  
3x3 matrix used for 3D rotation and scale. Contains 3 vector fields x,y and z. Can also be accessed as array of 3D vectors. Almost always used as orthogonal basis for a [Transform](class_transform).

###  Member Function Description  

#### <a name="determinant">determinant</a>
  * [float](class_float)  **determinant**  **(** **)**

Return the determinant of the matrix.

#### <a name="get_euler">get_euler</a>
  * [Vector3](class_vector3)  **get&#95;euler**  **(** **)**

Return euler angles from the matrix.

#### <a name="inverse">inverse</a>
  * [Matrix3](class_matrix3)  **inverse**  **(** **)**

Return the affine inverse of the matrix.

#### <a name="orthonormalized">orthonormalized</a>
  * [Matrix3](class_matrix3)  **orthonormalized**  **(** **)**

Return the orthonormalized version of the matrix (useful to call from time to time to avoid rounding error).

#### <a name="rotated">rotated</a>
  * [Matrix3](class_matrix3)  **rotated**  **(** [Vector3](class_vector3) axis, [float](class_float) phi  **)**

Return the rotated version of the matrix, by a given axis and angle.

#### <a name="scaled">scaled</a>
  * [Matrix3](class_matrix3)  **scaled**  **(** [Vector3](class_vector3) scale  **)**

Return the scaled version of the matrix, by a 3D scale.

#### <a name="tdotx">tdotx</a>
  * [float](class_float)  **tdotx**  **(** [Vector3](class_vector3) with  **)**

Transposed dot product with the x axis of the matrix.

#### <a name="tdoty">tdoty</a>
  * [float](class_float)  **tdoty**  **(** [Vector3](class_vector3) with  **)**

Transposed dot product with the y axis of the matrix.

#### <a name="tdotz">tdotz</a>
  * [float](class_float)  **tdotz**  **(** [Vector3](class_vector3) with  **)**

Transposed dot product with the z axis of the matrix.

#### <a name="transposed">transposed</a>
  * [Matrix3](class_matrix3)  **transposed**  **(** **)**

Return the transposed version of the matrix.

#### <a name="xform">xform</a>
  * [Vector3](class_vector3)  **xform**  **(** [Vector3](class_vector3) v  **)**

Return a vector transformed by the matrix and return it.

#### <a name="xform_inv">xform_inv</a>
  * [Vector3](class_vector3)  **xform&#95;inv**  **(** [Vector3](class_vector3) v  **)**

Return a vector transformed by the transposed matrix and return it.

#### <a name="Matrix3">Matrix3</a>
  * [Matrix3](class_matrix3)  **Matrix3**  **(** [Vector3](class_vector3) x_axis, [Vector3](class_vector3) y_axis, [Vector3](class_vector3) z_axis  **)**

Create a matrix from 3 axis vectors.

#### <a name="Matrix3">Matrix3</a>
  * [Matrix3](class_matrix3)  **Matrix3**  **(** [Vector3](class_vector3) axis, [float](class_float) phi  **)**

Create a matrix from an axis vector and an angle.

#### <a name="Matrix3">Matrix3</a>
  * [Matrix3](class_matrix3)  **Matrix3**  **(** [Quat](class_quat) from  **)**

Create a matrix from a quaternion.
