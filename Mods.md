## Information
Following in [NotITG](https://www.noti.tg/)'s footsteps, Average4K has developed some built in mods which are normally used to create other mods.

The rest of this page will be dedicated to documenting those built in mods.

Note: all videos on this page are from [this video](https://www.youtube.com/watch?v=5EfC9jMnxh0&feature=youtu.be). Which is why there is music in these videos.

## amovex/movex
Standing for "all move x position", this moves the current selected playfield in the x axis.

Example:
```lua
-- Moves the playfield 350 pixels to the right, on the 4th beat. Over a span of 2 beats in the "outCubic" lerp
activateMod("amovex", 4, 2, "outCubic", 350)
```

Column Variant Example:
```lua
-- Moves column 1 of the playfield 350 pixels to the right, on the 4th beat. Over a span of 2 beats in the "outCubic" lerp
activateModMap("movex", 4, 2, "outCubic", 350, 0) -- reminder that 0 is 1 since the column numbers are 0 index based. 0, 1, 2, 3 for the 4 column numbers.
```

[amovex](_media/amovex.mp4 ':include :type=video controls width=35% muted=true autoplay=true loop=true')

## amovey/movey

Standing for "all move y position", this moves the current selected playfield in the y axis.

Example:
```lua
-- Moves the playfield 350 pixels down, on the 4th beat. Over a span of 2 beats in the "outCubic" lerp
activateMod("amovey", 4, 2, "outCubic", 350)
```

Column Variant Example:
```lua
-- Moves column 1 of the playfield 350 pixels down, on the 4th beat. Over a span of 2 beats in the "outCubic" lerp
activateModMap("movey", 4, 2, "outCubic", 350, 0) -- reminder that 0 is 1 since the column numbers are 0 index based. 0, 1, 2, 3 for the 4 column numbers.
```

[amovex](_media/amovey.mp4 ':include :type=video controls width=35% muted=true autoplay=true loop=true')

## drunk/drunkCol

Drunk affects the x axis of the arrows in a drunkish type of way. I dunno what else to say

Example:
```lua
-- Smoothly interperlates drunk to 100% (1) on the 4th beat, over a span of 2 beats.
activateMod("drunk", 4, 2, "outCubic", 1)
```

Column Variant Example:
```lua
-- Smoothly interperlates drunk to 100% (1) on column one. On the 4th beat, over a span of 2 beats.
activateModMap("drunkCol", 4, 2, "outCubic", 1, 0) -- reminder that 0 is 1 since the column numbers are 0 index based. 0, 1, 2, 3 for the 4 column numbers.
```

[drunk](_media/drunk.mp4 ':include :type=video controls width=35% muted=true autoplay=true loop=true')

## tipsy/tipsyCol

Tipsy affects the y axis of the arrows in a tipsyish type of way. I dunno what else to say

Example:
```lua
-- Smoothly interperlates tipsy to 100% (1) on the 4th beat, over a span of 2 beats.
activateMod("tipsy", 4, 2, "outCubic", 1)
```

Column Variant Example:
```lua
-- Smoothly interperlates tipsy to 100% (1) on column one. On the 4th beat, over a span of 2 beats.
activateModMap("tipsyCol", 4, 2, "outCubic", 1, 0) -- reminder that 0 is 1 since the column numbers are 0 index based. 0, 1, 2, 3 for the 4 column numbers.
```

[tipsy](_media/tipsy.mp4 ':include :type=video controls width=35% muted=true autoplay=true loop=true')

## wave/waveCol

Wave distorts the y axis like an ocean wave.

Note: Looks better on slower scrollspeeds (around 400-500)

Example:
```lua
-- Smoothly interperlates wave to 100% (1) on the 4th beat, over a span of 2 beats.
activateMod("wave", 4, 2, "outCubic", 1)
```

Column Variant Example:
```lua
-- Smoothly interperlates wave to 100% (1) on column one. On the 4th beat, over a span of 2 beats.
activateModMap("waveCol", 4, 2, "outCubic", 1, 0) -- reminder that 0 is 1 since the column numbers are 0 index based. 0, 1, 2, 3 for the 4 column numbers.
```

[wave](_media/wave.mp4 ':include :type=video controls width=35% muted=true autoplay=true loop=true')

## aconfusion/confusion

Standing for "all confusion", this rotates notes and receptors.

Example:
```lua
-- Smoothly interperlates confusion to 180 degrees (1) on the 4th beat, over a span of 2 beats.
activateMod("aconfusion", 4, 2, "outCubic", 180)
```

Column Variant Example:
```lua
-- Smoothly interperlates aconfusion to 180 degrees (1) on column one. On the 4th beat, over a span of 2 beats.
activateModMap("aconfusion", 4, 2, "outCubic", 180, 0) -- reminder that 0 is 1 since the column numbers are 0 index based. 0, 1, 2, 3 for the 4 column numbers.
```

[wave](_media/confusion.mp4 ':include :type=video controls width=35% muted=true autoplay=true loop=true')

## reverse

Reverse the scrollspeed and flip the receptors.

Example:
```lua
-- Smoothly interperlates reverse to 100% in the first column (1) on the 4th beat, over a span of 2 beats.
activateModMap("reverse", 4, 2, "outCubic", 1, 0)
```

[reverse](_media/reverse.mp4 ':include :type=video controls width=35% muted=true autoplay=true loop=true')

## dizzy/dizzyCol

Rotate the notes and receptors based on the current beat.

Example:
```lua
-- Smoothly interperlates dizzy to 100% (1) on the 4th beat, over a span of 2 beats.
activateMod("dizzy", 4, 2, "outCubic", 1, 0)
```

Column Variant Example:
```lua
-- Smoothly interperlates dizzy to 100% (1) in the first column on the 4th beat, over a span of 2 beats.
activateMod("dizzyCol", 4, 2, "outCubic", 1, 0)
```

[dizzy](_media/dizzy.mp4 ':include :type=video controls width=35% muted=true autoplay=true loop=true')

## mini/miniCol

Sizes up and down the current playfield (.5 = default, 1 = 50% size, 0 = 150% size)

Example:
```lua
-- Smoothly interperlates mini to 100% (1) on the 4th beat, over a span of 2 beats.
activateMod("mini", 4, 2, "outCubic", 1, 0)
```

Column Variant Example:
```lua
-- Smoothly interperlates mini to 100% (1) in the first column on the 4th beat, over a span of 2 beats.
activateMod("miniCol", 4, 2, "outCubic", 1, 0)
```
(the video says 0 = double, its lying)

[mini](_media/mini.mp4 ':include :type=video controls width=35% muted=true autoplay=true loop=true')

## stealthWhite

Changes the colors of the notes and receptors to white

Column Variant Example:
```lua
-- Smoothly interperlates stealthWhite to 100% (1) in the first column on the 4th beat, over a span of 2 beats.
activateMod("stealthWhite", 4, 2, "outCubic", 1, 0)
```

[stealthWhite](_media/stealthWhite.mp4 ':include :type=video controls width=35% muted=true autoplay=true loop=true')

## stealthOpacity/stealthOpacityReceptors

Changes the opacity of the notes and receptors

Column Variant Note Example:
```lua
-- Smoothly interperlates stealthOpacity to 100% (1) in the first column on the 4th beat, over a span of 2 beats.
activateMod("stealthOpacity", 4, 2, "outCubic", 1, 0)
```

Column Variant Receptor Example:
```lua
-- Smoothly interperlates stealthOpacity to 100% (1) in the first column on the 4th beat, over a span of 2 beats.
activateMod("stealthOpacityReceptors", 4, 2, "outCubic", 1, 0)
```

[stealthOpacity](_media/stealthOpacity.mp4 ':include :type=video controls width=35% muted=true autoplay=true loop=true')

## Sprite Path

Currently sprite paths (splines) are pretty buggy, and they will be fixed in the future.

#### pathAlpha

Changes the opacity of the sprite path

Example:
```lua
-- Sets the Sprite Path's alpha to 1 on the start of the song
activateMod("pathAlpha", 0, 0, "outCubic", 1)
```

#### pathDensity

Changes the density of the sprite path

Example:
```lua
-- Sets the Sprite Path's density to 1 on the start of the song
activateMod("pathDensity", 0, 0, "outCubic", 1)
```

## Splines

The sprite path is the visual part of splines (and yes splines are also buggy), but they are less buggy.

Here is an in depth tutorial on them:

[splineTutorial](_media/splineTutorial.mp4 ':include :type=video controls width=35%')

This video is taken from the main tutorial [here](https://www.youtube.com/watch?v=5EfC9jMnxh0&feature=youtu.be).