# Binary Serialization Format

### Introduction

Godot has a simple serialization API based on Variant. It's used for converting data types to an array of bytes efficiently. This API is used in the functions [File.get_var](class_file#get_var), [File.store_var](class_file#store_var) as well as the packet APIs for [PacketPeer](class_packetpeer). This format is not used for binary scenes and resources.

### Packet Specification

The packet is designed to be always padded to 4 bytes. All values are little endian encoded. 
All packets have a 4 byte header representing an integer, specifying the type of data:

Type | Value
---|---
0 | null
1 | bool
2 | integer
3 | float
4 | string
5 | vector2
6 | rect2
7 | vector3
8 | matrix32
9 | plane
10| quaternion
11| aabb (rect3)
12| matrix3x3
13| transform (matrix 4x3)
14| color
15| image
16| node path
17| rid (unsupported)
18| object (unsupported)
19| input event
20| dictionary
21| array 
22| byte array
23| int array
24| float array
25| string array
26| vector2 array
27| vector3 array
28| color array

Following this is the actual packet contents, which varies for each type of packet:

### 0: null
### 1: bool

Offset | Len | Type | Description
---|---|---|---
4|4|Integer| 0 for False, 1 for True

### 2: integer

Offset | Len | Type | Description
---|---|---|---
4|4|Integer| Signed, 32-Bit Integer

### 3: float

Offset | Len | Type | Description
---|---|---|---
4|4|Float| IEE 754 32-Bits Float

### 4: string

Offset | Len | Type | Description
---|---|---|---
4|4|Integer| String Length (in Bytes)
8|X|Bytes| UTF-8 Encoded String

### 5: vector2

Offset | Len | Type | Description
---|---|---|---
4|4|Float| X Coordinate
8|4|Float| Y Coordinate

### 6: rect2

Offset | Len | Type | Description
---|---|---|---
4|4|Float| X Coordinate
8|4|Float| Y Coordinate
12|4|Float| X Size
16|4|Float| Y Size


### 7: vector3

Offset | Len | Type | Description
---|---|---|---
4|4|Float| X Coordinate
8|4|Float| Y Coordinate
12|4|Float| Z Coordinate

### 8: matrix32
### 9: plane
### 10: quaternion
### 11: aabb (rect3)
### 12: matrix3x3
### 13: transform (matrix 4x3)
### 14: color
### 15: image
### 16: node path
### 17: rid (unsupported)
### 18: object (unsupported)
### 19: input event
### 20: dictionary
### 21: array 
### 22: byte array
### 23: int array
### 24: float array
### 25: string array
### 26: vector2 array
### 27: vector3 array
### 28: color array



