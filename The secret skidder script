LaLaLa Hub

local Players = game:GetService("Players")
local LocalPlayer = Players.LocalPlayer
local UIS = game:GetService("UserInputService")
local TweenService = game:GetService("TweenService")

-- 🖥️ Welcome Animation GUI
local splashGui = Instance.new("ScreenGui", Players.LocalPlayer:WaitForChild("PlayerGui"))
splashGui.Name = "LaLaLaSplash"
splashGui.ResetOnSpawn = false

local splashFrame = Instance.new("Frame", splashGui)
splashFrame.Size = UDim2.new(0, 400, 0, 200)
splashFrame.Position = UDim2.new(0.5, -200, 0.5, -100)
splashFrame.BackgroundColor3 = Color3.fromRGB(255, 255, 0)
splashFrame.BackgroundTransparency = 1
splashFrame.BorderSizePixel = 0
Instance.new("UICorner", splashFrame).CornerRadius = UDim.new(0, 12)

local welcomeText = Instance.new("TextLabel", splashFrame)
welcomeText.Size = UDim2.new(1, 0, 0.6, 0)
welcomeText.Position = UDim2.new(0, 0, 0, 0)
welcomeText.BackgroundTransparency = 1
welcomeText.Text = "👋 Welcome to LaLaLa Hub"
welcomeText.Font = Enum.Font.FredokaOne
welcomeText.TextSize = 28
welcomeText.TextColor3 = Color3.fromRGB(50, 50, 50)

local creditsText = Instance.new("TextLabel", splashFrame)
creditsText.Size = UDim2.new(1, -10, 0.4, 0)
creditsText.Position = UDim2.new(0, 10, 0.6, 0)
creditsText.BackgroundTransparency = 1
creditsText.Text = "Created by Nicholas"
creditsText.Font = Enum.Font.Gotham
creditsText.TextSize = 18
creditsText.TextColor3 = Color3.fromRGB(80, 80, 80)
creditsText.TextXAlignment = Enum.TextXAlignment.Right
creditsText.TextYAlignment = Enum.TextYAlignment.Bottom

-- Fade-in animation
TweenService:Create(splashFrame, TweenInfo.new(0.8), {BackgroundTransparency = 0.2}):Play()
task.wait(3)
TweenService:Create(splashFrame, TweenInfo.new(0.8), {BackgroundTransparency = 1}):Play()
task.wait(0.8)
splashGui:Destroy()

-- 🧠 Main GUI Setup
local gui = Instance.new("ScreenGui", Players.LocalPlayer:WaitForChild("PlayerGui"))
gui.Name = "LaLaLaHub"
gui.ResetOnSpawn = false

-- Toggle Button
local toggleBtn = Instance.new("ImageButton")
toggleBtn.Size = UDim2.new(0, 60, 0, 60)
toggleBtn.Position = UDim2.new(0, 20, 0.5, -30)
toggleBtn.BackgroundColor3 = Color3.fromRGB(255, 255, 0)
toggleBtn.Image = "rbxassetid://3926305904"
toggleBtn.ImageColor3 = Color3.fromRGB(50, 50, 50)
toggleBtn.Parent = gui
toggleBtn.AutoButtonColor = false
toggleBtn.BackgroundTransparency = 0.2
toggleBtn.BorderSizePixel = 0
toggleBtn.AnchorPoint = Vector2.new(0, 0.5)
toggleBtn.ZIndex = 2

-- Hover effect
toggleBtn.MouseEnter:Connect(function()
	toggleBtn:TweenSize(UDim2.new(0, 65, 0, 65), "Out", "Quad", 0.2, true)
end)
toggleBtn.MouseLeave:Connect(function()
	toggleBtn:TweenSize(UDim2.new(0, 60, 0, 60), "Out", "Quad", 0.2, true)
end)

-- Main Frame
local mainFrame = Instance.new("Frame")
mainFrame.Size = UDim2.new(0, 520, 0, 320)
mainFrame.Position = UDim2.new(0.5, -260, 0.5, -160)
mainFrame.BackgroundColor3 = Color3.fromRGB(230, 230, 230)
mainFrame.Visible = false
mainFrame.Parent = gui
mainFrame.BorderSizePixel = 0
mainFrame.BackgroundTransparency = 0.1
Instance.new("UICorner", mainFrame).CornerRadius = UDim.new(0, 12)

-- Drop shadow
local shadow = Instance.new("ImageLabel", mainFrame)
shadow.Size = UDim2.new(1, 20, 1, 20)
shadow.Position = UDim2.new(0, -10, 0, -10)
shadow.BackgroundTransparency = 1
shadow.Image = "rbxassetid://1316045217"
shadow.ImageTransparency = 0.5
shadow.ZIndex = 0

-- Title
local title = Instance.new("TextLabel")
title.Size = UDim2.new(1, 0, 0, 40)
title.BackgroundTransparency = 1
title.Text = "🌟 LaLaLa Hub 🌟"
title.Font = Enum.Font.FredokaOne
title.TextSize = 28
title.TextColor3 = Color3.fromRGB(255, 215, 0)
title.Parent = mainFrame

-- Tabs (Left)
local tabFrame = Instance.new("Frame")
tabFrame.Size = UDim2.new(0, 130, 1, -40)
tabFrame.Position = UDim2.new(0, 0, 0, 40)
tabFrame.BackgroundColor3 = Color3.fromRGB(255, 255, 0)
tabFrame.Parent = mainFrame
Instance.new("UICorner", tabFrame).CornerRadius = UDim.new(0, 8)

-- Buttons (Right)
local buttonFrame = Instance.new("Frame")
buttonFrame.Size = UDim2.new(1, -140, 1, -40)
buttonFrame.Position = UDim2.new(0, 140, 0, 40)
buttonFrame.BackgroundColor3 = Color3.fromRGB(245, 245, 245)
buttonFrame.Parent = mainFrame
Instance.new("UICorner", buttonFrame).CornerRadius = UDim.new(0, 8)

-- Toggle GUI with animation
local open = false
toggleBtn.MouseButton1Click:Connect(function()
	open = not open
	mainFrame.Visible = open
	mainFrame.BackgroundTransparency = 1
	TweenService:Create(mainFrame, TweenInfo.new(0.4), {BackgroundTransparency = 0.1}):Play()
end)

-- Create Toggle Button Function
local function createToggle(name, callback)
	local toggle = Instance.new("TextButton")
	toggle.Size = UDim2.new(1, -20, 0, 40)
	toggle.Position = UDim2.new(0, 10, 0, #buttonFrame:GetChildren() * 45)
	toggle.BackgroundColor3 = Color3.fromRGB(255, 255, 0)
	toggle.Text = name .. " [OFF]"
	toggle.Font = Enum.Font.GothamBold
	toggle.TextSize = 18
	toggle.TextColor3 = Color3.fromRGB(50, 50, 50)
	toggle.Parent = buttonFrame
	Instance.new("UICorner", toggle).CornerRadius = UDim.new(0, 6)

	local state = false
	toggle.MouseButton1Click:Connect(function()
		state = not state
		toggle.Text = name .. (state and " [ON]" or " [OFF]")
		callback(state)
	end)
end

-- MM2 Features
createToggle("Infinite Jump", function(state)
	if state then
		_G.JumpEnabled = true
		UIS.JumpRequest:Connect(function()
			if _G.JumpEnabled then
				LocalPlayer.Character:FindFirstChildOfClass("Humanoid"):ChangeState("Jumping")
			end
		end)
	else
		_G.JumpEnabled = false
	end
end)

createToggle("Fly", function(state)
	if state then
		local flyPart = Instance.new("BodyVelocity")
		flyPart.Velocity = Vector3.new(0, 50, 0)
		flyPart.MaxForce = Vector3.new(0, math.huge, 0)
		flyPart.Parent = LocalPlayer.Character.HumanoidRootPart
		_G.FlyPart = flyPart
	else
		if _G.FlyPart then _G.FlyPart:Destroy() end
	end
end)
createToggle("Teleport to Lobby", function(state)
	if state then
		local char = LocalPlayer.Character
		if char and char:FindFirstChild("HumanoidRootPart") then
			char:MoveTo(Vector3.new(112.871, 137.230, 74.192))
		end
	end
end)
