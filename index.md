## Rose Wrapper Documentation

Please remember this is __limited__ execution, meaning it can be **very** unstable at points.
At the moment we can only fetch values, and use class functions which will be documented below.

__Fetching Values__
_Bool/String/Int/Number Values_
```lua
local yourValue = game.Workspace.Example
print(yourValue.ClassName.." - "..yourValue.Value)
```

__DataModel:GetService(string servicename)__
_DataModel - Get service by name_
```lua
local players = game:GetService("Players")
if players ~= nil then
  print'Good'
end

local rs = game:GetService("jdskdskdj")
if rs == nil then
  warn'Bad'
end
```

__Instance:Destroy()__
_Instance - Destroy the instance given_
```lua
local me = game.Players.LocalPlayer.Name
game.Workspace:FindFirstChild(me):Destroy()


local part = game.Workspace.Part
game.Workspace:FindFirstChild(part):Destroy()
```

__Instance:IsA(string className)__
_Instance - Returns true if the object is an instance of the given class, or if the object's class inherits from the given class_
```lua
print(Workspace:IsA("Instance" )) --> true
print(Workspace:IsA("Workspace")) --> true
print(game:IsA("Workspace")) --> false
print(game:IsA("DataModel")) --> true
```

__Instance:FindFirstChild(string name)__
_Instance - Returns the first child found with the given name, or nil if no such child exists_
```lua
local found = workspace:FindFirstChild("Brick")
if found then 
  print'Good'
  return
end
warn'Bad'
```


__Instance:ClearAllChildren()__
_Instance - Removes all descendants of the object_
```lua
local part = workspace:FindFirstChild("Part")

print("Part has " .. #part:GetChildren() .. " children")
 
part:ClearAllChildren()
 
print("Part has " .. #part:GetChildren() .. " children")
```

__Players:GetPlayers()__
_Table - Returns all the players in your game_
```lua
local players = game:GetService("Players")
table.foreach(players:GetPlayers(), function(i,p) print(p.Name) end)


local players = game:GetService("Players")
for i,v in pairs(players:GetPlayers()) do
  print(v.Name)
end
```

__Players:GetGuests()__
_Table - Returns all the guests in your game_
```lua
local players = game:GetService("Players")
table.foreach(players:GetGuests(), function(i,p) print(p.Name) end)


local players = game:GetService("Players")
for i,v in pairs(players:GetGuests()) do
  print(v.Name)
end
```

__Players:Find(string player)__
_Table - Find the player by a shortname_
```lua
local players = game:GetService("Players")
local me = players:Find("example")
if me[1] ~= nil then
  print(me.Name)
end
```
__Players:GetChildren()__
_Table - Returns all the Players in your game_
```lua
for i,v in pairs(game.Players:GetChildren())
do print(v.Name)
end
```
