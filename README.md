# Networker
Simple to use networking system to make developing smoother &amp; having basic protection against exploiters.
This module simply creates an `Events` folder in `ReplicatedStorage` and using the `:bind()` method, creates the respective bindable (randomized Name for security).

> [!TIP]
> **6/18/24** - Added `returnResultData` option, will return a table with data and functions for the data (`.after()`, ...)

| [Get Model on Roblox](https://create.roblox.com/store/asset/17409077618/Networker) |
| ------------- |

> [!NOTE]
> I'm very aware the code is not too clean. I made this for myself to have a cleaner RS. I don't care how you alter the code whatsoever so if you know what you're doing, do whatever man. There's probably better networking systems available anyway lolz

## Usage
### Binding
To bind a remote, simply use the `:bind()` method:
```lua
Network:bind(ROB, Type, Name, Callback)

-- ROB = "Remote" or "Bindable"
-- Type = "Event" or "Function"
-- Name = Any string
-- Callback = Callback function

-- Example:
Network:bind("Remote", "Event", "CreatePart", function(plr, partName)
    local part = Instance.new("Part")
    part.Parent = workspace
    part.Name = partName
end)
```
### Calling
To call a remote, simply use the `:call()` method:
```lua
Network:call(Name, whoToCall, ...)

-- Name = Any string
-- whoToCall = Player | true (for all players) | nil (for Client -> Server)
-- ... = any arguments

-- Example:
Network:call("CreatePart", nil, "New Part")
```
