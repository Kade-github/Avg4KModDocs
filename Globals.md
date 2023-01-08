## config
| Property | Type | Description |
| --- | --- |----------- |
| downscroll | boolean | The donwscroll setting |
| noteSize | float | The noteSize setting |
| playField | string | The name of the playfield sprite (**deprecated**/**obsolete**) |
| displayWidth | int | The current games width |
| displayHeight | int | The current games height |
| scrollSpeed | int | The scrollspeed setting |

This is a lua class that can be accessed from anywhere in the code.

Example:
```lua
function create()
    local scrollspeed = config.scrollSpeed
    local downscroll = config.downscroll
    local notesize = config.noteSize
end
```