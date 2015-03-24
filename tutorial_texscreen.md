# Screen Reading Shaders

### Introduction

Very often it is desired to make a shader that reads from the same screen it's writing to. 3D APIs such as OpenGL or DirectX make this very difficult because of internal hardware limitations. GPUs are extremely parallel, so reading and writing causes all sort of cache and coherency problems. As a result, not even the most modern hardware supports this properly.

The workaround is to make a copy of the screen, or a part of the screen, to a back-buffer and then read from it while drawing. Godot provides a few tools that makes this process easy!

### TexScreen shader instruction.

Godot shading language has a special instruction, "texscreen", it takes as parameter the UV of the screen and returns a vec3 RGB with the color. A special built-in varying: SCREEN_UV can be used to obtain the UV for the current fragment. As a result, this simple 2D fragment shader:

```glsl
COLOR=vec4( texscreen(SCREEN_UV), 1.0 );
```

results in an invisible object, because it just shows what lies behind. The same shader using the visual editor looks like this:

<p align="center"><img src="images/texscreen_visual.png"></p>

### TexScreen Example

Texscreen instruction can be used for a lot of things. There is a special demo for _Screen Space Shaders_, that you can download to see and learn. One example is a simple shader to adjust brightness, contrast and saturation:

```glsl
uniform float brightness=1.0; 
uniform float contrast=1.0;
uniform float saturation=1.0;

vec3 c = texscreen(SCREEN_UV);

c.rgb = mix(vec3(0.0),c.rgb,brightness);
c.rgb = mix(vec3(0.5),c.rgb,contrast);
c.rgb = mix(vec3(dot(vec3(1.0),c.rgb)*0.33333),c.rgb,saturation);

COLOR.rgb=c;

```

### Behind The Scenes


