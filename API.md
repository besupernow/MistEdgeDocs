# API

## Data
data is the Main variable for calling the Module and Needs to be Required.

Example:
```lua
data = require(script.Parent.DataStore)
```
| **Functions**  |
|---|
|**:onJoin()** *object*  |
|**:onLeave()** *object* |
|**:TimeSave()** *void* |
| **:ShowGui()** *void* |
| **:Update()** *void* |
| **:AutoUpdate()** *bool* |

## Functions

### data:onJoin()
data:onJoin(player) Can be called when the Player Joins the Game. To make sure that the Function Functions Right we have to put it in `game.Players.PlayerAdded` Function to call it at the right time. 

Example:
``` lua
data = require(script.Parent.DataStore)
game.Players.PlayerAdded:Connect(function(player)
data:onJoin(player)
end)
```
#### Requirements
*player*

> [!TIP|style:flat|label:Core Function|iconVisibility:hidden]
> This Function is a Core Function

### data:onLeave()
data:onLeave(player) Can be called when the Player Joins the Game. To make sure that the Function Functions Right we have to put it in `game.Players.PlayerLeave` Function to call it at the right time. 
``` lua
data = require(script.Parent.DataStore)
game.Players.PlayerLeave:Connect(function(player)
data:onLeave(player)
end)
```
#### Requirements
*player*

> [!TIP|style:flat|label:Core Function|iconVisibility:hidden]
> This Function is a Core Function


### data:TimeSave()
data:TimeSave() Creates a Interval of when the Data Updates to The Server. 

Example
```lua
data = require(script.Parent.DataStore)
timer = 10
while wait(timer)do
data:TimeSave()
end
```
#### Requirements
None

> [!NOTE|style:flat|label:Optional|iconVisibility:hidden]
> This is an Optional Function, but is Recommended to Use

### data:Update()
data:Update() can Update when the Function is Called

Example for a Save Button:
``` lua
data = require(script.Parent.DataStore)
script.Parent.MouseButton1Click:Connect(function()
data:Update()
end)
```

#### Requirements 
None

> [!TIP|style:flat|label:Tip]
> Use Within a Function to allow more Functionality


### data:ShowGui()
data:ShowGui() Shows the Save Dialogue.

> [!WARNING|style:flat|label:Not Implemented]
> This Function has not been Implemented in the Module

### data:AutoUpdate()
data:AutoUpdate() sends a bool value to see if autoupdating is on
``` lua
data = require(script.Parent.DataStore)
data:AutoUpdate(true)
end)
```

#### Requirements
*bool*

> [!NOTE|style:flat|label:Recommended|iconVisibility:hidden]
> This is an Optional Function, but is Recommended to Use
