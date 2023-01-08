## consolePrint

| Argument | Type | Description |
| --- | --- |----------- |
| text | string | The text to be printed |

This function returns nothing.

Example:

```lua
consolePrint("Hello world!")
```

## setScrollSpeed

| Argument | Type | Description |
| --- | --- |----------- |
| cmod | int |The cmod speed to set the current scrollspeed too |

This function returns nothing.

Example:

```lua
setScrollSpeed(600)
```

## setNoteSize

| Argument | Type | Description |
| --- | --- |----------- |
| size | float |The size to set the current notesize to |

This function returns nothing.

Example:

```lua
setNoteSize(1.25)
```

## createPlayfield

This function has no arguments.

| Returns | Type | Description |
| --- | --- |----------- |
| pid | int | The created playfield's id |

Example:

```lua
local pid = createPlayfield()
```

Note: Currently there is no "deletePlayfield" so please create only the amount of playfields you need.

## setPlayfield

| Argument | Type | Description |
| --- | --- |----------- |
| pid | int | The playfield id to set the current playfield id to |

This function returns nothing.

Example:

```lua
local pid = createPlayfield()
setPlayfield(pid)

-- 0 is the default initial playfield id
setPlayfield(0)
```

## activateMod

| Argument | Type | Description |
| --- | --- |----------- |
| name | string | The name of the mod |
| tweenStart | float | The beat of when to start the tween |
| tweenLen | float | The length in beats of the tween |
| easingFunc | string | The name of the tween, the the list of tweens can be found [here](Easing.md) |
| amount | float | The value to put the mod to |

This function returns nothing.

Example:

```lua
-- Set drunk to 100% (1) on the start of the song, over the span of 1 beat
activateMod("drunk", 0, 1, "inoutback", 1)
```

## activateModMap


| Argument | Type | Description |
| --- | --- |----------- |
| name | string | The name of the mod |
| tweenStart | float | The beat of when to start the tween |
| tweenLen | float | The length in beats of the tween |
| easingFunc | string | The name of the tween, the the list of tweens can be found [here](Easing.md) |
| amount | float | The value to put the mod to |
| column | int | The column to apply the mod to (0->3) |

This function returns nothing.

Example:

```lua
-- Set drunk to 100% (1) in the first column. On the start of the song, over the span of 1 beat
activateModMap("drunk", 0, 1, "inoutback", 1, 0)
```

## createSprite


| Argument | Type | Description |
| --- | --- |----------- |
| path | string | The path (relative to the mod directory, without the extension) |
| name | string | The name of the sprite |
| x | int | The initial point of the sprite on the x axis |
| y | int | The initial point of the sprite on the y axis |

This function returns nothing.

Example:

```lua
-- Create the "car" sprite with the same path at 0,0.
createSprite("car", "car", 0, 0)
```

## activateSpriteMod

| Argument | Type | Description |
| --- | --- |----------- |
| sprite | string | The name of the sprite |
| name | string | The name of the mod |
| tweenStart | float | The beat of when to start the tween |
| tweenLen | float | The length in beats of the tween |
| easingFunc | string | The name of the tween, the the list of tweens can be found [here](Easing.md) |

This function returns nothing.

Note: The mods that sprites can use are pretty much all [built-in](Mods.md) mods except for obvious ones like wave, drunk, and tipsy.

Example:

```lua
-- Move the "car" sprite to the right by 500 pixels on the start of the song, over the span of 1 beat.
activateSpriteMod("car", "movex", 0, 1, "inoutback", 500)
```

## getSpriteWidth

| Argument | Type | Description |
| --- | --- |----------- |
| sprite | string | The name of the sprite |

| Returns | Type | Description |
| --- | --- |----------- |
| width | int | The width of the sprite |

Example:

```lua
-- Get the width of the sprite called "car"
local width = getSpriteWidth("car")
```

## getSpriteHeight

| Argument | Type | Description |
| --- | --- |----------- |
| sprite | string | The name of the sprite |

| Returns | Type | Description |
| --- | --- |----------- |
| height | int | The height of the sprite |

Example:

```lua
-- Get the height of the sprite called "car"
local height = getSpriteHeight("car")
```

## setSpriteOffset

| Argument | Type | Description |
| --- | --- |----------- |
| sprite | string | The name of the sprite |
| xOffset | int | The x offset |
| yOffset | int | The y offset |

This function returns nothing.

Example:

```lua
-- Set the sprite offset of "car" to 100,100
setSpriteOffset("car", 100, 100)
```

## createShader

| Argument | Type | Description |
| --- | --- |----------- |
| shader | string | The name of the shader |
| vertPath | string | The vert path of the shader (relative to the mod directory) |
| fragPath | string | The frag path of the shader (relative to the mod directory) |

This function returns nothing.

Example:

```lua
-- Loads a shader by the name of "blur"
createShader("blur", "blurVert", "blurFrag")
```

## applyShader

| Argument | Type | Description |
| --- | --- |----------- |
| shader | string | The name of the shader |
| sprite | string | The name of the sprite |

This function returns nothing.

Example:

```lua
-- Applys "blur" to the sprite "car"
applyShader("blur", "car")
```
