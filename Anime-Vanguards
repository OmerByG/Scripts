local Library,Themes = loadstring(game:HttpGet("https://raw.githubusercontent.com/trinyxScripts/nexus-ui/refs/heads/main/nexuslib.lua"))()
local main = Library:new{
	Name = "Anime Vanguards",
	Style = "Classic",
	Theme = "Dark",
	KeySystemConfig = {
		KeySystem = false,
	},
}

local player = game:GetService("Players").LocalPlayer

task.spawn(function()
	    while wait() do
	    gems = player:GetAttribute("Gems") or 0
    end
end)

local gameTab = main:CreateTab({Icon = "globe",Text = "Game"})
local lobbyTab = main:CreateTab({Icon = "globe",Text = "Lobby"})
local eventTab = main:CreateTab({Icon = "satellite-dish",Text = "Event"})
local miscTab = main:CreateTab({Icon = "app-window",Text = "Misc"})
local settingsTab = main:CreateTab({Icon = "settings",Text = "Settings"})

local summonTg = lobbyTab:Toggle({
	Name = "Summon",
	State = false,
	callback = function(v)
	    loop = v
		args = {
			[1] = "SummonMany",
			[2] = "Special",
			[3] = 1,
		}
	    
	    while loop and gems >= 50 do
			game:GetService("ReplicatedStorage").Networking.Units.SummonEvent:FireServer(unpack(args))
			wait()
	    end
	end
})
