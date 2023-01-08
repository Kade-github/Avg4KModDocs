## Setting up the modfile
> Quick guide on the structure, and how to setup a modfile

Average4K's default chart directories look something like this:

```
└── chartFolder
     ├── chart.sm
     └── banner.png
```

Which works for regular files, but to make this a modfile. You have to create a **mod** folder

```
└── chartFolder/
     ├── chart.sm
     ├── banner.png
     └── mod/
         └── mod.lua
```

This folder also contains a **lua** file called *"mod.lua"*.

Inside this file is where all of the lua code will go, and the template for the initial state of a modchart is:

```lua
function create()
    -- Lua! Horray
end
```

## Activating mods