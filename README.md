# Networker
Simple to use networking system to make developing smoother &amp; having basic protection against exploiters.
This module simply creates an `Events` folder in `ReplicatedStorage` and using the `:bind()` method, creates the respective bindable (randomized Name for security).

## Usage
### Binding events/funtions
To bind a remote, simply use the `:bind()` method: (Server -> Client)
```lua
Network:bind(ROB, Type, Name, Callback)

-- ROB = "Remote" or "Bindable"
-- Type = "Event" or "Function"
-- Name = Any string
-- Callback = Callback function

-- Example:
Network:bind("Remote", "Event", "CreatePart", function(plr, ...)
    local part = Instance.new("Part")
    part.Parent = workspace
end)
```
