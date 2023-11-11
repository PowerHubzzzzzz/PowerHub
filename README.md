game.Players.LocalPlayer.Character.Humanoid.Health = 0


wait(0.5)


game.Players.LocalPlayer.Character.Humanoid.Health = 0


wait(0.5)



local notification = Instance.new("Sound")
notification.Parent = game:GetService("SoundService")
notification.SoundId = "rbxassetid://16647570" --sound id
notification.Volume = 0

game.StarterGui:SetCore("SendNotification", {
      Icon = "http://www.roblox.com/asset/?id=";
      Title = "Xonic Hub Map Blox Fruits", 
      Text = "Youtube link : https://www.youtube.com/@XONICHUB";
notification:Play()
})

local notification = Instance.new("Sound")
notification.Parent = game:GetService("SoundService")
notification.SoundId = "rbxassetid://16647570" --sound id
notification.Volume = 0

game.StarterGui:SetCore("SendNotification", {
      Icon = "http://www.roblox.com/asset/?id=";
      Title = "Open Highlight", 
      Text = "Youtube link : https://www.youtube.com/@XONICHUB";
notification:Play()
})

_G.AutoHighlight = true

spawn(function()
        while wait() do
            if _G.AutoHighlight then
                pcall(function()
                    wait(1)
                    local players = game.Players:GetPlayers()

                    for i,v in pairs(players) do
                    local esp = Instance.new("Highlight")
                    esp.Name = v.Name
                    esp.FillTransparency = 0.4
                    esp.FillColor = Color3.new(0, 255, 0)
                    esp.OutlineColor = Color3.new(1, 0.333333, 1)
                    esp.OutlineTransparency = 0
                    esp.Parent = v.Character
                    end
                    game.Players.LocalPlayer.Character.Highlight:Destroy()
                    wait(0.5)
                    local players = game.Players:GetPlayers()

                    for i,v in pairs(players) do
                    local esp = Instance.new("Highlight")
                    esp.Name = v.Name
                    esp.FillTransparency = 0.4
                    esp.FillColor = Color3.new(0, 255, 0)
                    esp.OutlineColor = Color3.new(1, 0.333333, 1)
                    esp.OutlineTransparency = 0
                    esp.Parent = v.Character
                    end
                    game.Players.LocalPlayer.Character.Highlight:Destroy()
                end)
            end
        end
    end)
    
    _G.Color = Color3.fromRGB(3, 174, 255)
_G.Logo = 7743878857


local Evil = loadstring(game:HttpGet("https://newpchx2.0xlii.repl.co/AllUI/Protected_9405524596134885.lua"))()
local Win = library:Evil("Xonic","Hub",_G.Logo )

local tab1 = Win:CraftTab('Main')
local page1 = tab1:CraftPage('Main',1)

local player = page1:Label('Auto Farm Kaitan')

loadstring(game:HttpGet("https://raw.githubusercontent.com/PowerHubzzzzzz/XonicHub2/main/README.md?token=GHSAT0AAAAAACJ3FRNRHM4P6YEWN524HXEEZKPIUQA"))();
spawn(function()
	while wait() do
		if _G.Auto_Farm_Level then
			pcall(function()
				local QuestTitle = game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text
				if not string.find(QuestTitle, NameMon) then
					StartMagnet = false
					game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
				end
				if game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false then
					StartMagnet = false
					CheckQuest()
					repeat wait() TP1(CFrameQuest) until (CFrameQuest.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 3 or not _G.Auto_Farm_Level
					if (CFrameQuest.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 3 then
						wait(0.1)
						game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest",NameQuest,LevelQuest)
						wait(0.1)
					end
				elseif game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == true then
					CheckQuest()
					if game:GetService("Workspace").Enemies:FindFirstChild(Mon) then
						for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
							if v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 then
								if v.Name == Mon then
									if string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, NameMon) then
										repeat task.wait()
											AutoHaki()                                            
											PosMon = v.HumanoidRootPart.CFrame
											TP1(v.HumanoidRootPart.CFrame * CFrame.new(0,40,0))
											v.HumanoidRootPart.CanCollide = false
											v.Humanoid.WalkSpeed = 0
											v.Head.CanCollide = false
											v.HumanoidRootPart.Size = Vector3.new(70,70,70)
											StartMagnet = true
											game:GetService'VirtualUser':CaptureController()
											game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
										until not _G.Auto_Farm_Level or v.Humanoid.Health <= 0 or not v.Parent or game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false
									else
										StartMagnet = false
										game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
									end
								end
							end
						end
					else
						TP1(CFrameMon)
						StartMagnet = false
						if game:GetService("ReplicatedStorage"):FindFirstChild(Mon) then
						 TP1(game:GetService("ReplicatedStorage"):FindFirstChild(Mon).HumanoidRootPart.CFrame * CFrame.new(15,10,2))
						end
					end
				end
			end)
		end
	end
end)

spawn(function()
    pcall(function()
        while wait() do
			if _G.Auto_Farm_Level then
				if game.Players.LocalPlayer.Data.Level.Value >= 10 then
					game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(-7894.6176757813, 5547.1416015625, -380.29119873047))
					TP1(CFrame.new(-7679.40723, 5565.16113, -502.522491, -0.948657334, -1.87793722e-11, -0.316305608, -1.05328055e-11, 1, -2.77811975e-11, 0.316305608, -2.30232517e-11, -0.948657334))
                    StartMagnet = false
                    for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                        if v.Name == "Shanda [Lv. 475]" then
							repeat task.wait()
								AutoHaki()
                                StartMagnet = true
								_G.FastAttackNoob = true
								game:GetService'VirtualUser':CaptureController()
								game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
                                TP1(v.HumanoidRootPart.CFrame * CFrame.new(1,14,1))
                                wait(.1)
                                TP1(v.HumanoidRootPart.CFrame * CFrame.new(10,14,10))
                                wait(.1)
                                TP1(v.HumanoidRootPart.CFrame * CFrame.new(20,14,19))
                                wait(.1)
                                TP1(v.HumanoidRootPart.CFrame * CFrame.new(15,14,13))
                                wait(.1)
                                TP1(v.HumanoidRootPart.CFrame * CFrame.new(10,14,5))
                                wait(.1)
                                TP1(v.HumanoidRootPart.CFrame * CFrame.new(6,14,2))
                                wait(.1)
                                TP1(v.HumanoidRootPart.CFrame * CFrame.new(1,14,1))
                            until not _G.Fast_Farm_Level or v.Humanoid.Health <= 0 or game.Players.LocalPlayer.Character.Humanoid.Health <= 0
                            break  -- Exit the loop once the enemy is defeated or the player dies
                        end
                    end
                end
            end
        end
    end)
end)

spawn(function()
		while wait() do
			if _G.Auto_Farm_Level then
				pcall(function()
				CheckQuest()
		   for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
	for x,y in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
	if v.Name == "Shanda [Lv. 475]" then
		if y.Name == "Shanda [Lv. 475]" then
	   v.HumanoidRootPart.CFrame = y.HumanoidRootPart.CFrame
	   v.HumanoidRootPart.Size = Vector3.new(60,60,60)
	   y.HumanoidRootPart.Size = Vector3.new(60,60,60)
	   v.HumanoidRootPart.Transparency = 1
	   v.HumanoidRootPart.CanCollide = false
	   y.HumanoidRootPart.CanCollide = false
	   v.Humanoid.WalkSpeed = 0
	   y.Humanoid.WalkSpeed = 0
	   v.Humanoid.JumpPower = 0
	   y.Humanoid.JumpPower = 0
	   if sethiddenproperty then
		 sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)
	end
	end
	end
	end
	end
	end)
	end
	end
	end)

page1:Button('Super Fast Attack',function()
    _G.SuperFastMode = true

local plr = game.Players.LocalPlayer

local CbFw = debug.getupvalues(require(plr.PlayerScripts.CombatFramework))
local CbFw2 = CbFw[2]

function GetCurrentBlade() 
    local p13 = CbFw2.activeController
    local ret = p13.blades[1]
    if not ret then return end
    while ret.Parent~=game.Players.LocalPlayer.Character do ret=ret.Parent end
    return ret
end
function AttackNoCD() 
    local AC = CbFw2.activeController
    for i = 1, 1 do 
        local bladehit = require(game.ReplicatedStorage.CombatFramework.RigLib).getBladeHits(
            plr.Character,
            {plr.Character.HumanoidRootPart},
            60
        )
        local cac = {}
        local hash = {}
        for k, v in pairs(bladehit) do
            if v.Parent:FindFirstChild("HumanoidRootPart") and not hash[v.Parent] then
                table.insert(cac, v.Parent.HumanoidRootPart)
                hash[v.Parent] = true
            end
        end
        bladehit = cac
        if #bladehit > 0 then
            local u8 = debug.getupvalue(AC.attack, 5)
            local u9 = debug.getupvalue(AC.attack, 6)
            local u7 = debug.getupvalue(AC.attack, 4)
            local u10 = debug.getupvalue(AC.attack, 7)
            local u12 = (u8 * 798405 + u7 * 727595) % u9
            local u13 = u7 * 798405
            (function()
                u12 = (u12 * u9 + u13) % 1099511627776
                u8 = math.floor(u12 / u9)
                u7 = u12 - u8 * u9
            end)()
            u10 = u10 + 1
            debug.setupvalue(AC.attack, 5, u8)
            debug.setupvalue(AC.attack, 6, u9)
            debug.setupvalue(AC.attack, 4, u7)
            debug.setupvalue(AC.attack, 7, u10)
            pcall(function()
                for k, v in pairs(AC.animator.anims.basic) do
                    v:Play()
                end                  
            end)
            if plr.Character:FindFirstChildOfClass("Tool") and AC.blades and AC.blades[1] then 
                game:GetService("ReplicatedStorage").RigControllerEvent:FireServer("weaponChange",tostring(GetCurrentBlade()))
                game.ReplicatedStorage.Remotes.Validator:FireServer(math.floor(u12 / 1099511627776 * 16777215), u10)
                game:GetService("ReplicatedStorage").RigControllerEvent:FireServer("hit", bladehit, i, "") 
            end
        end
    end
end
local cac
if _G.SuperFastMode then 
	cac=task.wait
else
	cac=wait
end
while cac() do 
	AttackNoCD()
end
end)

page1:Toggle('Auto Farm Kaitan',nil,function(value)
    _G.Auto_Farm_Level = value
	_G.Double_Quest = value 
	_G.Player_Hunter = value
	_G.Auto_Saber = value
    _G.FastAttack = value
	_G.AutoBuyLegendarySword = value 
	_G.Start_Kaitan = value
        StopTween(_G.Auto_Farm_Level)
end)
