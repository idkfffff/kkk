local ScreenGui = Instance.new("ScreenGui")local Main = Instance.new("Frame")local Logo = Instance.new("TextLabel")local Close = Instance.new("TextButton")local EspName = Instance.new("TextButton")local Fullbright = Instance.new("TextButton")local InfiniteJump = Instance.new("TextButton")local Speed = Instance.new("TextButton")local Open = Instance.new("ImageButton")local TextBox = Instance.new("TextBox")ScreenGui.Parent = script.Parent--ScreenGui.Parent = game.CoreGui
Main.Name = "Main"Main.Parent = ScreenGui Main.BackgroundColor3 = Color3.fromRGB(0, 0, 0)Main.BorderColor3 = Color3.fromRGB(0, 0, 0)Main.BorderSizePixel = 0 Main.Position = UDim2.new(0.307, 0,0.209, 0)Main.Size = UDim2.new(0, 624,0, 443)Main.Visible = false
Main.Active = true Main.Draggable = true TextBox.Position = UDim2.new(0.069, 0,0.174, 0)TextBox.Parent = Main TextBox.ZIndex = 2 TextBox.Size = UDim2.new(0, 200,0, 50)TextBox.BackgroundColor3 = Color3.fromRGB(255, 255, 255)TextBox.Font = Enum.Font.SourceSansBold TextBox.TextScaled = true
Logo.BackgroundTransparency = 1 Logo.Position = UDim2.new(0.017, 0,0.029, 0)Logo.Size = UDim2.new(0.084, 0,0.042, 0)Logo.Font = Enum.Font.SourceSansBold Logo.Text = "B A D T I M E   H U B"Logo.TextSize = 27 Logo.TextStrokeTransparency = 1 Logo.TextColor3 = Color3.fromRGB(255, 255, 255)
Logo.TextXAlignment = Enum.TextXAlignment.Left Logo.Parent = Main Close.Name = "Close"Close.Parent = Main Close.BackgroundTransparency = 1 Close.Position = UDim2.new(0.934, 0,0, 0)Close.Size = UDim2.new(0, 43,0, 40)Close.Font = Enum.Font.SourceSans Close.Text = "×"
Close.TextColor3 = Color3.fromRGB(255, 255, 255)Close.TextScaled = false Close.TextSize = 30 Close.TextStrokeTransparency = 0.000 Close.TextWrapped = false Close.MouseButton1Down:connect(function()Main.Visible = false Open.Visible = true end)
EspName.Name = "Earned All Chest"EspName.Parent = Main EspName.BackgroundColor3 = Color3.fromRGB(255, 255, 255)EspName.BackgroundTransparency = 0.900 EspName.BorderColor3 = Color3.fromRGB(0, 0, 0)EspName.BorderSizePixel = 0
EspName.Position = UDim2.new(0.042, 0,0.677, 0)EspName.Size = UDim2.new(0, 200,0, 50)EspName.Font = Enum.Font.Arcade EspName.Text = "Earned All Chest"EspName.TextColor3 = Color3.fromRGB(255, 255, 255)EspName.TextScaled = true EspName.TextSize = 14.000 EspName.TextStrokeTransparency = 0.000
EspName.TextWrapped = true EspName.MouseButton1Down:connect(function() for k,v in pairs(game:GetService("Workspace").Chests:GetChildren()) do firetouchinterest(game.Players.LocalPlayer.Character.HumanoidRootPart,v,0)end end)

Fullbright.Name = "Fullbright"
Fullbright.Parent = Main
Fullbright.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Fullbright.BackgroundTransparency = 0.900
Fullbright.BorderColor3 = Color3.fromRGB(0, 0, 0)
Fullbright.BorderSizePixel = 0
Fullbright.Position = UDim2.new(0.440841585, 0, 0.351881504, 0)
Fullbright.Size = UDim2.new(0, 70, 0, 50)
Fullbright.Font = Enum.Font.Arcade
Fullbright.Text = "Fullbright"
Fullbright.TextColor3 = Color3.fromRGB(255, 255, 255)
Fullbright.TextScaled = true
Fullbright.TextSize = 14.000
Fullbright.TextStrokeTransparency = 0.000
Fullbright.TextWrapped = true
Fullbright.MouseButton1Down:connect(function()
	if not _G.FullBrightExecuted then

		_G.FullBrightEnabled = false

		_G.NormalLightingSettings = {
			Brightness = game:GetService("Lighting").Brightness,
			ClockTime = game:GetService("Lighting").ClockTime,
			FogEnd = game:GetService("Lighting").FogEnd,
			GlobalShadows = game:GetService("Lighting").GlobalShadows,
			Ambient = game:GetService("Lighting").Ambient
		}

		game:GetService("Lighting"):GetPropertyChangedSignal("Brightness"):Connect(function()
			if game:GetService("Lighting").Brightness ~= 1 and game:GetService("Lighting").Brightness ~= _G.NormalLightingSettings.Brightness then
				_G.NormalLightingSettings.Brightness = game:GetService("Lighting").Brightness
				if not _G.FullBrightEnabled then
					repeat
						wait()
					until _G.FullBrightEnabled
				end
				game:GetService("Lighting").Brightness = 1
			end
		end)

		game:GetService("Lighting"):GetPropertyChangedSignal("ClockTime"):Connect(function()
			if game:GetService("Lighting").ClockTime ~= 12 and game:GetService("Lighting").ClockTime ~= _G.NormalLightingSettings.ClockTime then
				_G.NormalLightingSettings.ClockTime = game:GetService("Lighting").ClockTime
				if not _G.FullBrightEnabled then
					repeat
						wait()
					until _G.FullBrightEnabled
				end
				game:GetService("Lighting").ClockTime = 12
			end
		end)

		game:GetService("Lighting"):GetPropertyChangedSignal("FogEnd"):Connect(function()
			if game:GetService("Lighting").FogEnd ~= 786543 and game:GetService("Lighting").FogEnd ~= _G.NormalLightingSettings.FogEnd then
				_G.NormalLightingSettings.FogEnd = game:GetService("Lighting").FogEnd
				if not _G.FullBrightEnabled then
					repeat
						wait()
					until _G.FullBrightEnabled
				end
				game:GetService("Lighting").FogEnd = 786543
			end
		end)

		game:GetService("Lighting"):GetPropertyChangedSignal("GlobalShadows"):Connect(function()
			if game:GetService("Lighting").GlobalShadows ~= false and game:GetService("Lighting").GlobalShadows ~= _G.NormalLightingSettings.GlobalShadows then
				_G.NormalLightingSettings.GlobalShadows = game:GetService("Lighting").GlobalShadows
				if not _G.FullBrightEnabled then
					repeat
						wait()
					until _G.FullBrightEnabled
				end
				game:GetService("Lighting").GlobalShadows = false
			end
		end)

		game:GetService("Lighting"):GetPropertyChangedSignal("Ambient"):Connect(function()
			if game:GetService("Lighting").Ambient ~= Color3.fromRGB(178, 178, 178) and game:GetService("Lighting").Ambient ~= _G.NormalLightingSettings.Ambient then
				_G.NormalLightingSettings.Ambient = game:GetService("Lighting").Ambient
				if not _G.FullBrightEnabled then
					repeat
						wait()
					until _G.FullBrightEnabled
				end
				game:GetService("Lighting").Ambient = Color3.fromRGB(178, 178, 178)
			end
		end)

		game:GetService("Lighting").Brightness = 1
		game:GetService("Lighting").ClockTime = 12
		game:GetService("Lighting").FogEnd = 786543
		game:GetService("Lighting").GlobalShadows = false
		game:GetService("Lighting").Ambient = Color3.fromRGB(178, 178, 178)

		local LatestValue = true
		spawn(function()
			repeat
				wait()
			until _G.FullBrightEnabled
			while wait() do
				if _G.FullBrightEnabled ~= LatestValue then
					if not _G.FullBrightEnabled then
						game:GetService("Lighting").Brightness = _G.NormalLightingSettings.Brightness
						game:GetService("Lighting").ClockTime = _G.NormalLightingSettings.ClockTime
						game:GetService("Lighting").FogEnd = _G.NormalLightingSettings.FogEnd
						game:GetService("Lighting").GlobalShadows = _G.NormalLightingSettings.GlobalShadows
						game:GetService("Lighting").Ambient = _G.NormalLightingSettings.Ambient
					else
						game:GetService("Lighting").Brightness = 1
						game:GetService("Lighting").ClockTime = 12
						game:GetService("Lighting").FogEnd = 786543
						game:GetService("Lighting").GlobalShadows = false
						game:GetService("Lighting").Ambient = Color3.fromRGB(178, 178, 178)
					end
					LatestValue = not LatestValue
				end
			end
		end)
	end

	_G.FullBrightExecuted = true
	_G.FullBrightEnabled = not _G.FullBrightEnabled
end)

InfiniteJump.Name = "InfiniteJump"
InfiniteJump.Parent = Main
InfiniteJump.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
InfiniteJump.BackgroundTransparency = 0.900
InfiniteJump.BorderColor3 = Color3.fromRGB(0, 0, 0)
InfiniteJump.BorderSizePixel = 0
InfiniteJump.Position = UDim2.new(0.62244463, 0, 0.54112041, 0)
InfiniteJump.Size = UDim2.new(0, 200, 0, 50)
InfiniteJump.Font = Enum.Font.Arcade
InfiniteJump.Text = "Infinite Jump"
InfiniteJump.TextColor3 = Color3.fromRGB(255, 255, 255)
InfiniteJump.TextScaled = true
InfiniteJump.TextSize = 14.000
InfiniteJump.TextStrokeTransparency = 0.000
InfiniteJump.TextWrapped = true
InfiniteJump.MouseButton1Down:connect(function()
	local InfiniteJumpEnabled = true
	game:GetService("UserInputService").JumpRequest:connect(function()
		if InfiniteJumpEnabled then
			game:GetService"Players".LocalPlayer.Character:FindFirstChildOfClass'Humanoid':ChangeState("Jumping")
		end
	end)
	local InfiniteJump = CreateButton("Infinite Jump: Off", StuffFrame)
	InfiniteJump.Position = UDim2.new(0,10,0,130)
	InfiniteJump.Size = UDim2.new(0,150,0,30)
	InfiniteJump.MouseButton1Click:connect(function()
		local state = InfiniteJump.Text:sub(string.len("Infinite Jump: ") + 1) --too lazy to count lol
		local new = state == "Off" and "On" or state == "On" and "Off"
		InfiniteJumpEnabled = new == "On"
		InfiniteJump.Text = "Infinite Jump: " .. new
	end)
end)

Speed.Name = "Speed"
Speed.Parent = Main
Speed.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Speed.BackgroundTransparency = 0.900
Speed.BorderColor3 = Color3.fromRGB(0, 0, 0)
Speed.BorderSizePixel = 0
Speed.Position = UDim2.new(0.069, 0,0.327, 0)
Speed.Size = UDim2.new(0, 200,0, 24)
Speed.Font = Enum.Font.Arcade
Speed.Text = "Speed"
Speed.TextColor3 = Color3.fromRGB(255, 255, 255)
Speed.TextScaled = true
Speed.TextSize = 14.000
Speed.TextStrokeTransparency = 0.000
Speed.TextWrapped = true
Speed.MouseButton1Down:connect(function()
	game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = TextBox.Text
end)

Open.Name = "Open"
Open.Parent = ScreenGui
Open.BackgroundTransparency = 1
Open.Position = UDim2.new(0.015, 0,0.445, 0)
Open.Size = UDim2.new(0, 60,0, 32)
Open.Active = true
Open.Image = "rbxassetid://3926307971"
Open.ScaleType = Enum.ScaleType.Fit
Open.ImageRectOffset = Vector2.new(964, 4)
Open.ImageRectSize = Vector2.new(36, 36)
--Open.Draggable = true

Open.MouseButton1Down:connect(function()
	Open.Visible = false
	Main.Visible = true
end)
