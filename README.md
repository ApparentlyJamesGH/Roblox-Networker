# Networker
Simple to use networking system to make developing smoother &amp; having basic protection against exploiters.
This module simply creates an `Events` folder in `ReplicatedStorage` and using the `:bind()` method, creates the respective bindable (randomized Name for security).

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
