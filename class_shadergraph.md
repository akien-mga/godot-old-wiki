**Important:** This wiki is soon going to be taken down, as the official documentation of the Godot project is now on http://docs.godotengine.org.

#  ShaderGraph  
####**Inherits:** [Shader](class_shader)
####**Category:** Core

###  Brief Description  


###  Member Functions 
  * void  **[node&#95;add](#node_add)**  **(** [int](class_int) shader_type, [int](class_int) node_type, [int](class_int) id  **)**
  * void  **[node&#95;remove](#node_remove)**  **(** [int](class_int) shader_type, [int](class_int) id  **)**
  * void  **[node&#95;set&#95;pos](#node_set_pos)**  **(** [int](class_int) shader_type, [int](class_int) id, [Vector2](class_vector2) pos  **)**
  * [Vector2](class_vector2)  **[node&#95;get&#95;pos](#node_get_pos)**  **(** [int](class_int) shader_type, [int](class_int) id  **)** const
  * [int](class_int)  **[node&#95;get&#95;type](#node_get_type)**  **(** [int](class_int) shader_type, [int](class_int) id  **)** const
  * [Array](class_array)  **[get&#95;node&#95;list](#get_node_list)**  **(** [int](class_int) shader_type  **)** const
  * void  **[scalar&#95;const&#95;node&#95;set&#95;value](#scalar_const_node_set_value)**  **(** [int](class_int) shader_type, [int](class_int) id, [float](class_float) value  **)**
  * void  **[scalar&#95;const&#95;node&#95;get&#95;value](#scalar_const_node_get_value)**  **(** [int](class_int) shader_type, [int](class_int) id, [float](class_float) arg2  **)**
  * void  **[vec&#95;const&#95;node&#95;set&#95;value](#vec_const_node_set_value)**  **(** [int](class_int) shader_type, [int](class_int) id, [Vector3](class_vector3) value  **)**
  * void  **[vec&#95;const&#95;node&#95;get&#95;value](#vec_const_node_get_value)**  **(** [int](class_int) shader_type, [int](class_int) id, [Vector3](class_vector3) arg2  **)**
  * void  **[rgb&#95;const&#95;node&#95;set&#95;value](#rgb_const_node_set_value)**  **(** [int](class_int) shader_type, [int](class_int) id, [Color](class_color) value  **)**
  * void  **[rgb&#95;const&#95;node&#95;get&#95;value](#rgb_const_node_get_value)**  **(** [int](class_int) shader_type, [int](class_int) id, [Color](class_color) arg2  **)**
  * void  **[xform&#95;const&#95;node&#95;set&#95;value](#xform_const_node_set_value)**  **(** [int](class_int) shader_type, [int](class_int) id, [Transform](class_transform) value  **)**
  * void  **[xform&#95;const&#95;node&#95;get&#95;value](#xform_const_node_get_value)**  **(** [int](class_int) shader_type, [int](class_int) id, [Transform](class_transform) arg2  **)**
  * void  **[texture&#95;node&#95;set&#95;filter&#95;size](#texture_node_set_filter_size)**  **(** [int](class_int) shader_type, [int](class_int) id, [int](class_int) filter_size  **)**
  * void  **[texture&#95;node&#95;get&#95;filter&#95;size](#texture_node_get_filter_size)**  **(** [int](class_int) shader_type, [int](class_int) id, [int](class_int) arg2  **)**
  * void  **[texture&#95;node&#95;set&#95;filter&#95;strength](#texture_node_set_filter_strength)**  **(** [int](class_int) shader_type, [float](class_float) id, [float](class_float) filter_strength  **)**
  * void  **[texture&#95;node&#95;get&#95;filter&#95;strength](#texture_node_get_filter_strength)**  **(** [int](class_int) shader_type, [float](class_float) id, [float](class_float) arg2  **)**
  * void  **[scalar&#95;op&#95;node&#95;set&#95;op](#scalar_op_node_set_op)**  **(** [int](class_int) shader_type, [float](class_float) id, [int](class_int) op  **)**
  * [int](class_int)  **[scalar&#95;op&#95;node&#95;get&#95;op](#scalar_op_node_get_op)**  **(** [int](class_int) shader_type, [float](class_float) id  **)** const
  * void  **[vec&#95;op&#95;node&#95;set&#95;op](#vec_op_node_set_op)**  **(** [int](class_int) shader_type, [float](class_float) id, [int](class_int) op  **)**
  * [int](class_int)  **[vec&#95;op&#95;node&#95;get&#95;op](#vec_op_node_get_op)**  **(** [int](class_int) shader_type, [float](class_float) id  **)** const
  * void  **[vec&#95;scalar&#95;op&#95;node&#95;set&#95;op](#vec_scalar_op_node_set_op)**  **(** [int](class_int) shader_type, [float](class_float) id, [int](class_int) op  **)**
  * [int](class_int)  **[vec&#95;scalar&#95;op&#95;node&#95;get&#95;op](#vec_scalar_op_node_get_op)**  **(** [int](class_int) shader_type, [float](class_float) id  **)** const
  * void  **[rgb&#95;op&#95;node&#95;set&#95;op](#rgb_op_node_set_op)**  **(** [int](class_int) shader_type, [float](class_float) id, [int](class_int) op  **)**
  * [int](class_int)  **[rgb&#95;op&#95;node&#95;get&#95;op](#rgb_op_node_get_op)**  **(** [int](class_int) shader_type, [float](class_float) id  **)** const
  * void  **[xform&#95;vec&#95;mult&#95;node&#95;set&#95;no&#95;translation](#xform_vec_mult_node_set_no_translation)**  **(** [int](class_int) shader_type, [int](class_int) id, [bool](class_bool) disable  **)**
  * [bool](class_bool)  **[xform&#95;vec&#95;mult&#95;node&#95;get&#95;no&#95;translation](#xform_vec_mult_node_get_no_translation)**  **(** [int](class_int) shader_type, [int](class_int) id  **)** const
  * void  **[scalar&#95;func&#95;node&#95;set&#95;function](#scalar_func_node_set_function)**  **(** [int](class_int) shader_type, [int](class_int) id, [int](class_int) func  **)**
  * [int](class_int)  **[scalar&#95;func&#95;node&#95;get&#95;function](#scalar_func_node_get_function)**  **(** [int](class_int) shader_type, [int](class_int) id  **)** const
  * void  **[vec&#95;func&#95;node&#95;set&#95;function](#vec_func_node_set_function)**  **(** [int](class_int) shader_type, [int](class_int) id, [int](class_int) func  **)**
  * [int](class_int)  **[vec&#95;func&#95;node&#95;get&#95;function](#vec_func_node_get_function)**  **(** [int](class_int) shader_type, [int](class_int) id  **)** const
  * void  **[input&#95;node&#95;set&#95;name](#input_node_set_name)**  **(** [int](class_int) shader_type, [int](class_int) id, [String](class_string) name  **)**
  * [String](class_string)  **[input&#95;node&#95;get&#95;name](#input_node_get_name)**  **(** [int](class_int) shader_type, [int](class_int) id  **)**
  * void  **[scalar&#95;input&#95;node&#95;set&#95;value](#scalar_input_node_set_value)**  **(** [int](class_int) shader_type, [int](class_int) id, [float](class_float) value  **)**
  * [float](class_float)  **[scalar&#95;input&#95;node&#95;get&#95;value](#scalar_input_node_get_value)**  **(** [int](class_int) shader_type, [int](class_int) id  **)** const
  * void  **[vec&#95;input&#95;node&#95;set&#95;value](#vec_input_node_set_value)**  **(** [int](class_int) shader_type, [int](class_int) id, [Vector3](class_vector3) value  **)**
  * [Vector3](class_vector3)  **[vec&#95;input&#95;node&#95;get&#95;value](#vec_input_node_get_value)**  **(** [int](class_int) shader_type, [int](class_int) id  **)** const
  * void  **[rgb&#95;input&#95;node&#95;set&#95;value](#rgb_input_node_set_value)**  **(** [int](class_int) shader_type, [int](class_int) id, [Color](class_color) value  **)**
  * [Color](class_color)  **[rgb&#95;input&#95;node&#95;get&#95;value](#rgb_input_node_get_value)**  **(** [int](class_int) shader_type, [int](class_int) id  **)** const
  * void  **[xform&#95;input&#95;node&#95;set&#95;value](#xform_input_node_set_value)**  **(** [int](class_int) shader_type, [int](class_int) id, [Transform](class_transform) value  **)**
  * [Transform](class_transform)  **[xform&#95;input&#95;node&#95;get&#95;value](#xform_input_node_get_value)**  **(** [int](class_int) shader_type, [int](class_int) id  **)** const
  * void  **[texture&#95;input&#95;node&#95;set&#95;value](#texture_input_node_set_value)**  **(** [int](class_int) shader_type, [int](class_int) id, [Texture](class_texture) value  **)**
  * [Texture](class_texture)  **[texture&#95;input&#95;node&#95;get&#95;value](#texture_input_node_get_value)**  **(** [int](class_int) shader_type, [int](class_int) id  **)** const
  * void  **[cubemap&#95;input&#95;node&#95;set&#95;value](#cubemap_input_node_set_value)**  **(** [int](class_int) shader_type, [int](class_int) id, [CubeMap](class_cubemap) value  **)**
  * [CubeMap](class_cubemap)  **[cubemap&#95;input&#95;node&#95;get&#95;value](#cubemap_input_node_get_value)**  **(** [int](class_int) shader_type, [int](class_int) id  **)** const
  * void  **[comment&#95;node&#95;set&#95;text](#comment_node_set_text)**  **(** [int](class_int) shader_type, [int](class_int) id, [String](class_string) text  **)**
  * [String](class_string)  **[comment&#95;node&#95;get&#95;text](#comment_node_get_text)**  **(** [int](class_int) shader_type, [int](class_int) id  **)** const
  * void  **[color&#95;ramp&#95;node&#95;set&#95;ramp](#color_ramp_node_set_ramp)**  **(** [int](class_int) shader_type, [int](class_int) id, [ColorArray](class_colorarray) colors, [RealArray](class_realarray) offsets  **)**
  * [ColorArray](class_colorarray)  **[color&#95;ramp&#95;node&#95;get&#95;colors](#color_ramp_node_get_colors)**  **(** [int](class_int) shader_type, [int](class_int) id  **)** const
  * [RealArray](class_realarray)  **[color&#95;ramp&#95;node&#95;get&#95;offsets](#color_ramp_node_get_offsets)**  **(** [int](class_int) shader_type, [int](class_int) id  **)** const
  * void  **[curve&#95;map&#95;node&#95;set&#95;points](#curve_map_node_set_points)**  **(** [int](class_int) shader_type, [int](class_int) id, [Vector2Array](class_vector2array) points  **)**
  * [Vector2Array](class_vector2array)  **[curve&#95;map&#95;node&#95;get&#95;points](#curve_map_node_get_points)**  **(** [int](class_int) shader_type, [int](class_int) id  **)** const
  * Error  **[connect&#95;node](#connect_node)**  **(** [int](class_int) shader_type, [int](class_int) src_id, [int](class_int) src_slot, [int](class_int) dst_id, [int](class_int) dst_slot  **)**
  * [bool](class_bool)  **[is&#95;node&#95;connected](#is_node_connected)**  **(** [int](class_int) shader_type, [int](class_int) src_id, [int](class_int) src_slot, [int](class_int) dst_id, [int](class_int) dst_slot  **)** const
  * void  **[disconnect&#95;node](#disconnect_node)**  **(** [int](class_int) shader_type, [int](class_int) src_id, [int](class_int) src_slot, [int](class_int) dst_id, [int](class_int) dst_slot  **)**
  * [Array](class_array)  **[get&#95;node&#95;connections](#get_node_connections)**  **(** [int](class_int) shader_type  **)** const
  * void  **[clear](#clear)**  **(** [int](class_int) shader_type  **)**
  * void  **[node&#95;set&#95;state](#node_set_state)**  **(** [int](class_int) shader_type, [int](class_int) id, var state  **)**
  * void  **[node&#95;get&#95;state](#node_get_state)**  **(** [int](class_int) shader_type, [int](class_int) id  **)** const

###  Signals  
  *  **updated**  **(** **)**

###  Numeric Constants  
  * **NODE_INPUT** = **0**
  * **NODE_SCALAR_CONST** = **1**
  * **NODE_VEC_CONST** = **2**
  * **NODE_RGB_CONST** = **3**
  * **NODE_XFORM_CONST** = **4**
  * **NODE_TIME** = **5**
  * **NODE_SCREEN_TEX** = **6**
  * **NODE_SCALAR_OP** = **7**
  * **NODE_VEC_OP** = **8**
  * **NODE_VEC_SCALAR_OP** = **9**
  * **NODE_RGB_OP** = **10**
  * **NODE_XFORM_MULT** = **11**
  * **NODE_XFORM_VEC_MULT** = **12**
  * **NODE_XFORM_VEC_INV_MULT** = **13**
  * **NODE_SCALAR_FUNC** = **14**
  * **NODE_VEC_FUNC** = **15**
  * **NODE_VEC_LEN** = **16**
  * **NODE_DOT_PROD** = **17**
  * **NODE_VEC_TO_SCALAR** = **18**
  * **NODE_SCALAR_TO_VEC** = **19**
  * **NODE_VEC_TO_XFORM** = **21**
  * **NODE_XFORM_TO_VEC** = **20**
  * **NODE_SCALAR_INTERP** = **22**
  * **NODE_VEC_INTERP** = **23**
  * **NODE_COLOR_RAMP** = **24**
  * **NODE_CURVE_MAP** = **25**
  * **NODE_SCALAR_INPUT** = **26**
  * **NODE_VEC_INPUT** = **27**
  * **NODE_RGB_INPUT** = **28**
  * **NODE_XFORM_INPUT** = **29**
  * **NODE_TEXTURE_INPUT** = **30**
  * **NODE_CUBEMAP_INPUT** = **31**
  * **NODE_DEFAULT_TEXTURE** = **32**
  * **NODE_OUTPUT** = **33**
  * **NODE_COMMENT** = **34**
  * **NODE_TYPE_MAX** = **35**
  * **SLOT_TYPE_SCALAR** = **0**
  * **SLOT_TYPE_VEC** = **1**
  * **SLOT_TYPE_XFORM** = **2**
  * **SLOT_TYPE_TEXTURE** = **3**
  * **SLOT_MAX** = **4**
  * **SHADER_TYPE_VERTEX** = **0**
  * **SHADER_TYPE_FRAGMENT** = **1**
  * **SHADER_TYPE_LIGHT** = **2**
  * **SHADER_TYPE_MAX** = **3**
  * **SLOT_IN** = **0**
  * **SLOT_OUT** = **1**
  * **GRAPH_OK** = **0**
  * **GRAPH_ERROR_CYCLIC** = **1**
  * **GRAPH_ERROR_MISSING_CONNECTIONS** = **2**
  * **SCALAR_OP_ADD** = **0**
  * **SCALAR_OP_SUB** = **1**
  * **SCALAR_OP_MUL** = **2**
  * **SCALAR_OP_DIV** = **3**
  * **SCALAR_OP_MOD** = **4**
  * **SCALAR_OP_POW** = **5**
  * **SCALAR_OP_MAX** = **6**
  * **SCALAR_OP_MIN** = **7**
  * **SCALAR_OP_ATAN2** = **8**
  * **SCALAR_MAX_OP** = **9**
  * **VEC_OP_ADD** = **0**
  * **VEC_OP_SUB** = **1**
  * **VEC_OP_MUL** = **2**
  * **VEC_OP_DIV** = **3**
  * **VEC_OP_MOD** = **4**
  * **VEC_OP_POW** = **5**
  * **VEC_OP_MAX** = **6**
  * **VEC_OP_MIN** = **7**
  * **VEC_OP_CROSS** = **8**
  * **VEC_MAX_OP** = **9**
  * **VEC_SCALAR_OP_MUL** = **0**
  * **VEC_SCALAR_OP_DIV** = **1**
  * **VEC_SCALAR_OP_POW** = **2**
  * **VEC_SCALAR_MAX_OP** = **3**
  * **RGB_OP_SCREEN** = **0**
  * **RGB_OP_DIFFERENCE** = **1**
  * **RGB_OP_DARKEN** = **2**
  * **RGB_OP_LIGHTEN** = **3**
  * **RGB_OP_OVERLAY** = **4**
  * **RGB_OP_DODGE** = **5**
  * **RGB_OP_BURN** = **6**
  * **RGB_OP_SOFT_LIGHT** = **7**
  * **RGB_OP_HARD_LIGHT** = **8**
  * **RGB_MAX_OP** = **9**
  * **SCALAR_FUNC_SIN** = **0**
  * **SCALAR_FUNC_COS** = **1**
  * **SCALAR_FUNC_TAN** = **2**
  * **SCALAR_FUNC_ASIN** = **3**
  * **SCALAR_FUNC_ACOS** = **4**
  * **SCALAR_FUNC_ATAN** = **5**
  * **SCALAR_FUNC_SINH** = **6**
  * **SCALAR_FUNC_COSH** = **7**
  * **SCALAR_FUNC_TANH** = **8**
  * **SCALAR_FUNC_LOG** = **9**
  * **SCALAR_FUNC_EXP** = **10**
  * **SCALAR_FUNC_SQRT** = **11**
  * **SCALAR_FUNC_ABS** = **12**
  * **SCALAR_FUNC_SIGN** = **13**
  * **SCALAR_FUNC_FLOOR** = **14**
  * **SCALAR_FUNC_ROUND** = **15**
  * **SCALAR_FUNC_CEIL** = **16**
  * **SCALAR_FUNC_FRAC** = **17**
  * **SCALAR_FUNC_SATURATE** = **18**
  * **SCALAR_FUNC_NEGATE** = **19**
  * **SCALAR_MAX_FUNC** = **20**
  * **VEC_FUNC_NORMALIZE** = **0**
  * **VEC_FUNC_SATURATE** = **1**
  * **VEC_FUNC_NEGATE** = **2**
  * **VEC_FUNC_RECIPROCAL** = **3**
  * **VEC_FUNC_RGB2HSV** = **4**
  * **VEC_FUNC_HSV2RGB** = **5**
  * **VEC_MAX_FUNC** = **6**

###  Member Function Description  
