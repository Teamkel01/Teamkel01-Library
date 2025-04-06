# Teamkel01 Library
This library isnt fully finished.


## Starting the Library

```lua 
-- services
local UIS = game:GetService('UserInputService')
local players = game:GetService("Players")
local tweenService = game:GetService("TweenService")
local runService = game:GetService("RunService")
local coreGui = game:GetService("CoreGui")


-- Instances:

local Teamkel01Gui = Instance.new("ScreenGui")
local TopBar = Instance.new("Frame")
local UICorner = Instance.new("UICorner")
local TopBarCover = Instance.new("Frame")
local Main = Instance.new("Frame")
local UICorner_2 = Instance.new("UICorner")
local TabHolder = Instance.new("Frame")
local UICorner_3 = Instance.new("UICorner")
local TabHolderCover = Instance.new("Frame")
local ButtonHolder = Instance.new("Frame")
local UIPadding = Instance.new("UIPadding")
local Home = Instance.new("TextLabel")
local UIPadding_2 = Instance.new("UIPadding")
local Icon = Instance.new("ImageLabel")
local Scrollingfixer = Instance.new("Frame")
local ContentContainer = Instance.new("ScrollingFrame")
local Button = Instance.new("TextButton")
local UICorner_4 = Instance.new("UICorner")
local UIPadding_3 = Instance.new("UIPadding")
local TextLabel = Instance.new("TextLabel")
local UIPadding_4 = Instance.new("UIPadding")
local UIListLayout = Instance.new("UIListLayout")
local Section = Instance.new("TextLabel")
local Slider = Instance.new("Frame")
local UICorner_5 = Instance.new("UICorner")
local UIPadding_5 = Instance.new("UIPadding")
local TextLabel_2 = Instance.new("TextLabel")
local Value = Instance.new("TextLabel")
local SliderBack = Instance.new("Frame")
local UICorner_6 = Instance.new("UICorner")
local Draggable = Instance.new("Frame")
local UICorner_7 = Instance.new("UICorner")
local Dropdown = Instance.new("Frame")
local UICorner_8 = Instance.new("UICorner")
local UIPadding_6 = Instance.new("UIPadding")
local TextLabel_3 = Instance.new("TextLabel")
local OptionHolder = Instance.new("Frame")
local UIListLayout_2 = Instance.new("UIListLayout")
local Button_2 = Instance.new("Frame")
local UICorner_9 = Instance.new("UICorner")
local UIPadding_7 = Instance.new("UIPadding")
local TextLabel_4 = Instance.new("TextLabel")
local Button_3 = Instance.new("Frame")
local UICorner_10 = Instance.new("UICorner")
local UIPadding_8 = Instance.new("UIPadding")
local TextLabel_5 = Instance.new("TextLabel")
local Button_4 = Instance.new("Frame")
local UICorner_11 = Instance.new("UICorner")
local UIPadding_9 = Instance.new("UIPadding")
local TextLabel_6 = Instance.new("TextLabel")
local Icon_2 = Instance.new("ImageLabel")
local ToggleInactive = Instance.new("Frame")
local UICorner_12 = Instance.new("UICorner")
local UIPadding_10 = Instance.new("UIPadding")
local TextLabel_7 = Instance.new("TextLabel")
local Frame = Instance.new("Frame")
local UICorner_13 = Instance.new("UICorner")
local Frame_2 = Instance.new("Frame")
local UICorner_14 = Instance.new("UICorner")
local ToggleActive = Instance.new("Frame")
local UICorner_15 = Instance.new("UICorner")
local UIPadding_11 = Instance.new("UIPadding")
local TextLabel_8 = Instance.new("TextLabel")
local Frame_3 = Instance.new("Frame")
local UICorner_16 = Instance.new("UICorner")
local Frame_4 = Instance.new("Frame")
local UICorner_17 = Instance.new("UICorner")
local UIListLayout_3 = Instance.new("UIListLayout")
local MainCover = Instance.new("Frame")
local MainCover2 = Instance.new("Frame")
local Title = Instance.new("TextLabel")
local Close = Instance.new("TextButton")
local Minimise = Instance.new("TextButton")

local Closed = false
local ToggleActive = false


local viewport = workspace.CurrentCamera.ViewportSize

local Library = {}
GUI = {}

function Library:validate(defaults, options)
	for i,v in pairs(defaults) do
		if options[i] == nil then
			options[i] = v
		end
	end
	return options
end

local tweenInfo = TweenInfo.new(
	1.5,
	Enum.EasingStyle.Linear,
	Enum.EasingDirection.Out,
	0,
	false,
	0
)

function Library:Init(options) 
	options = Library:validate({
		name = "Teamkel01"
	}, options or {})

	local GUI = {}



	Teamkel01Gui.Name = "Teamkel01Gui"
	Teamkel01Gui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
	Teamkel01Gui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
	Teamkel01Gui.ResetOnSpawn = false

	TopBar.Name = "TopBar"
	TopBar.Parent = Teamkel01Gui
	TopBar.BackgroundColor3 = Color3.fromRGB(10, 10, 10)
	TopBar.BorderColor3 = Color3.fromRGB(0, 0, 0)
	TopBar.BorderSizePixel = 0
	TopBar.Position = UDim2.new(0.282880247, 0, 0.226829275, 0)
	TopBar.Size = UDim2.new(0, 590, 0, 40)

	UICorner.CornerRadius = UDim.new(0, 5)
	UICorner.Parent = TopBar

	TopBarCover.Name = "TopBarCover"
	TopBarCover.Parent = TopBar
	TopBarCover.BackgroundColor3 = Color3.fromRGB(10, 10, 10)
	TopBarCover.BorderColor3 = Color3.fromRGB(0, 0, 0)
	TopBarCover.BorderSizePixel = 0
	TopBarCover.Position = UDim2.new(0, 0, 0.75, 0)
	TopBarCover.Size = UDim2.new(1, 0, 0, 10)

	Main.Name = "Main"
	Main.Parent = TopBar
	Main.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
	Main.BorderColor3 = Color3.fromRGB(0, 0, 0)
	Main.BorderSizePixel = 0
	Main.Position = UDim2.new(0, 0, 1, 0)
	Main.Size = UDim2.new(0, 590, 0, 475)

	UICorner_2.CornerRadius = UDim.new(0, 5)
	UICorner_2.Parent = Main

	TabHolder.Name = "TabHolder"
	TabHolder.Parent = Main
	TabHolder.BackgroundColor3 = Color3.fromRGB(10, 10, 10)
	TabHolder.BorderColor3 = Color3.fromRGB(0, 0, 0)
	TabHolder.BorderSizePixel = 0
	TabHolder.Position = UDim2.new(0, 0, -3.2123765e-08, 0)
	TabHolder.Size = UDim2.new(0.200000003, 0, 1.00000012, 0)

	UICorner_3.CornerRadius = UDim.new(0, 5)
	UICorner_3.Parent = TabHolder

	TabHolderCover.Name = "TabHolderCover"
	TabHolderCover.Parent = TabHolder
	TabHolderCover.BackgroundColor3 = Color3.fromRGB(10, 10, 10)
	TabHolderCover.BorderColor3 = Color3.fromRGB(0, 0, 0)
	TabHolderCover.BorderSizePixel = 0
	TabHolderCover.Position = UDim2.new(0.915254235, 0, 0, 0)
	TabHolderCover.Size = UDim2.new(0, 10, 1, 0)

	ButtonHolder.Name = "ButtonHolder"
	ButtonHolder.Parent = TabHolder
	ButtonHolder.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	ButtonHolder.BackgroundTransparency = 1.000
	ButtonHolder.BorderColor3 = Color3.fromRGB(0, 0, 0)
	ButtonHolder.BorderSizePixel = 0
	ButtonHolder.Position = UDim2.new(0, 0, -3.21237614e-08, 0)
	ButtonHolder.Size = UDim2.new(1, 0, 1.00000012, 0)

	local UIListLayout = Instance.new("UIListLayout")
	UIListLayout.Parent = ButtonHolder
	UIListLayout.HorizontalAlignment = Enum.HorizontalAlignment.Center
	UIListLayout.SortOrder = Enum.SortOrder.LayoutOrder
	UIListLayout.Padding = UDim.new(0, 40)

	UIPadding.Parent = ButtonHolder
	UIPadding.PaddingBottom = UDim.new(0, 8)
	UIPadding.PaddingTop = UDim.new(0, 8)

	-- Find the UIListLayout inside the ButtonHolder
	local buttonHolderLayout = ButtonHolder:FindFirstChildOfClass("UIListLayout")

	-- If the UIListLayout doesn't exist, create one
	if not buttonHolderLayout then
		buttonHolderLayout = Instance.new("UIListLayout")
		buttonHolderLayout.Parent = ButtonHolder
		buttonHolderLayout.HorizontalAlignment = Enum.HorizontalAlignment.Center
		buttonHolderLayout.VerticalAlignment = Enum.VerticalAlignment.Top
		buttonHolderLayout.SortOrder = Enum.SortOrder.LayoutOrder
		buttonHolderLayout.Padding = UDim.new(0, 10) -- Add padding between buttons
	end

	-- Set the padding between buttons
	buttonHolderLayout.Padding = UDim.new(0, 10) -- Adjust this value as needed

	MainCover.Name = "MainCover"
	MainCover.Parent = Main
	MainCover.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
	MainCover.BorderColor3 = Color3.fromRGB(0, 0, 0)
	MainCover.BorderSizePixel = 0
	MainCover.Position = UDim2.new(0.972881377, 0, 0, 0)
	MainCover.Size = UDim2.new(0, 16, 0, 7)

	MainCover2.Name = "MainCover2"
	MainCover2.Parent = Main
	MainCover2.BackgroundColor3 = Color3.fromRGB(10, 10, 10)
	MainCover2.BorderColor3 = Color3.fromRGB(0, 0, 0)
	MainCover2.BorderSizePixel = 0
	MainCover2.Size = UDim2.new(0, 19, 0, 14)

	Title.Name = "Title"
	Title.Parent = TopBar
	Title.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Title.BackgroundTransparency = 1.000
	Title.BorderColor3 = Color3.fromRGB(0, 0, 0)
	Title.BorderSizePixel = 0
	Title.Position = UDim2.new(0.0334360413, 0, 0.125, 0)
	Title.Size = UDim2.new(0, 140, 0, 30)
	Title.Font = Enum.Font.GothamBold
	Title.Text = options.Title
	Title.TextColor3 = Color3.fromRGB(255, 255, 255)
	Title.TextSize = 17.000
	Title.TextWrapped = true
	Title.TextXAlignment = Enum.TextXAlignment.Left

	Close.Name = "Close"
	Close.Parent = TopBar
	Close.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Close.BackgroundTransparency = 1.000
	Close.BorderColor3 = Color3.fromRGB(0, 0, 0)
	Close.BorderSizePixel = 0
	Close.Position = UDim2.new(0.932203412, 0, 0, 0)
	Close.Size = UDim2.new(0, 40, 0, 40)
	Close.Font = Enum.Font.Gotham
	Close.Text = "x"
	Close.TextColor3 = Color3.fromRGB(255, 255, 255)
	Close.TextSize = 20.000
	Close.TextWrapped = true
	Close.MouseButton1Down:Connect(function()
		Teamkel01Gui:Destroy()
	end)

	Minimise.Name = "Minimise"
	Minimise.Parent = TopBar
	Minimise.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Minimise.BackgroundTransparency = 1.000
	Minimise.BorderColor3 = Color3.fromRGB(0, 0, 0)
	Minimise.BorderSizePixel = 0
	Minimise.Position = UDim2.new(0.864406765, 0, 0, 0)
	Minimise.Size = UDim2.new(0, 40, 0, 40)
	Minimise.Font = Enum.Font.Gotham
	Minimise.Text = "_"
	Minimise.TextColor3 = Color3.fromRGB(255, 255, 255)
	Minimise.TextSize = 20.000
	Minimise.TextWrapped = true
	Minimise.MouseButton1Click:Connect(function()
		if Closed == false then
			Main:TweenSize(UDim2.new(0,590,0,0), Enum.EasingDirection.In, Enum.EasingStyle.Linear, 0.25)
			ButtonHolder:TweenSize(UDim2.new(0,118,0,0), Enum.EasingDirection.In, Enum.EasingStyle.Linear, 0.25)
			ContentContainer:TweenSize(UDim2.new(0,458,0,0), Enum.EasingDirection.In, Enum.EasingStyle.Linear, 0.25)
			MainCover:TweenSize(UDim2.new(0,16,0,0), Enum.EasingDirection.In, Enum.EasingStyle.Linear, 0.25)
			MainCover2:TweenSize(UDim2.new(0,19,0,0), Enum.EasingDirection.In, Enum.EasingStyle.Linear, 0.25)
			Closed = true
			wait(0.25)
			Main.Visible = false
		else
			Main:TweenSize(UDim2.new(0,590,0,475), Enum.EasingDirection.In, Enum.EasingStyle.Linear, 0.25)
			ButtonHolder:TweenSize(UDim2.new(0,118,0,475), Enum.EasingDirection.In, Enum.EasingStyle.Linear, 0.25)
			ContentContainer:TweenSize(UDim2.new(0,458,0,455), Enum.EasingDirection.In, Enum.EasingStyle.Linear, 0.25)
			MainCover:TweenSize(UDim2.new(0,16,0,7), Enum.EasingDirection.In, Enum.EasingStyle.Linear, 0.25)
			MainCover2:TweenSize(UDim2.new(0,19,0,14), Enum.EasingDirection.In, Enum.EasingStyle.Linear, 0.25)
			Main.Visible = true
			Closed = false
		end
	end)
end

function GUI:CreateTab(options)
	options = Library:validate({
		name = "Home",
		icon = "rbxassetid://2790547157"
	}, options or {})

	local Tab = {}

	Home.Name = "Home"
	Home.Parent = ButtonHolder
	Home.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Home.BackgroundTransparency = 1.000
	Home.BorderColor3 = Color3.fromRGB(0, 0, 0)
	Home.BorderSizePixel = 0
	Home.Size = UDim2.new(1, 0, 0, 40)
	Home.Font = Enum.Font.GothamBold
	Home.Text = options.Text
	Home.TextColor3 = Color3.fromRGB(255, 255, 255)
	Home.TextSize = 13.000
	Home.TextXAlignment = Enum.TextXAlignment.Left

	UIPadding_2.Parent = Home
	UIPadding_2.PaddingLeft = UDim.new(0, 35)

	Icon.Name = "Icon"
	Icon.Parent = Home
	Icon.BackgroundTransparency = 1.000
	Icon.Position = UDim2.new(0, -30, 0, 7)
	Icon.Size = UDim2.new(0, 25, 0, 25)
	Icon.Image = options.icon

	Scrollingfixer.Name = "Scrolling fixer"
	Scrollingfixer.Parent = Home
	Scrollingfixer.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Scrollingfixer.BackgroundTransparency = 1.000
	Scrollingfixer.BorderColor3 = Color3.fromRGB(0, 0, 0)
	Scrollingfixer.BorderSizePixel = 0
	Scrollingfixer.Position = UDim2.new(1.0963856, 0, 0, 0)
	Scrollingfixer.Size = UDim2.new(0, 455, 0, 459)

	ContentContainer.Name = "ContentContainer"
	ContentContainer.Parent = Scrollingfixer
	ContentContainer.Active = true
	ContentContainer.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	ContentContainer.BackgroundTransparency = 1.000
	ContentContainer.BorderColor3 = Color3.fromRGB(0, 0, 0)
	ContentContainer.BorderSizePixel = 0
	ContentContainer.Position = UDim2.new(-0.00426468067, 0, -0.00192746101, 0)
	ContentContainer.Size = UDim2.new(0, 458, 0, 455)
	ContentContainer.ScrollBarThickness = 0

	-- Find the UIListLayout inside the ContentContainer
	local uiListLayout = ContentContainer:FindFirstChildOfClass("UIListLayout")

	-- If the UIListLayout doesn't exist, create one
	if not uiListLayout then
		uiListLayout = Instance.new("UIListLayout")
		uiListLayout.Parent = ContentContainer
		uiListLayout.HorizontalAlignment = Enum.HorizontalAlignment.Center
		uiListLayout.VerticalAlignment = Enum.VerticalAlignment.Top
		uiListLayout.SortOrder = Enum.SortOrder.LayoutOrder
		uiListLayout.Padding = UDim.new(0, 35) -- Add padding between buttons
	end

	-- Set the padding between buttons
	uiListLayout.Padding = UDim.new(0, 10) -- Adjust this value as needed

end

function GUI:Button(options, parentFrame)
	options = Library:validate({
		text = "Button",
		Callback = function() end,
		initialPosition = nil  -- Default initial position
	}, options or {})

	-- Create the button inside the provided parent frame or ContentContainer if no frame is provided
	local buttonParent = parentFrame or ContentContainer

	-- Calculate the Y position based on the number of existing buttons
	local buttonCount = #buttonParent:GetChildren()
	local buttonYPosition = -40 + buttonCount * 40  -- Base Y position for subsequent buttons
	if buttonCount == 0 then
		buttonYPosition = 0  -- Adjust Y position for the first button
	end

	local button = Instance.new("TextButton")
	button.Name = "Button"
	button.Parent = buttonParent
	button.BackgroundColor3 = Color3.fromRGB(10, 10, 10)
	button.BorderColor3 = Color3.fromRGB(0, 0, 0)
	button.Font = Enum.Font.Ubuntu
	button.Text = options.text
	button.TextSize = 15
	button.TextColor3 = Color3.fromRGB(255, 255, 255)
	button.BorderSizePixel = 0
	button.Position = UDim2.new(0.02, 0, 0, buttonYPosition)
	button.Size = UDim2.new(0.96, 0, 0, 35)

	local UICorner = Instance.new("UICorner")
	UICorner.CornerRadius = UDim.new(0, 4)
	UICorner.Parent = button

	-- Connect the callback function to the button click event
	button.MouseButton1Click:Connect(options.Callback)

	return button
end































function GUI:Toggle(options, parentFrame)
	options = options or {}
	local text = options.text or "Toggle"
	local callback = options.callback or function(state) end

	-- Create the button inside the provided parent frame or ContentContainer if no frame is provided
	local toggleParent = parentFrame or ContentContainer

	-- Calculate the Y position based on the number of existing toggle buttons
	local toggleCount = #toggleParent:GetChildren()
	local toggleYPosition = -40 + toggleCount * 40  -- Base Y position for subsequent toggles
	if toggleCount == 0 then
		toggleYPosition = 0  -- Adjust Y position for the first toggle
	end

	local ToggleInactive = Instance.new("Frame")
	ToggleInactive.Name = "ToggleInactive"
	ToggleInactive.Parent = toggleParent
	ToggleInactive.BackgroundColor3 = Color3.fromRGB(10, 10, 10)
	ToggleInactive.BorderColor3 = Color3.fromRGB(0, 0, 0)
	ToggleInactive.BorderSizePixel = 0
	ToggleInactive.Position = UDim2.new(0.02, 0, 0, toggleYPosition)
	ToggleInactive.Size = UDim2.new(0.96, 0, 0, 35)

	local UICorner_12 = Instance.new("UICorner")
	UICorner_12.CornerRadius = UDim.new(0, 4)
	UICorner_12.Parent = ToggleInactive

	local UIPadding_10 = Instance.new("UIPadding")
	UIPadding_10.Parent = ToggleInactive
	UIPadding_10.PaddingBottom = UDim.new(0, 6)
	UIPadding_10.PaddingLeft = UDim.new(0, 6)
	UIPadding_10.PaddingRight = UDim.new(0, 6)
	UIPadding_10.PaddingTop = UDim.new(0, 6)

	local TextLabel_7 = Instance.new("TextLabel")
	TextLabel_7.Parent = ToggleInactive
	TextLabel_7.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	TextLabel_7.BackgroundTransparency = 1.000
	TextLabel_7.BorderColor3 = Color3.fromRGB(0, 0, 0)
	TextLabel_7.BorderSizePixel = 0
	TextLabel_7.Size = UDim2.new(1, 0, 1, 0)
	TextLabel_7.Font = Enum.Font.Ubuntu
	TextLabel_7.Text = text
	TextLabel_7.TextColor3 = Color3.fromRGB(255, 255, 255)
	TextLabel_7.TextSize = 15
	TextLabel_7.TextXAlignment = Enum.TextXAlignment.Left

	local ToggleFrame = Instance.new("Frame")
	ToggleFrame.Parent = ToggleInactive
	ToggleFrame.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
	ToggleFrame.BorderColor3 = Color3.fromRGB(0, 0, 0)
	ToggleFrame.BorderSizePixel = 0
	ToggleFrame.Position = UDim2.new(0.869976342, 0, 0, 3)
	ToggleFrame.Size = UDim2.new(0, 50, 0, 17)

	local UICorner_13 = Instance.new("UICorner")
	UICorner_13.CornerRadius = UDim.new(0, 5)
	UICorner_13.Parent = ToggleFrame

	local ToggleButton = Instance.new("TextButton")
	ToggleButton.Parent = ToggleFrame
	ToggleButton.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	ToggleButton.BorderColor3 = Color3.fromRGB(0, 0, 0)
	ToggleButton.BorderSizePixel = 0
	ToggleButton.Text = ""
	ToggleButton.Position = UDim2.new(0.00219298247, 0, 0, 0)
	ToggleButton.Size = UDim2.new(0, 25, 0, 17)

	local UICorner_14 = Instance.new("UICorner")
	UICorner_14.CornerRadius = UDim.new(0, 3)
	UICorner_14.Parent = ToggleButton

	local ToggleActive = false -- Initialize ToggleActive

	ToggleButton.MouseButton1Click:Connect(function()
		if ToggleActive == false then
			ToggleButton:TweenPosition(UDim2.new(1, -ToggleButton.Size.X.Offset, 0, 0), Enum.EasingDirection.InOut, Enum.EasingStyle.Linear, 0.1, true)
			ToggleActive = true
		else
			ToggleActive = false
			ToggleButton:TweenPosition(UDim2.new(0.00219298247, 0, 0, 0), Enum.EasingDirection.In, Enum.EasingStyle.Linear, 0.1)
		end
	end)

	ToggleButton.MouseButton1Click:Connect(function()
		callback(ToggleActive) -- Pass the current state of the toggle button to the callback
	end)
end







function GUI:Slider(options, parentFrame)
	options = Library:validate({
		text = options.text or "Slider",
		min = options.min or 0,
		max = options.max or 100,
		default = options.default or 16,
		callback = options.callback or function(v) print(v) end
	}, options or {})

	local slider = {}

	-- Calculate the Y position based on the number of existing sliders
	local sliderCount = #parentFrame:GetChildren()
	local sliderYPosition = -27 + sliderCount * 37
	if sliderCount == 0 then
		sliderYPosition = 0  -- Adjust Y position for the first slider
	end

	local SliderFrame = Instance.new("Frame")
	SliderFrame.Name = "SliderFrame"
	SliderFrame.Parent = parentFrame
	SliderFrame.BackgroundColor3 = Color3.fromRGB(10, 10, 10)
	SliderFrame.BorderColor3 = Color3.fromRGB(0, 0, 0)
	SliderFrame.BorderSizePixel = 0
	SliderFrame.Position = UDim2.new(0.02, 0, 0, sliderYPosition)
	SliderFrame.Size = UDim2.new(0.96, 0, 0, 55)

	local UICorner = Instance.new("UICorner")
	UICorner.CornerRadius = UDim.new(0, 4)
	UICorner.Parent = SliderFrame

	local UIPadding = Instance.new("UIPadding")
	UIPadding.Parent = SliderFrame
	UIPadding.PaddingBottom = UDim.new(0, 6)
	UIPadding.PaddingLeft = UDim.new(0, 6)
	UIPadding.PaddingRight = UDim.new(0, 6)
	UIPadding.PaddingTop = UDim.new(0, 6)

	local TextLabel = Instance.new("TextLabel")
	TextLabel.Parent = SliderFrame
	TextLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	TextLabel.BackgroundTransparency = 1.000
	TextLabel.BorderColor3 = Color3.fromRGB(0, 0, 0)
	TextLabel.BorderSizePixel = 0
	TextLabel.Size = UDim2.new(30, 0, 0, 20)
	TextLabel.Font = Enum.Font.Gotham
	TextLabel.Text = options.text
	TextLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
	TextLabel.TextSize = 15
	TextLabel.TextWrapped = true
	TextLabel.TextXAlignment = Enum.TextXAlignment.Left

	local Value = Instance.new("TextLabel")
	Value.Name = "Value"
	Value.Parent = SliderFrame
	Value.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Value.BackgroundTransparency = 1.000
	Value.BorderColor3 = Color3.fromRGB(0, 0, 0)
	Value.BorderSizePixel = 0
	Value.Position = UDim2.new(0.955082715, 0, -0.157719657, 0)
	Value.Size = UDim2.new(0, 25, 0, 25)
	Value.Font = Enum.Font.Ubuntu
	Value.Text = tostring(options.default)
	Value.TextColor3 = Color3.fromRGB(255, 255, 255)
	Value.TextSize = 15.000
	Value.TextWrapped = true

	local SliderBack = Instance.new("Frame")
	SliderBack.Name = "SliderBack"
	SliderBack.Parent = SliderFrame
	SliderBack.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
	SliderBack.BorderColor3 = Color3.fromRGB(0, 0, 0)
	SliderBack.BorderSizePixel = 0
	SliderBack.Position = UDim2.new(0, 0, 0.788598299, 0)
	SliderBack.Size = UDim2.new(1, 0, 0, 5)

	local UICorner_2 = Instance.new("UICorner")
	UICorner_2.Parent = SliderBack

	local Draggable = Instance.new("Frame")
	Draggable.Name = "Draggable"
	Draggable.Parent = SliderBack
	Draggable.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Draggable.BorderColor3 = Color3.fromRGB(0, 0, 0)
	Draggable.BorderSizePixel = 0
	Draggable.Size = UDim2.new(0.1, 0, 1, 0)

	local UICorner_3 = Instance.new("UICorner")
	UICorner_3.Parent = Draggable

	local dragging = false
	local startSize = nil
	local startMousePosition = nil
	local sliderValue = options.default

	-- Methods
	function slider:SetValue(value)
		sliderValue = value
		Value.Text = tostring(sliderValue)
		options.callback(sliderValue)
	end

	function slider:GetValue()
		return sliderValue
	end

	Draggable.InputBegan:Connect(function(input)
		if input.UserInputType == Enum.UserInputType.MouseButton1 then
			dragging = true
			startSize = Draggable.Size.X.Scale  -- Store initial size
			startMousePosition = input.Position.X  -- Store initial mouse position
		end
	end)

	local UIS = game:GetService("UserInputService")

	UIS.InputChanged:Connect(function(value)
		if dragging and value.UserInputType == Enum.UserInputType.MouseMovement then
			local sliderWidth = SliderBack.AbsoluteSize.X
			local delta = value.Position.X - startMousePosition
			local newSize = math.clamp(startSize + (delta / sliderWidth), 0.01, 1)  -- Adjust size based on delta
			Draggable.Size = UDim2.new(newSize, 0, 1, 0)  -- Set new size
			local newValue = math.floor(options.min + (newSize * (options.max - options.min) + 0.5))  -- Calculate value based on position
			Value.Text = tostring(newValue)
			options.callback(newValue)  -- Call the callback with the new value
			sliderValue = newValue  -- Update slider value
		end
	end)

	UIS.InputEnded:Connect(function(input)
		if input.UserInputType == Enum.UserInputType.MouseButton1 then
			dragging = false
		end
	end)

	return slider
end










function GUI:Section(options)
	options = Library:validate({
		text = "Section"  -- Change 'name' to 'text'
	}, options or {})

	local SectionFrame = Instance.new("Frame")
	SectionFrame.Name = "SectionFrame"
	SectionFrame.Parent = ContentContainer
	SectionFrame.BackgroundColor3 = Color3.fromRGB(15, 15, 15)
	SectionFrame.BorderColor3 = Color3.fromRGB(0, 0, 0)
	SectionFrame.BorderSizePixel = 0

	local UICorner_2 = Instance.new("UICorner")
	UICorner_2.CornerRadius = UDim.new(0, 5)
	UICorner_2.Parent = SectionFrame

	local Section = Instance.new("TextLabel")
	Section.Name = "Section"
	Section.Parent = SectionFrame
	Section.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Section.BackgroundTransparency = 1.000
	Section.BorderColor3 = Color3.fromRGB(0, 0, 0)
	Section.BorderSizePixel = 0
	Section.Size = UDim2.new(1, 0, 0, 35) -- Adjusted size to fit the text
	Section.Font = Enum.Font.GothamMedium
	Section.Text = options.text  -- Change from options.name to options.text
	Section.TextColor3 = Color3.fromRGB(255, 255, 255)
	Section.TextSize = 15.000
	Section.TextXAlignment = Enum.TextXAlignment.Left

	local sectionPadding = Instance.new("UIPadding")
	sectionPadding.Parent = Section
	sectionPadding.PaddingLeft = UDim.new(0, 5)  -- Adjust this value to move the text to the right

	-- Dynamically adjust the size of the section frame based on the content
	local function updateSectionSize()
		local totalHeight = Section.Size.Y.Offset + 5
		for _, child in ipairs(SectionFrame:GetChildren()) do
			if child:IsA("TextLabel") or child:IsA("TextButton") or child:IsA("Frame") then
				totalHeight = totalHeight + child.Size.Y.Offset + 5 -- Add 5 pixels of padding between elements
			end
			if child.Name == "SliderFrame" then
				totalHeight = totalHeight + 20 -- Adjust height for sliders
			end
		end
		SectionFrame.Size = UDim2.new(1, 0, 0, totalHeight)
	end

	SectionFrame.ChildAdded:Connect(updateSectionSize)
	SectionFrame.ChildRemoved:Connect(updateSectionSize)

	return SectionFrame
end















function GUI:Notification(options)
	options = Library:validate({
		Title = options.Title or "Title",
		Description = options.Description or "Description",
		Time = tonumber(options.Time) or 3  -- Convert Time to a number
	}, options or {})

	local NotificationsGUI = game.Players.LocalPlayer:WaitForChild("PlayerGui"):FindFirstChild("Notifications")
	if not NotificationsGUI then
		NotificationsGUI = Instance.new("ScreenGui")
		NotificationsGUI.Name = "Notifications"
		NotificationsGUI.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
		NotificationsGUI.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
	end

	-- Calculate the position of the new notification frame
	local existingNotifications = NotificationsGUI:GetChildren()
	local yOffset = -105 * #existingNotifications  -- Adjust this value to increase the space between notifications
	local position = UDim2.new(1, 0, 0.8, yOffset)  -- Starting position for new notification frame

	local NotificationFrame = Instance.new("Frame")
	NotificationFrame.Name = "NotificationFrame"
	NotificationFrame.Parent = NotificationsGUI
	NotificationFrame.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
	NotificationFrame.BorderColor3 = Color3.fromRGB(0, 0, 0)
	NotificationFrame.BorderSizePixel = 0
	NotificationFrame.Position = position
	NotificationFrame.Size = UDim2.new(0, 300, 0, 100) -- Initial size

	local UICorner = Instance.new("UICorner")
	UICorner.CornerRadius = UDim.new(0, 7)
	UICorner.Parent = NotificationFrame

	local Title = Instance.new("TextLabel")
	Title.Name = "Title"
	Title.Parent = NotificationFrame
	Title.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Title.BackgroundTransparency = 1.000
	Title.BorderColor3 = Color3.fromRGB(0, 0, 0)
	Title.BorderSizePixel = 0
	Title.Position = UDim2.new(0.0233333334, 0, 0.0700000003, 0)
	Title.Size = UDim2.new(0, 260, 0, 30)
	Title.Font = Enum.Font.Ubuntu
	Title.Text = options.Title
	Title.TextColor3 = Color3.fromRGB(255, 255, 255)
	Title.TextSize = 20.000
	Title.TextXAlignment = Enum.TextXAlignment.Left

	local Description = Instance.new("TextLabel")
	Description.Name = "Description"
	Description.Parent = NotificationFrame
	Description.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Description.BackgroundTransparency = 1.000
	Description.BorderColor3 = Color3.fromRGB(0, 0, 0)
	Description.BorderSizePixel = 0
	Description.Position = UDim2.new(0.0233333334, 0, 0.349999994, 0)
	Description.Size = UDim2.new(0, 285, 0, 43)
	Description.Font = Enum.Font.Ubuntu
	Description.Text = options.Description
	Description.TextColor3 = Color3.fromRGB(255, 255, 255)
	Description.TextSize = 16.000
	Description.TextXAlignment = Enum.TextXAlignment.Left

	local Close = Instance.new("TextButton")
	Close.Name = "Close"
	Close.Parent = NotificationFrame
	Close.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Close.BackgroundTransparency = 1.000
	Close.BorderColor3 = Color3.fromRGB(0, 0, 0)
	Close.BorderSizePixel = 0
	Close.Position = UDim2.new(0.899999976, 0, 0, 0)
	Close.Size = UDim2.new(0, 30, 0, 30)
	Close.Font = Enum.Font.SourceSans
	Close.Text = "x"
	Close.TextColor3 = Color3.fromRGB(255, 255, 255)
	Close.TextScaled = true
	Close.TextSize = 14.000
	Close.TextWrapped = true
	Close.MouseButton1Click:Connect(function()
		NotificationFrame:Destroy()
	end)

	local NotificationTimerBackground = Instance.new("Frame")
	NotificationTimerBackground.Name = "NotificationTimerBackground"
	NotificationTimerBackground.Parent = NotificationFrame
	NotificationTimerBackground.BackgroundColor3 = Color3.fromRGB(35, 35, 35)
	NotificationTimerBackground.BorderColor3 = Color3.fromRGB(0, 0, 0)
	NotificationTimerBackground.BorderSizePixel = 0
	NotificationTimerBackground.Position = UDim2.new(0.0233333334, 0, 0.829999983, 0)
	NotificationTimerBackground.Size = UDim2.new(0, 285, 0, 5)

	local UICorner_2 = Instance.new("UICorner")
	UICorner_2.CornerRadius = UDim.new(0, 3)
	UICorner_2.Parent = NotificationTimerBackground

	local NotificationTimer = Instance.new("Frame")
	NotificationTimer.Name = "NotificationTimer"
	NotificationTimer.Parent = NotificationFrame
	NotificationTimer.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	NotificationTimer.BorderColor3 = Color3.fromRGB(0, 0, 0)
	NotificationTimer.BorderSizePixel = 0
	NotificationTimer.Position = UDim2.new(0.0233333334, 0, 0.829999983, 0)
	NotificationTimer.Size = UDim2.new(0, 285, 0, 5)

	local UICorner_3 = Instance.new("UICorner")
	UICorner_3.CornerRadius = UDim.new(0, 3)
	UICorner_3.Parent = NotificationTimer

	NotificationFrame:TweenPosition(UDim2.new(0.77, 0, 0.8, yOffset), Enum.EasingDirection.In, Enum.EasingStyle.Sine, 0.5)

	NotificationTimer:TweenSize(UDim2.new(0, 0, 0, 5), Enum.EasingDirection.In, Enum.EasingStyle.Linear, options.Time)

	wait(options.Time)
	NotificationFrame:TweenPosition(UDim2.new(1, 0, 0.8, yOffset), Enum.EasingDirection.In, Enum.EasingStyle.Back, 0.5)
	wait(0.5)
	NotificationFrame:Destroy()
end





























--Drag

local frame = TopBar
local dragToggle = nil
local dragSpeed = 0.1
local dragStart = nil
local startPos = nil

local function updateInput(input)
	local delta = input.Position - dragStart
	local position = UDim2.new(startPos.X.Scale, startPos.X.Offset + delta.X,
		startPos.Y.Scale, startPos.Y.Offset + delta.Y)
	game:GetService('TweenService'):Create(frame, TweenInfo.new(dragSpeed), {Position = position}):Play()
end

frame.InputBegan:Connect(function(input)
	if (input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch) then 
		dragToggle = true
		dragStart = input.Position
		startPos = frame.Position
		input.Changed:Connect(function()
			if input.UserInputState == Enum.UserInputState.End then
				dragToggle = false
			end
		end)
	end
end)

UIS.InputChanged:Connect(function(input)
	if input.UserInputType == Enum.UserInputType.MouseMovement or input.UserInputType == Enum.UserInputType.Touch then
		if dragToggle then
			updateInput(input)
		end
	end
end)


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
local section = GUI:Section({
    text = "My Section"
})
```

## Creating a Button

```lua
local button1 = GUI:Button({
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
