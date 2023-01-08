## create

There are no arguments in this event.

The first function that gets called when the game loads the modfile.

Example:

```lua
--[[
    On create, print "Hello World" to the console (F11)
]]--
function create()
    consolePrint("Hello World")
end
```

## update

| Argument | Type | Description |
| --- | --- |----------- |
| beat | float | The current beat of the song |

A function that gets called every so often, **not every frame**; But pretty close.


Example:

```lua
--[[
    On update, do nothing.
]]--
function update(beat)
    -- get it? its doing nothing
end
```

## hit

| Argument | Type | Description |
| --- | --- |----------- |
| lane | int | The lane of the hit note |

A function that gets called whenever the play successfully hits a note.


Example:

```lua
--[[
    When a note is hit, print "You hit a note! {lane}" in the console
]]--
function hit(lane)
    consolePrint("You hit a note! " .. tostring(lane))
end
```

## key_pressed

| Argument | Type | Description |
| --- | --- |----------- |
| key | int | The key code of the key pressed |

A function for when a key is pressed.

[Link](https://wiki.libsdl.org/SDL2/SDLKeycodeLookup) to a page with the keycodes.

Example:

```lua
--[[
    When space is pressed, print "Space" in the console
]]--
function key_pressed(key)
    if key == 32 then
        consolePrint("Space")
    end
end
```

## key_released

| Argument | Type | Description |
| --- | --- |----------- |
| key | int | The key code of the key released |

A function for when a key is released.

[Link](https://wiki.libsdl.org/SDL2/SDLKeycodeLookup) to a page with the keycodes.

Example:

```lua
--[[
    When space is released, print "Released space" in the console
]]--
function key_released(key)
    if key == 32 then
        consolePrint("Released space")
    end
end
```