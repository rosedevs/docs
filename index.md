## Rose Wrapper Documentation

Please remember this is __limited__ execution, meaning it can be **very** unstable at points.
At the moment we can only fetch values, and use class functions which will be documented below.

__game:GetService("Players"):GetPlayers()__
_Table - Returns all the players in your game_
```lua
local players = game:GetService("Players")
table.foreach(players:GetPlayers(), function(i,p) print(p.Name) end)


local players = game:GetService("Players")
for i,v in pairs(players:GetPlayers()) do
  print(v.Name)
end
```

__game:GetService("Players"):GetGuests()__
_Table - Returns all the guests in your game_
```lua
local players = game:GetService("Players")
table.foreach(players:GetGuests(), function(i,p) print(p.Name) end)


local players = game:GetService("Players")
for i,v in pairs(players:GetGuests()) do
  print(v.Name)
end
```

__game:GetService("Players"):Find(string player)__
_Table - Find the player by a shortname_
```lua
local players = game:GetService("Players")
local me = players:Find("example")
if me ~= nil then
  print(me.Name)
end
```
