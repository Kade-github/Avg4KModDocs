## Shader Structure/API

Average4K uses OpenGL GLSL to display shaders.

Average4K Shader Header (add in during runtime to every shader, so you can call these in your shader code if you want):
```glsl
// Avg4K Header
uniform float iTime; // Current time in the song (ms)
uniform float iBpm; // Current bpm in the song
uniform float iBeat; // Current beat in the song
```

Please use these templates.

Template Vert Shader:

```glsl
in vec2 v_position;
in vec2 v_uv;
in vec4 v_colour;
out vec2 f_uv;
out vec4 f_colour;
uniform mat4 u_projection;

void main()
{
	f_uv = v_uv;
	f_colour = v_colour;
	gl_Position = u_projection * vec4(v_position.xy, 0.0, 1.0);
}
```

Template Frag Shader:

```glsl
uniform sampler2D u_texture;
in vec2 f_uv;
in vec4 f_colour;

out vec4 o_colour;
void main()
{
	o_colour = texture(u_texture, f_uv) * f_colour;
	if (o_colour.a == 0.0)
		discard;	
}
```

As you can also see, Average4K has some custom uniforms to help you out.

| Uniform | Type | Description |
| --- | --- |----------- |
| iTime | float | The total time the program has been open (in ms) |
| iBpm | float | The current BPM of the song |
| iBeat | float | The current beat of the song |

## Special Thanks

All of this couldn't be possible without the wonderful [CuckyDev](https://twitter.com/cuckydev)

He basically taught me OpenGL, and he is in general a really nice and talented guy!

(also these shaders are his lol)