local Fluent = loadstring(game:HttpGet("https://github.com/dawid-scripts/Fluent/releases/latest/download/main.lua"))()
local SaveManager = loadstring(game:HttpGet("https://raw.githubusercontent.com/dawid-scripts/Fluent/master/Addons/SaveManager.lua"))()
local InterfaceManager = loadstring(game:HttpGet("https://raw.githubusercontent.com/dawid-scripts/Fluent/master/Addons/InterfaceManager.lua"))()

local Window = Fluent:CreateWindow({
    Title = "🥶 " .. Fluent.Version,
    SubTitle = "by Ari",
    TabWidth = 160,
    Size = UDim2.fromOffset(580, 460),
    Acrylic = true, -- The blur may be detectable, setting this to false disables blur entirely
    Theme = "Dark",
    MinimizeKey = Enum.KeyCode.LeftControl -- Used when theres no MinimizeKeybind
})

-- Fluent provides Lucide Icons https://lucide.dev/icons/ for the tabs, icons are optional
local Tabs = {
    Main = Window:AddTab({ Title = "Home", Icon = "home" }),
    Settings = Window:AddTab({ Title = "Maps", Icon = "" }),
    Duel = Window:AddTab({ Title = "Duels", Icon = "" }),
    Pets = Window:AddTab({ Title = ""})
}

local Options = Fluent.Options

do
    Fluent:Notify({
        Title = "Nah",
        Content = "by ari",
        SubContent = " ", -- Optional
        Duration = 2 -- Set to nil to make the notification not disappear
    })

    Tabs.Main:AddParagraph({
        Title = "Ari Script",
        Content = "Join in discord. \nhttps://discord.gg/kgxzbkm37G"
    })

    -- Primeiro Toggle: Auto tower red
    local ToggleRed = Tabs.Settings:AddToggle("MyToggleRed", {Title = "Auto tower red", Default = false})

    ToggleRed:OnChanged(function()
        print("ToggleRed changed:", ToggleRed.Value)
        
        if ToggleRed.Value then
            -- Torre vermelha
            local player = game.Players.LocalPlayer
            local character = player.Character or player.CharacterAdded:Wait()
            local rootPart = character:WaitForChild("HumanoidRootPart")
    
            -- Loop enquanto o ToggleRed for true
            while ToggleRed.Value do
                wait(5.15)  -- Tempo de espera de 4 segundos
                rootPart.CFrame = CFrame.new(-10470.420, 2542.952, -50.633)
            end
        end
    end)
    
    -- Inicializa o valor do ToggleRed como false
    ToggleRed:SetValue(false)

    -- Segundo Toggle: Auto moon tower
    local ToggleMoon = Tabs.Settings:AddToggle("MyToggleMoon", {Title = "Auto moon tower", Default = false})

    ToggleMoon:OnChanged(function()
        print("ToggleMoon changed:", ToggleMoon.Value)
        
        if ToggleMoon.Value then
            -- Torre da lua
            local player = game.Players.LocalPlayer
            local character = player.Character or player.CharacterAdded:Wait()
            local rootPart = character:WaitForChild("HumanoidRootPart")
            
            -- Loop enquanto o ToggleMoon for true
            while ToggleMoon.Value do
                wait(5.15)  -- Tempo de espera de 4 segundos
                rootPart.CFrame = CFrame.new(-5118.3, 6213.82, 145.79)
            end
        end
    end)

    -- Terceiro Toggle: Auto mart tower
    local ToggleMart = Tabs.Settings:AddToggle("MyToggleMart", {Title = "Auto mart tower", Default = false})

    ToggleMart:OnChanged(function()
        print("ToggleMart changed:", ToggleMart.Value)
        
        if ToggleMart.Value then
            -- Torre de Marte
            local player = game.Players.LocalPlayer
            local character = player.Character or player.CharacterAdded:Wait()
            local rootPart = character:WaitForChild("HumanoidRootPart")
            
            -- Loop enquanto o ToggleMart for true
            while ToggleMart.Value do
                wait(5.15)  -- Tempo de espera de 4 segundos
                rootPart.CFrame = CFrame.new(-46.67, 8744.20, 151.233)
            end
        end
    end)

    -- Quarto Toggle: Auto ice tower
    local ToggleIce = Tabs.Settings:AddToggle("ToggleIce", {Title = "Auto ice tower", Default = false})

    ToggleIce:OnChanged(function()
        print("ToggleIce changed:", ToggleIce.Value)
        
        if ToggleIce.Value then
            -- Torre de Gelo
            local player = game.Players.LocalPlayer
            local character = player.Character or player.CharacterAdded:Wait()
            local rootPart = character:WaitForChild("HumanoidRootPart")
            
            -- Loop enquanto o ToggleIce for true (corrigido aqui)
            while ToggleIce.Value do
                wait(5.15)  -- Tempo de espera de 4 segundos
                rootPart.CFrame = CFrame.new(5025.223, 13441.714, 161.198)
            end
        end
    end)
end

    -- Quinto Toggle: Auto Flower tower
    local ToggleFlower = Tabs.Settings:AddToggle("MyToggleFlower", {Title = "Auto flower tower", Default = false})

    ToggleFlower:OnChanged(function()
        print("ToggleFlower changed:", ToggleFlower.Value)
        
        if ToggleFlower.Value then
            -- Torre de Flor
            local player = game.Players.LocalPlayer
            local character = player.Character or player.CharacterAdded:Wait()
            local rootPart = character:WaitForChild("HumanoidRootPart")
            
            -- Loop enquanto o ToggleFlower for true
            while ToggleFlower.Value do
                wait(5.15)  -- Tempo de espera de 4 segundos
                rootPart.CFrame = CFrame.new(10097.19, 19199.77, 169.42)
            end
        end
    end)

    -- Sexto Toggle: Auto Snow tower
    local ToggleSnow = Tabs.Settings:AddToggle("MyToggleSnow", {Title = "Auto snow tower", Default = false})

    ToggleSnow:OnChanged(function()
        print("ToggleSnow changed:", ToggleSnow.Value)
        
        if ToggleSnow.Value then
            -- Torre de Flor
            local player = game.Players.LocalPlayer
            local character = player.Character or player.CharacterAdded:Wait()
            local rootPart = character:WaitForChild("HumanoidRootPart")
            
            -- Loop enquanto o ToggleSnow for true
            while ToggleSnow.Value do
                wait(5.15)  -- Tempo de espera de 4 segundos
                rootPart.CFrame = CFrame.new(15385.9, 27328.3, 185.09)
            end
        end
    end)

        -- Setimo Toggle: Auto Dark tower
        local ToggleDark = Tabs.Settings:AddToggle("MyToggleDark", {Title = "Auto dark tower", Default = false})

        ToggleDark:OnChanged(function()
            print("ToggleDark changed:", ToggleDark.Value)
            
            if ToggleDark.Value then
                -- Torre de Flor
                local player = game.Players.LocalPlayer
                local character = player.Character or player.CharacterAdded:Wait()
                local rootPart = character:WaitForChild("HumanoidRootPart")
                
                -- Loop enquanto o ToggleDark for true
                while ToggleDark.Value do
                    wait(5.15)  -- Tempo de espera de 4 segundos
                    rootPart.CFrame = CFrame.new(20505.63, 45666, 211.43)
                end
            end
        end)

                -- Oitava Toggle: Auto Empty tower
                local ToggleEmpty = Tabs.Settings:AddToggle("MyToggleEmpty", {Title = "Auto empty tower", Default = false})

                ToggleEmpty:OnChanged(function()
                    print("ToggleEmpty changed:", ToggleEmpty.Value)
                    
                    if ToggleEmpty.Value then
                        -- Torre de Flor
                        local player = game.Players.LocalPlayer
                        local character = player.Character or player.CharacterAdded:Wait()
                        local rootPart = character:WaitForChild("HumanoidRootPart")
                        
                        -- Loop enquanto o ToggleEmpty for true
                        while ToggleEmpty.Value do
                            wait(5.15)  -- Tempo de espera de 4 segundos
                            rootPart.CFrame = CFrame.new(25626, 64009.68, 239.275)
                        end
                    end
                end)
                                -- Nona Toggle: Auto Desert tower
                                local ToggleDesert = Tabs.Settings:AddToggle("MyToggleDesert", {Title = "Auto desert tower", Default = false})

                                ToggleDesert:OnChanged(function()
                                    print("ToggleDesert changed:", ToggleDesert.Value)
                                    
                                    if ToggleDesert.Value then
                                        -- Torre de Flor
                                        local player = game.Players.LocalPlayer
                                        local character = player.Character or player.CharacterAdded:Wait()
                                        local rootPart = character:WaitForChild("HumanoidRootPart")
                                        
                                        -- Loop enquanto o ToggleDesert for true
                                        while ToggleDesert.Value do
                                            wait(5.15)  -- Tempo de espera de 4 segundos
                                            rootPart.CFrame = CFrame.new(30746.43, 82358.5, 266.386)
                                        end
                                    end
                                end)
                                                                -- Decima Toggle: Auto Florest tower
                                                                local ToggleFlorest = Tabs.Settings:AddToggle("MyToggleFlorest", {Title = "Auto florest tower", Default = false})

                                                                ToggleFlorest:OnChanged(function()
                                                                    print("ToggleFlorest changed:", ToggleFlorest.Value)
                                                                    
                                                                    if ToggleFlorest.Value then
                                                                        -- Torre de Flor
                                                                        local player = game.Players.LocalPlayer
                                                                        local character = player.Character or player.CharacterAdded:Wait()
                                                                        local rootPart = character:WaitForChild("HumanoidRootPart")
                                                                        
                                                                        -- Loop enquanto o ToggleFlorest for true
                                                                        while ToggleFlorest.Value do
                                                                            wait(5.15)  -- Tempo de espera de 4 segundos
                                                                            rootPart.CFrame = CFrame.new(35866, 102661.34, 296.255)
                                                                        end
                                                                    end
                                                                end)

                                                                                                                                -- DecimaPrimeira Toggle: Auto Candy tower
                                                                                                                                local ToggleCandy = Tabs.Settings:AddToggle("MyToggleCandy", {Title = "Auto candy tower", Default = false})

                                                                                                                                ToggleCandy:OnChanged(function()
                                                                                                                                    print("ToggleCandy changed:", ToggleCandy.Value)
                                                                                                                                    
                                                                                                                                    if ToggleCandy.Value then
                                                                                                                                        -- Torre de Flor
                                                                                                                                        local player = game.Players.LocalPlayer
                                                                                                                                        local character = player.Character or player.CharacterAdded:Wait()
                                                                                                                                        local rootPart = character:WaitForChild("HumanoidRootPart")
                                                                                                                                        
                                                                                                                                        -- Loop enquanto o ToggleCandy for true
                                                                                                                                        while ToggleCandy.Value do
                                                                                                                                            wait(5.15)  -- Tempo de espera de 4 segundos
                                                                                                                                            rootPart.CFrame = CFrame.new(40986, 122850, 326.036)
                                                                                                                                        end
                                                                                                                                    end
                                                                                                                                end)

                                                                                                                                                                                                                                                                -- DecimaSegunda Toggle: Auto Punk tower
                                                                                                                                                                                                                                                                local MyTogglePunk = Tabs.Settings:AddToggle("MyTogglePunk", {Title = "Auto punk tower", Default = false})

                                                                                                                                                                                                                                                                MyTogglePunk:OnChanged(function()
                                                                                                                                                                                                                                                                    print("MyTogglePunk changed:", MyTogglePunk.Value)
                                                                                                                                                                                                                                                                    
                                                                                                                                                                                                                                                                    if MyTogglePunk.Value then
                                                                                                                                                                                                                                                                        -- Torre de Flor
                                                                                                                                                                                                                                                                        local player = game.Players.LocalPlayer
                                                                                                                                                                                                                                                                        local character = player.Character or player.CharacterAdded:Wait()
                                                                                                                                                                                                                                                                        local rootPart = character:WaitForChild("HumanoidRootPart")
                                                                                                                                                                                                                                                                        
                                                                                                                                                                                                                                                                        -- Loop enquanto o MyTogglePunk for true
                                                                                                                                                                                                                                                                        while MyTogglePunk.Value do
                                                                                                                                                                                                                                                                            wait(5.15)  -- Tempo de espera de 4 segundos
                                                                                                                                                                                                                                                                            rootPart.CFrame = CFrame.new(46106, 143084.687, 355.921)
                                                                                                                                                                                                                                                                        end
                                                                                                                                                                                                                                                                    end
                                                                                                                                                                                                                                                                end)

                                                                                                                                                                                                                                                                -- DecimaTerceira Toggle: Auto Beach tower
                                                                                                                                                                                                                                                                local MyToggleBeach = Tabs.Settings:AddToggle("MyToggleBeach", {Title = "Auto beach tower", Default = false})

                                                                                                                                                                                                                                                                MyToggleBeach:OnChanged(function()
                                                                                                                                                                                                                                                                    print("MyToggleBeach changed:", MyToggleBeach.Value)
                                                                                                                                                                                                                                                                    
                                                                                                                                                                                                                                                                    if MyToggleBeach.Value then
                                                                                                                                                                                                                                                                        -- Torre de Flor
                                                                                                                                                                                                                                                                        local player = game.Players.LocalPlayer
                                                                                                                                                                                                                                                                        local character = player.Character or player.CharacterAdded:Wait()
                                                                                                                                                                                                                                                                        local rootPart = character:WaitForChild("HumanoidRootPart")
                                                                                                                                                                                                                                                                        
                                                                                                                                                                                                                                                                        -- Loop enquanto o MyToggleBeach for true
                                                                                                                                                                                                                                                                        while MyToggleBeach.Value do
                                                                                                                                                                                                                                                                            wait(5.15)  -- Tempo de espera de 4 segundos
                                                                                                                                                                                                                                                                            rootPart.CFrame = CFrame.new(51226, 163343.7, 385.8)
                                                                                                                                                                                                                                                                        end
                                                                                                                                                                                                                                                                    end
                                                                                                                                                                                                                                                                end)

                                                                                                                                                                                                                                                                -- Toggle para Auto Duel
local ToggleDuel = Tabs.Duels:AddToggle("AutoDuel", {Title = "Auto Duel", Default = false})

ToggleDuel:OnChanged(function()
    print("Auto Duel:", ToggleDuel.Value)

    while ToggleDuel.Value do
        wait(0.5) -- Verifica a cada 0.5 segundos

        local player = game:GetService("Players").LocalPlayer
        local prompt = player.PlayerGui:FindFirstChild("RacePrompt") -- Detecta o prompt da duel

        if prompt and prompt.Enabled then
            game:GetService("ReplicatedStorage"):WaitForChild("PromptForRace"):FireServer()
            print("Duel aceito automaticamente!")
        end
    end
end)


                                                                                                                                                                                                                                                                                                                                                                                                                                                                        -- DecimoQuarto Toggle: Auto Sky tower
                                                                                                                                                                                                                                                                                                                                                                                                                                                                        local MyToggleSky = Tabs.Settings:AddToggle("MyToggleSky", {Title = "Auto sky tower", Default = false})

                                                                                                                                                                                                                                                                                                                                                                                                                                                                        MyToggleSky:OnChanged(function()
                                                                                                                                                                                                                                                                                                                                                                                                                                                                            print("MyToggleSky changed:", MyToggleSky.Value)
                                                                                                                                                                                                                                                                                                                                                                                                                                                                            
                                                                                                                                                                                                                                                                                                                                                                                                                                                                            if MyToggleSky.Value then
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                -- Torre de Flor
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                local player = game.Players.LocalPlayer
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                local character = player.Character or player.CharacterAdded:Wait()
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                local rootPart = character:WaitForChild("HumanoidRootPart")
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                -- Loop enquanto o MyToggleSky for true
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                while MyToggleSky.Value do
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    wait(5.15)  -- Tempo de espera de 4 segundos
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    rootPart.CFrame = CFrame.new(56346, 183586, 416.7)
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                end
                                                                                                                                                                                                                                                                                                                                                                                                                                                                            end
                                                                                                                                                                                                                                                                                                                                                                                                                                                                        end)

                                                                                                                                                                                                                                                                                                                                                                                                                                                                        -- DecimoQuarto Toggle: Auto sky tower
                                                                                                                                                                                                                                                                                                                                                                                                                                                                        local MyToggleSky = Tabs.Settings:AddToggle("MyToggleSky", {Title = "Auto sky tower", Default = false})

                                                                                                                                                                                                                                                                                                                                                                                                                                                                        MyToggleSky:OnChanged(function()
                                                                                                                                                                                                                                                                                                                                                                                                                                                                            print("MyToggleSky changed:", MyToggleSky.Value)
                                                                                                                                                                                                                                                                                                                                                                                                                                                                            
                                                                                                                                                                                                                                                                                                                                                                                                                                                                            if MyToggleSky.Value then
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                -- Torre dos céus
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                local player = game.Players.LocalPlayer
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                local character = player.Character or player.CharacterAdded:Wait()
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                local rootPart = character:WaitForChild("HumanoidRootPart")
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                -- Loop enquanto o MyToggleSky for true
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                while MyToggleSky.Value do
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    wait(5.15)  -- Tempo de espera de 4 segundos
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    rootPart.CFrame = CFrame.new(56346, 183586, 416.7)
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                end
                                                                                                                                                                                                                                                                                                                                                                                                                                                                            end
                                                                                                                                                                                                                                                                                                                                                                                                                                                                        end)
