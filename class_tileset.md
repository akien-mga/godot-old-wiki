#  TileSet  
####**Inherits:** [Resource](class_resource)
####**Category:** Core

###  Brief Description  
Tile library for tilemaps.

###  Member Functions 
  * void  **[create&#95;tile](#create_tile)**  **(** [int](class_int) id  **)**
  * void  **[tile&#95;set&#95;name](#tile_set_name)**  **(** [int](class_int) id, [String](class_string) name  **)**
  * [String](class_string)  **[tile&#95;get&#95;name](#tile_get_name)**  **(** [int](class_int) id  **)** const
  * void  **[tile&#95;set&#95;texture](#tile_set_texture)**  **(** [int](class_int) id, [Texture](class_texture) texture  **)**
  * [Texture](class_texture)  **[tile&#95;get&#95;texture](#tile_get_texture)**  **(** [int](class_int) id  **)** const
  * void  **[tile&#95;set&#95;material](#tile_set_material)**  **(** [int](class_int) id, [CanvasItemMaterial](class_canvasitemmaterial) material  **)**
  * [CanvasItemMaterial](class_canvasitemmaterial)  **[tile&#95;get&#95;material](#tile_get_material)**  **(** [int](class_int) id  **)** const
  * void  **[tile&#95;set&#95;texture&#95;offset](#tile_set_texture_offset)**  **(** [int](class_int) id, [Vector2](class_vector2) texture_offset  **)**
  * [Vector2](class_vector2)  **[tile&#95;get&#95;texture&#95;offset](#tile_get_texture_offset)**  **(** [int](class_int) id  **)** const
  * void  **[tile&#95;set&#95;shape&#95;offset](#tile_set_shape_offset)**  **(** [int](class_int) id, [Vector2](class_vector2) shape_offset  **)**
  * [Vector2](class_vector2)  **[tile&#95;get&#95;shape&#95;offset](#tile_get_shape_offset)**  **(** [int](class_int) id  **)** const
  * void  **[tile&#95;set&#95;region](#tile_set_region)**  **(** [int](class_int) id, [Rect2](class_rect2) region  **)**
  * [Rect2](class_rect2)  **[tile&#95;get&#95;region](#tile_get_region)**  **(** [int](class_int) id  **)** const
  * void  **[tile&#95;set&#95;shape](#tile_set_shape)**  **(** [int](class_int) id, [Shape2D](class_shape2d) shape  **)**
  * [Shape2D](class_shape2d)  **[tile&#95;get&#95;shape](#tile_get_shape)**  **(** [int](class_int) id  **)** const
  * void  **[tile&#95;set&#95;shapes](#tile_set_shapes)**  **(** [int](class_int) id, [Array](class_array) shapes  **)**
  * [Array](class_array)  **[tile&#95;get&#95;shapes](#tile_get_shapes)**  **(** [int](class_int) id  **)** const
  * void  **[tile&#95;set&#95;navigation&#95;polygon](#tile_set_navigation_polygon)**  **(** [int](class_int) id, [NavigationPolygon](class_navigationpolygon) navigation_polygon  **)**
  * [NavigationPolygon](class_navigationpolygon)  **[tile&#95;get&#95;navigation&#95;polygon](#tile_get_navigation_polygon)**  **(** [int](class_int) id  **)** const
  * void  **[tile&#95;set&#95;navigation&#95;polygon&#95;offset](#tile_set_navigation_polygon_offset)**  **(** [int](class_int) id, [Vector2](class_vector2) navigation_polygon_offset  **)**
  * [Vector2](class_vector2)  **[tile&#95;get&#95;navigation&#95;polygon&#95;offset](#tile_get_navigation_polygon_offset)**  **(** [int](class_int) id  **)** const
  * void  **[tile&#95;set&#95;light&#95;occluder](#tile_set_light_occluder)**  **(** [int](class_int) id, [OccluderPolygon2D](class_occluderpolygon2d) light_occluder  **)**
  * [OccluderPolygon2D](class_occluderpolygon2d)  **[tile&#95;get&#95;light&#95;occluder](#tile_get_light_occluder)**  **(** [int](class_int) id  **)** const
  * void  **[tile&#95;set&#95;occluder&#95;offset](#tile_set_occluder_offset)**  **(** [int](class_int) id, [Vector2](class_vector2) occluder_offset  **)**
  * [Vector2](class_vector2)  **[tile&#95;get&#95;occluder&#95;offset](#tile_get_occluder_offset)**  **(** [int](class_int) id  **)** const
  * void  **[remove&#95;tile](#remove_tile)**  **(** [int](class_int) id  **)**
  * void  **[clear](#clear)**  **(** **)**
  * [int](class_int)  **[get&#95;last&#95;unused&#95;tile&#95;id](#get_last_unused_tile_id)**  **(** **)** const
  * [int](class_int)  **[find&#95;tile&#95;by&#95;name](#find_tile_by_name)**  **(** [String](class_string) name  **)** const
  * [Array](class_array)  **[get&#95;tiles&#95;ids](#get_tiles_ids)**  **(** **)** const

###  Description  
A TileSet is a library of tiles for a [TileMap](class_tilemap). It contains a list of tiles, each consisting of a sprite and optional collision shapes.

###  Member Function Description  

#### <a name="create_tile">create_tile</a>
  * void  **create&#95;tile**  **(** [int](class_int) id  **)**

Create a new tile, the ID must be specified.

#### <a name="tile_set_name">tile_set_name</a>
  * void  **tile&#95;set&#95;name**  **(** [int](class_int) id, [String](class_string) name  **)**

Set the name of a tile, for decriptive purposes.

#### <a name="tile_get_name">tile_get_name</a>
  * [String](class_string)  **tile&#95;get&#95;name**  **(** [int](class_int) id  **)** const

Return the name of a tile, for decriptive purposes.

#### <a name="tile_set_texture">tile_set_texture</a>
  * void  **tile&#95;set&#95;texture**  **(** [int](class_int) id, [Texture](class_texture) texture  **)**

Set the texture of the tile.

#### <a name="tile_get_texture">tile_get_texture</a>
  * [Texture](class_texture)  **tile&#95;get&#95;texture**  **(** [int](class_int) id  **)** const

Return the texture of the tile.

#### <a name="tile_set_region">tile_set_region</a>
  * void  **tile&#95;set&#95;region**  **(** [int](class_int) id, [Rect2](class_rect2) region  **)**

Set the tile sub-region in the texture. This is common in texture atlases.

#### <a name="tile_get_region">tile_get_region</a>
  * [Rect2](class_rect2)  **tile&#95;get&#95;region**  **(** [int](class_int) id  **)** const

Return the tile sub-region in the texture. This is common in texture atlases.

#### <a name="tile_set_shape">tile_set_shape</a>
  * void  **tile&#95;set&#95;shape**  **(** [int](class_int) id, [Shape2D](class_shape2d) shape  **)**

Set a shape for the tile, enabling physics to collide it.

#### <a name="tile_get_shape">tile_get_shape</a>
  * [Shape2D](class_shape2d)  **tile&#95;get&#95;shape**  **(** [int](class_int) id  **)** const

Return the shape of the tile.

#### <a name="remove_tile">remove_tile</a>
  * void  **remove&#95;tile**  **(** [int](class_int) id  **)**

Remove a tile, by integer id.

#### <a name="clear">clear</a>
  * void  **clear**  **(** **)**

Clear all tiles.

#### <a name="get_last_unused_tile_id">get_last_unused_tile_id</a>
  * [int](class_int)  **get&#95;last&#95;unused&#95;tile&#95;id**  **(** **)** const

Find an empty id for creating a new tile.

#### <a name="find_tile_by_name">find_tile_by_name</a>
  * [int](class_int)  **find&#95;tile&#95;by&#95;name**  **(** [String](class_string) name  **)** const

Find the first tile with the given name.
