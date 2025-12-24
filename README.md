-- Rayfield UI
local Rayfield = loadstring(game:HttpGet("https://sirius.menu/rayfield"))()

local Window = Rayfield:CreateWindow({
	Name = "Unbeatable's Haxx",
	LoadingTitle = "loading hacks duh",
	LoadingSubtitle = "by unbeatable",
	Theme = "DarkBlue",

	ConfigurationSaving = {
		Enabled = true,
		FileName = "Big Hub"
	},

	KeySystem = true,
	KeySettings = {
		Title = "Unbeatable's key system",
		Subtitle = "Key System",
		Note = "No method of obtaining the key is provided",
		FileName = "Key",
		SaveKey = true,
		Key = {"tZ2sozp7aMSh a7z!"}
	}
})

Rayfield:Notify({
	Title = "Just letting you know",
	Content = "This hub was made in 2025. Scripts may break in future years.",
	Duration = 6
})

-- ======================
-- SCRIPTS TAB
-- ======================
local ScriptsTab = Window:CreateTab("SCRIPTS", 4483362458)

ScriptsTab:CreateButton({
	Name = "Infinite Yield",
	Callback = function()
		loadstring(game:HttpGet("https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source"))()
	end
})

ScriptsTab:CreateButton({
	Name = "Prison Life",
	Callback = function()
		loadstring(game:HttpGet("https://raw.githubusercontent.com/devguy100/PrizzLife/main/pladmin.lua"))()
	end
})

ScriptsTab:CreateButton({
	Name = "Da Hood",
	Callback = function()
		loadstring(game:HttpGet("https://raw.githubusercontent.com/SpaceYes/Lua/Main/DaHood.lua"))()
	end
})

ScriptsTab:CreateButton({
	Name = "Mic Up",
	Callback = function()
		loadstring(game:HttpGet("https://whimper.xyz/kitty"))()
	end
})

ScriptsTab:CreateButton({
	Name = "Murder Mystery 2",
	Callback = function()
		loadstring(game:HttpGet("https://raw.githubusercontent.com/Rojojin/MM2-Script/main/main.lua"))()
	end
})

ScriptsTab:CreateButton({
	Name = "AOT Revolution",
	Callback = function()
		loadstring(game:HttpGet("https://raw.githubusercontent.com/zerunquist/TekkitAotr/main/main.lua"))()
	end
})

ScriptsTab:CreateButton({
	Name = "Blue Lock Rivals",
	Callback = function()
		loadstring(game:HttpGet("https://raw.githubusercontent.com/Piskasiska22222/tester/main/test"))()
	end
})

ScriptsTab:CreateButton({
	Name = "Combat Warriors",
	Callback = function()
		loadstring(game:HttpGet("https://raw.githubusercontent.com/SpiritXmas/Project-Hook/main/required.lua"))()
	end
})

ScriptsTab:CreateButton({
	Name = "Crazy Dance Moves",
	Callback = function()
		loadstring(game:HttpGet("https://rawscripts.net/raw/Universal-Script-Energize-10408"))()
	end
})

ScriptsTab:CreateButton({
	Name = "Death Penalty",
	Callback = function()
		loadstring(game:HttpGet("https://raw.githubusercontent.com/0Ben1/fe/main/obf_rf6iQURzu1fqrytcnLBAvW34C9N55kS9g9G3CKz086rC47M6632sEd4ZZYB0AYgV.lua.txt", true))()
	end
})

ScriptsTab:CreateButton({
	Name = "Spelling Bee",
	Callback = function()
		loadstring(game:HttpGet("https://raw.githubusercontent.com/PreppyHub/PreppyHub/main/PreppyHub.lua"))()
	end
})

ScriptsTab:CreateButton({
	Name = "Hoops",
	Callback = function()
		loadstring(game:HttpGet("https://raw.githubusercontent.com/timothytuffknuckles/Blessed/main/autosave.luau"))()
	end
})

-- ======================
-- PLAYER TAB
-- ======================
local PlayerTab = Window:CreateTab("PLAYER", 4483362458)

PlayerTab:CreateSlider({
	Name = "WalkSpeed",
	Range = {0, 500},
	Increment = 16,
	CurrentValue = 16,
	Callback = function(Value)
		local hum = game.Players.LocalPlayer.Character and
			game.Players.LocalPlayer.Character:FindFirstChild("Humanoid")
		if hum then
			hum.WalkSpeed = Value
		end
	end
})

PlayerTab:CreateSlider({
	Name = "JumpPower",
	Range = {0, 500},
	Increment = 25,
	CurrentValue = 50,
	Callback = function(Value)
		local hum = game.Players.LocalPlayer.Character and
			game.Players.LocalPlayer.Character:FindFirstChild("Humanoid")
		if hum then
			hum.JumpPower = Value
		end
	end
})

PlayerTab:CreateSlider({
	Name = "Player Size",
	Range = {0.5, 3},
	Increment = 0.1,
	CurrentValue = 1,
	Callback = function(Value)
		local char = game.Players.LocalPlayer.Character
		local hum = char and char:FindFirstChild("Humanoid")
		if not hum then return end

		if hum.RigType == Enum.HumanoidRigType.R15 then
			for _, scale in ipairs({
				hum:FindFirstChild("BodyHeightScale"),
				hum:FindFirstChild("BodyWidthScale"),
				hum:FindFirstChild("BodyDepthScale"),
				hum:FindFirstChild("HeadScale")
			}) do
				if scale then
					scale.Value = Value
				end
			end
		end
	end
})
