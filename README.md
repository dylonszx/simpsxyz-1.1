-- carregar biblioteca 
local Fluent = loadstring(game:HttpGet("https://github.com/dawid-scripts/Fluent/releases/latest/download/main.lua"))()

-- aviso ao executar
Fluent:Notify({ Title = "EXECUTADO!", Content = "EXECUTADO COM SUCESSO!" })


local Window = Fluent:CreateWindow({
    Title = "Simpsxyz" .. Fluent.Version,
    TabWidth = 160, 
    Size = UDim2.fromOffset(580, 460), 
    Theme = "oceano"
})

local Tabs = {
    Main = Window:AddTab({ Title = "Inicio" }),
}

-- botões 
Tabs.Main:AddButton({ Title = "Radio", Callback = function() 
_G.boomboxb = game:GetObjects('rbxassetid://740618400')[1]
_G.boomboxb.Parent = game:GetService'Players'.LocalPlayer.Backpack
loadstring(_G.boomboxb.Client.Source)() 
loadstring(_G.boomboxb.Server.Source)() --the original scripts made by roblox with minor changes.
end })

-- botões 
Tabs.Main:AddButton({ Title = "Teleport Mouse (TP CLICK)", Callback = function() 
mouse = game.Players.LocalPlayer:GetMouse()
tool = Instance.new("Tool")
tool.RequiresHandle = false
tool.Name = "CLICK TP"
tool.Activated:connect(function()
local pos = mouse.Hit+Vector3.new(0,2.5,0)
pos = CFrame.new(pos.X,pos.Y,pos.Z)
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = pos
end)
tool.Parent = game.Players.LocalPlayer.Backpack
end })

-- botões 
Tabs.Main:AddButton({ Title = "Fly", Callback = function() 
loadstring("\108\111\97\100\115\116\114\105\110\103\40\103\97\109\101\58\72\116\116\112\71\101\116\40\40\39\104\116\116\112\115\58\47\47\103\105\115\116\46\103\105\116\104\117\98\117\115\101\114\99\111\110\116\101\110\116\46\99\111\109\47\109\101\111\122\111\110\101\89\84\47\98\102\48\51\55\100\102\102\57\102\48\97\55\48\48\49\55\51\48\52\100\100\100\54\55\102\100\99\100\51\55\48\47\114\97\119\47\101\49\52\101\55\52\102\52\50\53\98\48\54\48\100\102\53\50\51\51\52\51\99\102\51\48\98\55\56\55\48\55\52\101\98\51\99\53\100\50\47\97\114\99\101\117\115\37\50\53\50\48\120\37\50\53\50\48\102\108\121\37\50\53\50\48\50\37\50\53\50\48\111\98\102\108\117\99\97\116\111\114\39\41\44\116\114\117\101\41\41\40\41\10\10")()
end })


-- botões 
Tabs.Main:AddButton({ Title = "infinite jump", Callback = function() 
loadstring(game:HttpGet("https://raw.githubusercontent.com/HeyGyt/infjump/main/main"))()
end })

-- botões 
Tabs.Main:AddButton({ Title = "ESP", Callback = function() 
loadstring(game:HttpGet("https://raw.githubusercontent.com/dylonszx/ESP/refs/heads/main/README.md"))()
end })

end })


local Tabs = {
    Main = Window:AddTab({ Title = "Extras" }),

}

-- botões 
Tabs.Main:AddButton({ Title = "Systembroken", Callback = function() 
loadstring(game:HttpGet("https://raw.githubusercontent.com/H20CalibreYT/SystemBroken/main/script"))()
end })


-- botões 
Tabs.Main:AddButton({ Title = "Comandos admin", Callback = function() 
loadstring(game:HttpGet('https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source'))()
end })


-- botões 
Tabs.Main:AddButton({ Title = "REDzHUB", Callback = function() 
loadstring(game:HttpGet("https://raw.githubusercontent.com/REDzHUB/REDzHUB/main/REDzHUB"))()
end })

-- botões 
Tabs.Main:AddButton({ Title = "FE ADMIN", Callback = function() 
loadstring(game:HttpGetAsync("https://pastebin.com/raw/R8kwGUem"))()
end })
