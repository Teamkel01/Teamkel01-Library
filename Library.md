# Teamkel01 Library
This library isnt fully finished.


## Starting the Library

```lua 
loadstring(game:HttpGet(('https://pastebin.com/raw/k9j3n9Pm')))()
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
local button = GUI:Button({
	text = "Button",
	Callback = function()
		print("Button clicked!")
	end,
}, section)
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
}, section)
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
}, section)
```
## Creating a Notification

```lua
local Notification = GUI:Notification({ Title = "Title", Description = "Hello", Time = "3" })
```
