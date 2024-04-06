# Teamkel01 Library
This library isnt fully finished.


## Starting the Library

```lua 
loadstring(game:HttpGet(('https://raw.githubusercontent.com/Teamkel01/Teamkel01-Library/main/Source)'),true))()
```
## Creating the Window

```lua
local main = Library:Init { Title = "Teamkel01" }
```
## Creating a Tab

```lua
local Tab = GUI:CreateTab({
		Text = "Tab",
		icon = "rbxassetid://2790547157"
	})
```
## Creating a Section

```lua
    local Section = GUI:Section({
	    text = "Section",
	})
```

## Creating a Button

```lua
	local Button = GUI:Button({
		text = "Button",
		Callback = function()
			print("Clicked")
		end
	})
```

## Creating a Toggle

```lua
local Toggle = GUI:Toggle({
	text = "Toggle",
	callback = function(ToggleActive)
		if ToggleActive then
			print("Toggle Off")
		else
			print("Toggle On")
		end
	end
})
```

## Creating a Slider

```lua
local Slider = GUI:Slider({
	text = "WalkSpeed",
	min = 16,
	max = 100,
	default = 16,
	callback = function(value)
		local humanoid = game.Players.LocalPlayer.Character and game.Players.LocalPlayer.Character:FindFirstChildOfClass("Humanoid")
		if humanoid then
			humanoid.WalkSpeed = value
		end
		end
})
```

