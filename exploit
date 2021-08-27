local BuildABoat2 = Instance.new("ScreenGui")
local UI = Instance.new("Frame")
local TextButton = Instance.new("TextButton")
local TextLabel = Instance.new("TextLabel")
local TextLabel_2 = Instance.new("TextLabel")

--Properties:
BuildABoat2.ResetOnSpawn = false
BuildABoat2.Name = "BuildABoat2"
BuildABoat2.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
BuildABoat2.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

UI.Name = "UI"
UI.Parent = BuildABoat2
UI.BackgroundColor3 = Color3.fromRGB(77, 77, 77)
UI.BorderColor3 = Color3.fromRGB(0, 0, 0)
UI.Position = UDim2.new(0.0213805735, 0, 0.621931195, 0)
UI.Size = UDim2.new(0, 216, 0, 133)

TextButton.Parent = UI
TextButton.BackgroundColor3 = Color3.fromRGB(122, 0, 0)
TextButton.Position = UDim2.new(0.23340109, 0, 0.2781955, 0)
TextButton.Size = UDim2.new(0, 115, 0, 59)
TextButton.Font = Enum.Font.Cartoon
TextButton.Text = ""
TextButton.TextColor3 = Color3.fromRGB(255, 0, 0)
TextButton.TextSize = 28.000

TextLabel.Parent = UI
TextLabel.BackgroundColor3 = Color3.fromRGB(77, 77, 77)
TextLabel.BorderColor3 = Color3.fromRGB(0, 0, 0)
TextLabel.Position = UDim2.new(0, 0, 0.864661634, 0)
TextLabel.Size = UDim2.new(0, 216, 0, 18)
TextLabel.Font = Enum.Font.SourceSans
TextLabel.Text = "Script by Luxky#0001   UI by Luxky#0001"
TextLabel.TextColor3 = Color3.fromRGB(0, 0, 0)
TextLabel.TextSize = 14.000

TextLabel_2.Parent = UI
TextLabel_2.BackgroundColor3 = Color3.fromRGB(77, 77, 77)
TextLabel_2.BorderColor3 = Color3.fromRGB(0, 0, 0)
TextLabel_2.Size = UDim2.new(0, 216, 0, 20)
TextLabel_2.Font = Enum.Font.SourceSans
TextLabel_2.Text = "Build A Boat AFK AUTO FARM"
TextLabel_2.TextColor3 = Color3.fromRGB(0, 0, 0)
TextLabel_2.TextSize = 14.000

-- Scripts:

local function OUNJ_fake_script() -- TextButton.On/Off 
	local script = Instance.new('LocalScript', TextButton)

	script.Parent.MouseButton1Click:Connect(function()
		if script.Parent.BackgroundColor3 == Color3.new(0.12549, 1, 0.113725) then
			script.Parent.BackgroundColor3 = Color3.new(0.666667, 0, 0)
		else
			script.Parent.BackgroundColor3 = Color3.new(0.12549, 1, 0.113725)
		end
	end)
end
coroutine.wrap(OUNJ_fake_script)()
local function GPCZMU_fake_script() -- TextButton.LocalScript 
	local script = Instance.new('LocalScript', TextButton)

	getgenv().autoFarm = false
	
	local hum = game.Players.LocalPlayer.Character.Humanoid
	
	
	script.Parent.MouseButton1Click:Connect(function()
		getgenv().autoFarm = not getgenv().autoFarm
		
	spawn(function()
			if getgenv().autoFarm == false then
				hum.Health = 0
			end
			while autoFarm == true do
						local TS = game:GetService("TweenService")
						local location2 = CFrame.new(-61, 70.739624, 125) --288
						local location3 = CFrame.new(-55.7065125, -360.739624, 9492.35645, 0, 0, -1, 0, 1, 0, 1, 0, 0)
						local location = CFrame.new(-55.7065125, 70.739624, 9492.35645, 0, 0, -1, 0, 1, 0, 1, 0, 0)
						local plr = game.Players.LocalPlayer.Character.HumanoidRootPart
						local hum = game.Players.LocalPlayer.Character.Humanoid
						local tween1 = TS:Create(game.Players.LocalPlayer.Character.HumanoidRootPart, TweenInfo.new(3), {CFrame = location2 })
						if hum.Health == 0 then
							tween1:Cancel()
						else
							tween1:Play()
						wait(3)
						local tween = TS:Create(game.Players.LocalPlayer.Character.HumanoidRootPart, TweenInfo.new(20), {CFrame = location })
						if hum.Health == 0 then
							tween:Cancel()
						else
							tween:Play()
						wait(20)
						local tween2 = TS:Create(game.Players.LocalPlayer.Character.HumanoidRootPart, TweenInfo.new(3), {CFrame = location3 })
						if hum.Health == 0 then
							tween2:Cancel()
						else
							tween2:Play()
							wait(0.1)
							wait(8)
							workspace.ClaimRiverResultsGold:FireServer()
							wait(10)
						end
					end
				end
			end
		end)
	end)
	
end
coroutine.wrap(GPCZMU_fake_script)()
local function VZWBTQ_fake_script() -- UI.LocalScript 
	local script = Instance.new('LocalScript', UI)

	local dragger = {}; 
	local resizer = {};
	
	do
		local mouse = game:GetService("Players").LocalPlayer:GetMouse();
		local inputService = game:GetService('UserInputService');
		local heartbeat = game:GetService("RunService").Heartbeat;
		-- // credits to Ririchi / Inori for this cute drag function :)
		function dragger.new(frame)
			local s, event = pcall(function()
				return frame.MouseEnter
			end)
	
			if s then
				frame.Active = true;
	
				event:connect(function()
					local input = frame.InputBegan:connect(function(key)
						if key.UserInputType == Enum.UserInputType.MouseButton1 then
							local objectPosition = Vector2.new(mouse.X - frame.AbsolutePosition.X, mouse.Y - frame.AbsolutePosition.Y);
							while heartbeat:wait() and inputService:IsMouseButtonPressed(Enum.UserInputType.MouseButton1) do
								frame:TweenPosition(UDim2.new(0, mouse.X - objectPosition.X + (frame.Size.X.Offset * frame.AnchorPoint.X), 0, mouse.Y - objectPosition.Y + (frame.Size.Y.Offset * frame.AnchorPoint.Y)), 'Out', 'Quad', 0.1, true);
							end
						end
					end)
	
					local leave;
					leave = frame.MouseLeave:connect(function()
						input:disconnect();
						leave:disconnect();
					end)
				end)
			end
		end
	
		function resizer.new(p, s)
			p:GetPropertyChangedSignal('AbsoluteSize'):connect(function()
				s.Size = UDim2.new(s.Size.X.Scale, s.Size.X.Offset, s.Size.Y.Scale, p.AbsoluteSize.Y);
			end)
		end
	end
	script.Parent.Active = true
	script.Parent.Draggable = true
end
coroutine.wrap(VZWBTQ_fake_script)()
