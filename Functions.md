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

## setSpriteProperty

| Argument | Type | Description |
| --- | --- |----------- |
| sprite | string | The name of the sprite |
| property | string | The property to set |
| value | string | The value to set the property to |

### Properties

| Property | Description |
| --- |----------- |
| sparrow | A path to load a sparrow atlas (relative to mod directory, without extension) |
| loop | True or False to loop the sparrow animation |
| fps | The FPS to run the sparrow animation at |
| rageMin | The minimum frame to play |
| rageMax | The maximum frame to play |
| anim | The current sparrow animation to play |
| animFinish | A function's name to call when the sprite has finished its sparrow animation |
| anchor | A sprite's name to anchor to (meaning the current sprite gets anchored to the specified sprite) |

This function returns nothing.

Sparrow File loading example:

```lua
-- Loading a FNF spritesheet (yeah I know fnf crazy but its a good tutorial okay)
createSprite("BOYFRIEND", "bf",0,0)
setSpriteProperty("bf", "sparrow", "BOYFRIEND")
setSpriteProperty("bf", "loop", "true") -- it loops!
setSpriteProperty("bf", "fps", "24")
setSpriteProperty("bf", "animFinish", "finishBF") -- this doesn't get called on a loops end

setSpriteProperty("bf", "anim", "BF idle dance") -- this plays the idle!!

-- The current file structure looks like this:
-- └──  mod
--      ├── BOYFRIEND.png
--      ├── BOYFRIEND.xml
--      └── mod.lua
```

## createShader

| Argument | Type | Description |
| --- | --- |----------- |
| shader | string | The name of the shader |
| vertPath | string | The vert path of the shader (relative to the mod directory, without the extension) |
| fragPath | string | The frag path of the shader (relative to the mod directory, without the extension) |

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

## setNoteskin

| Argument | Type | Description |
| --- | --- |----------- |
| noteskin | string | The name of the noteskin folder in the mod directory (the folder should be something you can put into avg4k's noteskin folder) |

This function returns nothing.

Example:

```lua
-- Set the noteskin to "noteskin"
setNoteskin("noteskin")
```

## dom

Standing for "do-mod", it's a simple "do this function at this beat"

| Argument | Type | Description |
| --- | --- |----------- |
| function | luaFunction | The function to call |
| beat | float | The beat to call the function at |

This function returns nothing.

Example:

```lua
-- print "Hello World" at the 1st beat
function create()
    dom(function()
            consolePrint("Hello World!")
        end
        , 1)
end
```

## setModProperty

This function will set a mod's property without tweens or a time attached.

| Argument | Type | Description |
| --- | --- |----------- |
| mod | string | The mod to set |
| pid | int | The playfield the mod is on |
| column | int | The column the mod is on (if applicable, otherwise set to -1) |
| amount | float | The mod's main value |

This function returns nothing.

Example:

```lua
-- Instantly set "amovex" to -250
function create()
    setModProperty('amovex', 0, -1, -250)
end
```

## getModProperty

This function will get a mod's value.

| Argument | Type | Description |
| --- | --- |----------- |
| mod | string | The mod to set |
| pid | int | The playfield the mod is on |
| column | int | The column the mod is on (if applicable, otherwise set to -1) |

| Return | Type | Description |
| --- | --- |----------- |
| amount | float | The current value of the mod |

Example:

```lua
-- Instantly set "amovex" to -250 and print out the value
function create()
    setModProperty('amovex', 0, -1, -250)
    consolePrint(tostring(getModProperty('amovex',0,-1)))
end
```

## setSpriteMod

This function will set a sprites mod's property without tweens or a time attached.

| Argument | Type | Description |
| --- | --- |----------- |
| sprite | string | The sprite to set |
| mod | string | The mod to set |
| amount | float | The mod's main value |

This function returns nothing.

Example:

```lua
-- Instantly set "movex" to -250
function create()
    setSpriteMod('car', 'movex', -250)
end
```

## getSpriteMod

This function will get a sprites mod's property.

| Argument | Type | Description |
| --- | --- |----------- |
| sprite | string | The sprite to set |
| mod | string | The mod to set |

| Return | Type | Description |
| --- | --- |----------- |
| amount | float | The current value of the mod |

Example:

```lua
-- Instantly set "movex" to -250, and print the value to the console
function create()
    setSpriteMod('car', 'movex', -250)
    consolePrint(tostring(getSpriteMod('car', 'movex')))
end
```

## setAutoEnd

This function tells the game if it should the song prematurely, or once the song is finished.

Setting this to **"true"** will not end the song until it is set to **false**.

| Argument | Type | Description |
| --- | --- |----------- |
| autoEnd | bool | If the game should auto end the song or not |

This function returns nothing.

Example:

```lua
-- Stop the chart from ending
function create()
    setAutoEnd(true)
end
```

## formCompletePath

A very simple helper function that simply combines a relative path and creates an absolute one.

| Argument | Type | Description |
| --- | --- |----------- |
| path | string | A relative path in the mod/ folder |

| Return | Type | Description |
| --- | --- |----------- |
| absolute path | string | An absolute version of that path |

## tween

A simple tween function

| Argument | Type | Description |
| --- | --- |----------- |
| a | float | The start point |
| b | float | The end point |
| t | float | The time along the point |
| tween | string | The easing to use, list located [here](Easing.md) |

| Return | Type | Description |
| --- | --- |----------- |
| value | float | The return value of lerp |