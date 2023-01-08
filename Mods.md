## Information
Following in [NotITG](https://www.noti.tg/)'s footsteps, Average4K has developed some built in mods which are normally used to create other mods.

The rest of this page will be dedicated to documenting those built in mods.

Note: all videos on this page are from [this video](https://www.youtube.com/watch?v=5EfC9jMnxh0&feature=youtu.be). Which is why there is music in these videos.

## amovex
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

## amovey

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

## drunk

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

## tipsy

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