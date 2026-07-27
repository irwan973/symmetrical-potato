-- [[ TOOLSADMIN GUI + ANTIFLING + INVISIBLE + F3X + MOVE ROBLOX + FREE EMOTE + TIGERX 3.5 + SECURE DEX + QUANTUM ONYX + KRIM + FLY ADMIN + SERVERPRO INTEGRATED ]] --
local CoreGui = game:GetService("CoreGui")
local Players = game:GetService("Players")
local RunService = game:GetService("RunService")
local Lighting = game:GetService("Lighting")
local UserInputService = game:GetService("UserInputService")
local TeleportService = game:GetService("TeleportService")
local HttpService = game:GetService("HttpService")
local UserGameSettings = UserSettings():GetService("UserGameSettings")
local LocalPlayer = Players.LocalPlayer
local Mouse = LocalPlayer:GetMouse()

if CoreGui:FindFirstChild("GodModeIrwanGUI") then
    CoreGui.GodModeIrwanGUI:Destroy()
end

local ScreenGui = Instance.new("ScreenGui")
ScreenGui.Name = "GodModeIrwanGUI"
ScreenGui.Parent = CoreGui
ScreenGui.ResetOnSpawn = false

local ToggleButton = Instance.new("ImageButton")
ToggleButton.Name = "ToggleButton"
ToggleButton.Parent = ScreenGui
ToggleButton.BackgroundColor3 = Color3.fromRGB(30, 30, 40)
ToggleButton.Position = UDim2.new(0, 20, 0.5, -25)
ToggleButton.Size = UDim2.new(0, 50, 0, 50)
ToggleButton.Image = "rbxassetid://6031094678"
ToggleButton.Visible = false

local ToggleCorner = Instance.new("UICorner")
ToggleCorner.CornerRadius = UDim.new(1, 0)
ToggleCorner.Parent = ToggleButton

local ToggleStroke = Instance.new("UIStroke")
ToggleStroke.Parent = ToggleButton
ToggleStroke.Thickness = 2.5

RunService.RenderStepped:Connect(function()
    local hueBtn = (tick() * 1.5) % 5 / 5
    ToggleStroke.Color = Color3.fromHSV(hueBtn, 1, 1)
end)

local MainFrame = Instance.new("Frame")
MainFrame.Name = "MainFrame"
MainFrame.Parent = ScreenGui
MainFrame.BackgroundColor3 = Color3.fromRGB(20, 20, 25)
MainFrame.BorderSizePixel = 0
MainFrame.Position = UDim2.new(0.5, -175, 0.5, -225)
MainFrame.Size = UDim2.new(0, 350, 0, 480)
MainFrame.Active = true
MainFrame.Draggable = true

local UICorner = Instance.new("UICorner")
UICorner.CornerRadius = UDim.new(0, 10)
UICorner.Parent = MainFrame

local UIStroke = Instance.new("UIStroke")
UIStroke.Parent = MainFrame
UIStroke.Thickness = 2.5

RunService.RenderStepped:Connect(function()
    local hueMain = tick() % 5 / 5
    UIStroke.Color = Color3.fromHSV(hueMain, 1, 1)
end)

local TitleLabel = Instance.new("TextLabel")
TitleLabel.Parent = MainFrame
TitleLabel.BackgroundColor3 = Color3.fromRGB(30, 30, 40)
TitleLabel.Size = UDim2.new(1, 0, 0, 45)
TitleLabel.Font = Enum.Font.GothamBold
TitleLabel.Text = "🛠 TOOLS ADMIN GUI V5 🛠"
TitleLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
TitleLabel.TextSize = 16

local TitleCorner = Instance.new("UICorner")
TitleCorner.CornerRadius = UDim.new(0, 10)
TitleCorner.Parent = TitleLabel

local CloseBtn = Instance.new("TextButton")
CloseBtn.Name = "CloseBtn"
CloseBtn.Parent = MainFrame
CloseBtn.BackgroundColor3 = Color3.fromRGB(45, 45, 60)
CloseBtn.Position = UDim2.new(1, -38, 0, 8)
CloseBtn.Size = UDim2.new(0, 30, 0, 30)
CloseBtn.Font = Enum.Font.GothamBold
CloseBtn.Text = "X"
CloseBtn.TextColor3 = Color3.fromRGB(255, 69, 0)
CloseBtn.TextSize = 14

local CloseCorner = Instance.new("UICorner")
CloseCorner.CornerRadius = UDim.new(0, 6)
CloseCorner.Parent = CloseBtn

CloseBtn.MouseButton1Click:Connect(function()
    MainFrame.Visible = false
    ToggleButton.Visible = true
end)

ToggleButton.MouseButton1Click:Connect(function()
    MainFrame.Visible = true
    ToggleButton.Visible = false
end)

local TikTokLabel = Instance.new("TextLabel")
TikTokLabel.Parent = MainFrame
TikTokLabel.BackgroundColor3 = Color3.fromRGB(25, 25, 32)
TikTokLabel.Position = UDim2.new(0, 0, 1, -30)
TikTokLabel.Size = UDim2.new(1, 0, 0, 30)
TikTokLabel.Font = Enum.Font.GothamMedium
TikTokLabel.Text = "toolsadmin | TikTok: _irwan.vx"
TikTokLabel.TextColor3 = Color3.fromRGB(180, 180, 180)
TikTokLabel.TextSize = 13

local TikTokCorner = Instance.new("UICorner")
TikTokCorner.CornerRadius = UDim.new(0, 10)
TikTokCorner.Parent = TikTokLabel

local ButtonContainer = Instance.new("ScrollingFrame")
ButtonContainer.Parent = MainFrame
ButtonContainer.BackgroundTransparency = 1
ButtonContainer.Position = UDim2.new(0, 10, 0, 55)
ButtonContainer.Size = UDim2.new(1, -20, 1, -95)
ButtonContainer.CanvasSize = UDim2.new(0, 0, 0, 4550)
ButtonContainer.ScrollBarThickness = 4

local UIListLayout = Instance.new("UIListLayout")
UIListLayout.Parent = ButtonContainer
UIListLayout.SortOrder = Enum.SortOrder.LayoutOrder
UIListLayout.Padding = UDim.new(0, 10)

local function createButton(name, text, callback)
    local btn = Instance.new("TextButton")
    btn.Name = name
    btn.Parent = ButtonContainer
    btn.BackgroundColor3 = Color3.fromRGB(45, 45, 60)
    btn.Size = UDim2.new(1, 0, 0, 40)
    btn.Font = Enum.Font.GothamSemibold
    btn.Text = text
    btn.TextColor3 = Color3.fromRGB(255, 255, 255)
    btn.TextSize = 14
    
    local btnCorner = Instance.new("UICorner")
    btnCorner.CornerRadius = UDim.new(0, 8)
    btnCorner.Parent = btn
    
    btn.MouseButton1Click:Connect(callback)
end

-- =========================================================
-- FITUR DELETE & UNDO
-- =========================================================
local history = {}
local deleting = true

local DeleteUndoContainer = Instance.new("Frame")
DeleteUndoContainer.Parent = ButtonContainer
DeleteUndoContainer.BackgroundColor3 = Color3.fromRGB(35, 35, 48)
DeleteUndoContainer.Size = UDim2.new(1, 0, 0, 115)
Instance.new("UICorner", DeleteUndoContainer).CornerRadius = UDim.new(0, 8)

local DeleteUndoTitle = Instance.new("TextLabel")
DeleteUndoTitle.Parent = DeleteUndoContainer
DeleteUndoTitle.Size = UDim2.new(1, 0, 0, 25)
DeleteUndoTitle.BackgroundTransparency = 1
DeleteUndoTitle.Text = "🗑 Delete tools / Undo"
DeleteUndoTitle.TextColor3 = Color3.fromRGB(100, 255, 255)
DeleteUndoTitle.Font = Enum.Font.GothamBold
DeleteUndoTitle.TextSize = 14

local deleteToggle = Instance.new("TextButton")
deleteToggle.Parent = DeleteUndoContainer
deleteToggle.Size = UDim2.new(1, -20, 0, 35)
deleteToggle.Position = UDim2.new(0, 10, 0, 30)
deleteToggle.Text = "Delete: ON"
deleteToggle.BackgroundColor3 = Color3.fromRGB(50, 50, 50)
deleteToggle.TextColor3 = Color3.fromRGB(255, 255, 255)
deleteToggle.Font = Enum.Font.Gotham
deleteToggle.TextSize = 13
Instance.new("UICorner", deleteToggle).CornerRadius = UDim.new(0, 6)

local undoBtn = Instance.new("TextButton")
undoBtn.Parent = DeleteUndoContainer
undoBtn.Size = UDim2.new(1, -20, 0, 35)
undoBtn.Position = UDim2.new(0, 10, 0, 72)
undoBtn.Text = "Undo Delete"
undoBtn.BackgroundColor3 = Color3.fromRGB(70, 70, 70)
undoBtn.TextColor3 = Color3.fromRGB(255, 255, 255)
undoBtn.Font = Enum.Font.Gotham
undoBtn.TextSize = 13
Instance.new("UICorner", undoBtn).CornerRadius = UDim.new(0, 6)

deleteToggle.MouseButton1Click:Connect(function()
    deleting = not deleting
    deleteToggle.Text = "Delete: " .. (deleting and "ON" or "OFF")
    deleteToggle.BackgroundColor3 = deleting and Color3.fromRGB(50, 50, 50) or Color3.fromRGB(80, 20, 20)
end)

Mouse.Button1Down:Connect(function()
    if not deleting then return end
    local target = Mouse.Target
    if target and target:IsA("BasePart") and not target:IsDescendantOf(LocalPlayer.Character) then
        local clone = target:Clone()
        local props = {
            Parent = target.Parent,
            Material = target.Material,
            Color = target.Color,
            Size = target.Size,
            CFrame = target.CFrame,
            Anchored = target.Anchored,
            Transparency = target.Transparency,
            CanCollide = target.CanCollide,
            Name = target.Name
        }
        table.insert(history, {props = props, clone = clone})
        target:Destroy()
    end
end)

undoBtn.MouseButton1Click:Connect(function()
    if #history == 0 then return end
    local data = table.remove(history)
    local newPart = data.clone:Clone()
    for prop, val in pairs(data.props) do
        newPart[prop] = val
    end
    newPart.Parent = data.props.Parent
end)

-- MOUSE LOCK / SHIFTLOCK CUSTOM UI
local IsItOn = false
local MouseLockContainer = Instance.new("Frame")
MouseLockContainer.Parent = ButtonContainer
MouseLockContainer.BackgroundColor3 = Color3.fromRGB(35, 35, 48)
MouseLockContainer.Size = UDim2.new(1, 0, 0, 65)
Instance.new("UICorner", MouseLockContainer).CornerRadius = UDim.new(0, 8)

local MouseLockButton = Instance.new("TextButton")
MouseLockButton.Parent = MouseLockContainer
MouseLockButton.BackgroundColor3 = Color3.fromRGB(0, 170, 255)
MouseLockButton.Position = UDim2.new(0, 10, 0, 12)
MouseLockButton.Size = UDim2.new(1, -20, 0, 40)
MouseLockButton.Font = Enum.Font.GothamBold
MouseLockButton.Text = "🔒 MouseLock / ShiftLock"
MouseLockButton.TextColor3 = Color3.fromRGB(255, 255, 255)
MouseLockButton.TextSize = 13
Instance.new("UICorner", MouseLockButton).CornerRadius = UDim.new(0, 6)

local Crosshair = Instance.new("ImageLabel")
Crosshair.Name = "Crosshair"
Crosshair.Parent = ScreenGui
Crosshair.Size = UDim2.new(0, 30, 0, 30)
Crosshair.Position = UDim2.new(0.5, 0, 0.45, 0)
Crosshair.AnchorPoint = Vector2.new(0.5, 0.5)
Crosshair.BackgroundTransparency = 1
Crosshair.Image = 'rbxassetid://85514680408407'
Crosshair.Visible = false
Crosshair.ZIndex = 10

RunService:BindToRenderStep('SmoothTrans', Enum.RenderPriority.Camera.Value + 1, function()
    if IsItOn ~= true then return end
    if not workspace.CurrentCamera then return end
    if ((workspace.CurrentCamera.CFrame.Position - workspace.CurrentCamera.Focus.Position).Magnitude) < .6 then
        Crosshair.Visible = false 
    else
        workspace.CurrentCamera.Focus = (workspace.CurrentCamera.CFrame * CFrame.new(1.7,0,0)) * CFrame.new(0,0,-((workspace.CurrentCamera.Focus.Position - workspace.CurrentCamera.CFrame.Position).Magnitude))
        workspace.CurrentCamera.CFrame = workspace.CurrentCamera.CFrame * CFrame.new(1.7,0,0)
        Crosshair.Visible = true
    end 
end)

MouseLockButton.MouseButton1Click:Connect(function()
    IsItOn = not IsItOn
    if IsItOn == true then
        UserGameSettings.RotationType = Enum.RotationType.CameraRelative
        MouseLockButton.BackgroundColor3 = Color3.fromRGB(0, 255, 128)
    else
        UserGameSettings.RotationType = Enum.RotationType.MovementRelative
        MouseLockButton.BackgroundColor3 = Color3.fromRGB(0, 170, 255)
        Crosshair.Visible = false
    end 
end)

-- INSTANT PROXIMITY PROMPT
local instantPromptEnabled = false
local promptConnection = nil

local function setInstant(prompt)
    prompt.HoldDuration = 0
    prompt.RequiresLineOfSight = false
end

local InstantContainer = Instance.new("Frame")
InstantContainer.Parent = ButtonContainer
InstantContainer.BackgroundColor3 = Color3.fromRGB(35, 35, 48)
InstantContainer.Size = UDim2.new(1, 0, 0, 65)
Instance.new("UICorner", InstantContainer).CornerRadius = UDim.new(0, 8)

local InstantButton = Instance.new("TextButton")
InstantButton.Parent = InstantContainer
InstantButton.BackgroundColor3 = Color3.fromRGB(50, 50, 50)
InstantButton.Position = UDim2.new(0, 10, 0, 12)
InstantButton.Size = UDim2.new(1, -20, 0, 40)
InstantButton.Font = Enum.Font.GothamBold
InstantButton.Text = "⚡ Enable Instant Prompt"
InstantButton.TextColor3 = Color3.fromRGB(255, 255, 255)
InstantButton.TextSize = 13
Instance.new("UICorner", InstantButton).CornerRadius = UDim.new(0, 6)

InstantButton.MouseButton1Click:Connect(function()
    instantPromptEnabled = not instantPromptEnabled
    if instantPromptEnabled then
        InstantButton.Text = "⚡ Disable Instant Prompt"
        InstantButton.BackgroundColor3 = Color3.fromRGB(0, 204, 102)
        for _, prompt in ipairs(game:GetDescendants()) do
            if prompt:IsA("ProximityPrompt") then
                setInstant(prompt)
            end
        end
        promptConnection = game.DescendantAdded:Connect(function(obj)
            if obj:IsA("ProximityPrompt") then
                setInstant(obj)
            end
        end)
    else
        InstantButton.Text = "⚡ Enable Instant Prompt"
        InstantButton.BackgroundColor3 = Color3.fromRGB(50, 50, 50)
        if promptConnection then
            promptConnection:Disconnect()
            promptConnection = nil
        end
    end
end)

-- FITUR LAINNYA
local airwalkActive = false
local airwalkPart = nil
local noclipActive = false
local espActive = false
local espNameActive = false
local espNPCActive = false
local tpToolInstance = nil
local fullbrightActive = false
local fullbrightConn = nil

RunService.RenderStepped:Connect(function()
    local char = LocalPlayer.Character
    if airwalkActive and char and char:FindFirstChild("HumanoidRootPart") then
        local rootPart = char.HumanoidRootPart
        if not airwalkPart or not airwalkPart.Parent then
            airwalkPart = Instance.new("Part")
            airwalkPart.Size = Vector3.new(3, 1, 3)
            airwalkPart.Transparency = 1
            airwalkPart.Anchored = true
            airwalkPart.CanCollide = true
            airwalkPart.Parent = workspace
        end
        airwalkPart.Position = rootPart.Position - Vector3.new(0, 3.5, 0)
    else
        if airwalkPart then
            airwalkPart:Destroy()
            airwalkPart = nil
        end
    end
end)

RunService.Stepped:Connect(function()
    local char = LocalPlayer.Character
    if noclipActive and char then
        for _, part in pairs(char:GetDescendants()) do
            if part:IsA("BasePart") then
                part.CanCollide = false
            end
        end
    end
end)

local function toggleFullbright(state)
    fullbrightActive = state
    if fullbrightActive then
        Lighting.Brightness = 2
        Lighting.ClockTime = 14
        Lighting.GlobalShadows = false
        Lighting.OutdoorAmbient = Color3.fromRGB(255, 255, 255)
        Lighting.Ambient = Color3.fromRGB(255, 255, 255)
        
        fullbrightConn = RunService.RenderStepped:Connect(function()
            Lighting.Brightness = 2
            Lighting.ClockTime = 14
            Lighting.GlobalShadows = false
            Lighting.OutdoorAmbient = Color3.fromRGB(255, 255, 255)
            Lighting.Ambient = Color3.fromRGB(255, 255, 255)
        end)
    else
        if fullbrightConn then
            fullbrightConn:Disconnect()
            fullbrightConn = nil
        end
        Lighting.Brightness = 1
        Lighting.GlobalShadows = true
        Lighting.OutdoorAmbient = Color3.fromRGB(127, 127, 127)
        Lighting.Ambient = Color3.fromRGB(0, 0, 0)
    end
end

local function applyESP(player)
    if player == LocalPlayer then return end
    
    local function addHighlight(char)
        if not char:FindFirstChild("IrwanESP") then
            local highlight = Instance.new("Highlight")
            highlight.Name = "IrwanESP"
            highlight.Adornee = char
            highlight.FillColor = Color3.fromRGB(255, 69, 0)
            highlight.FillTransparency = 0.5
            highlight.OutlineColor = Color3.fromRGB(255, 255, 255)
            highlight.OutlineTransparency = 0
            highlight.Parent = char
        end
    end
    
    local function addBillboard(char)
        local head = char:WaitForChild("Head", 5)
        if head and not head:FindFirstChild("IrwanNameESP") then
            local billboard = Instance.new("BillboardGui")
            billboard.Name = "IrwanNameESP"
            billboard.Adornee = head
            billboard.Size = UDim2.new(0, 100, 0, 40)
            billboard.StudsOffset = Vector3.new(0, 2.5, 0)
            billboard.AlwaysOnTop = true
            
            local textLabel = Instance.new("TextLabel")
            textLabel.Parent = billboard
            textLabel.BackgroundTransparency = 1
            textLabel.Size = UDim2.new(1, 0, 1, 0)
            textLabel.Font = Enum.Font.GothamBold
            textLabel.Text = player.Name
            textLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
            textLabel.TextSize = 14
            textLabel.TextStrokeTransparency = 0
            textLabel.TextStrokeColor3 = Color3.fromRGB(0, 0, 0)
            
            billboard.Parent = head
        end
    end
    
    player.CharacterAdded:Connect(function(char)
        char:WaitForChild("HumanoidRootPart")
        if espActive then addHighlight(char) end
        if espNameActive then addBillboard(char) end
    end)
    
    if player.Character then
        if espActive then addHighlight(player.Character) end
        if espNameActive then addBillboard(player.Character) end
    end
end

for _, p in pairs(Players:GetPlayers()) do
    applyESP(p)
end
Players.PlayerAdded:Connect(applyESP)

local function toggleESP(state)
    espActive = state
    for _, p in pairs(Players:GetPlayers()) do
        if p ~= LocalPlayer and p.Character then
            local hl = p.Character:FindFirstChild("IrwanESP")
            if espActive then
                if not hl then
                    local highlight = Instance.new("Highlight")
                    highlight.Name = "IrwanESP"
                    highlight.Adornee = p.Character
                    highlight.FillColor = Color3.fromRGB(255, 69, 0)
                    highlight.FillTransparency = 0.5
                    highlight.OutlineColor = Color3.fromRGB(255, 255, 255)
                    highlight.OutlineTransparency = 0
                    highlight.Parent = p.Character
                end
            else
                if hl then hl:Destroy() end
            end
        end
    end
end

local function toggleESPName(state)
    espNameActive = state
    for _, p in pairs(Players:GetPlayers()) do
        if p ~= LocalPlayer and p.Character then
            local head = p.Character:FindFirstChild("Head")
            if head then
                local bb = head:FindFirstChild("IrwanNameESP")
                if espNameActive then
                    if not bb then
                        local billboard = Instance.new("BillboardGui")
                        billboard.Name = "IrwanNameESP"
                        billboard.Adornee = head
                        billboard.Size = UDim2.new(0, 100, 0, 40)
                        billboard.StudsOffset = Vector3.new(0, 2.5, 0)
                        billboard.AlwaysOnTop = true
                        
                        local textLabel = Instance.new("TextLabel")
                        textLabel.Parent = billboard
                        textLabel.BackgroundTransparency = 1
                        textLabel.Size = UDim2.new(1, 0, 1, 0)
                        textLabel.Font = Enum.Font.GothamBold
                        textLabel.Text = p.Name
                        textLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
                        textLabel.TextSize = 14
                        textLabel.TextStrokeTransparency = 0
                        textLabel.TextStrokeColor3 = Color3.fromRGB(0, 0, 0)
                        
                        billboard.Parent = head
                    end
                else
                    if bb then bb:Destroy() end
                end
            end
        end
    end
end

local function toggleESPNPC(state)
    espNPCActive = state
    
    local function processModel(model)
        if model:IsA("Model") and model ~= LocalPlayer.Character then
            local humanoid = model:FindFirstChildOfClass("Humanoid")
            local head = model:FindFirstChild("Head") or model:FindFirstChild("HumanoidRootPart")
            
            if humanoid and head and not Players:GetPlayerFromCharacter(model) then
                local bb = head:FindFirstChild("IrwanNPCESP")
                if espNPCActive then
                    if not bb then
                        local billboard = Instance.new("BillboardGui")
                        billboard.Name = "IrwanNPCESP"
                        billboard.Adornee = head
                        billboard.Size = UDim2.new(0, 100, 0, 40)
                        billboard.StudsOffset = Vector3.new(0, 2.5, 0)
                        billboard.AlwaysOnTop = true
                        
                        local textLabel = Instance.new("TextLabel")
                        textLabel.Parent = billboard
                        textLabel.BackgroundTransparency = 1
                        textLabel.Size = UDim2.new(1, 0, 1, 0)
                        textLabel.Font = Enum.Font.GothamBold
                        textLabel.Text = "[NPC] " .. model.Name
                        textLabel.TextColor3 = Color3.fromRGB(0, 255, 128)
                        textLabel.TextSize = 13
                        textLabel.TextStrokeTransparency = 0
                        textLabel.TextStrokeColor3 = Color3.fromRGB(0, 0, 0)
                        
                        billboard.Parent = head
                    end
                else
                    if bb then bb:Destroy() end
                end
            end
        end
    end

    for _, obj in pairs(workspace:GetDescendants()) do
        processModel(obj)
    end
end

workspace.DescendantAdded:Connect(function(obj)
    if espNPCActive and obj:IsA("Model") then
        task.wait(0.5)
        local humanoid = obj:FindFirstChildOfClass("Humanoid")
        local head = obj:FindFirstChild("Head") or obj:FindFirstChild("HumanoidRootPart")
        if humanoid and head and not Players:GetPlayerFromCharacter(obj) then
            local bb = head:FindFirstChild("IrwanNPCESP")
            if not bb then
                local billboard = Instance.new("BillboardGui")
                billboard.Name = "IrwanNPCESP"
                billboard.Adornee = head
                billboard.Size = UDim2.new(0, 100, 0, 40)
                billboard.StudsOffset = Vector3.new(0, 2.5, 0)
                billboard.AlwaysOnTop = true
                
                local textLabel = Instance.new("TextLabel")
                textLabel.Parent = billboard
                textLabel.BackgroundTransparency = 1
                textLabel.Size = UDim2.new(1, 0, 1, 0)
                textLabel.Font = Enum.Font.GothamBold
                textLabel.Text = "[NPC] " .. obj.Name
                textLabel.TextColor3 = Color3.fromRGB(0, 255, 128)
                textLabel.TextSize = 13
                textLabel.TextStrokeTransparency = 0
                textLabel.TextStrokeColor3 = Color3.fromRGB(0, 0, 0)
                
                billboard.Parent = head
            end
        end
    end
end)

local function freezeNPC(targetName)
    targetName = string.lower(targetName)
    for _, obj in pairs(workspace:GetDescendants()) do
        if obj:IsA("Model") and not Players:GetPlayerFromCharacter(obj) then
            local humanoid = obj:FindFirstChildOfClass("Humanoid")
            local rootPart = obj:FindFirstChild("HumanoidRootPart") or obj:FindFirstChild("Head")
            if humanoid and rootPart and string.match(string.lower(obj.Name), targetName) then
                humanoid.WalkSpeed = 0
                humanoid.JumpPower = 0
                for _, part in pairs(obj:GetDescendants()) do
                    if part:IsA("BasePart") then part.Anchored = true end
                end
            end
        end
    end
end

local function unfreezeNPC(targetName)
    targetName = string.lower(targetName)
    for _, obj in pairs(workspace:GetDescendants()) do
        if obj:IsA("Model") and not Players:GetPlayerFromCharacter(obj) then
            local humanoid = obj:FindFirstChildOfClass("Humanoid")
            local rootPart = obj:FindFirstChild("HumanoidRootPart") or obj:FindFirstChild("Head")
            if humanoid and rootPart and string.match(string.lower(obj.Name), targetName) then
                humanoid.WalkSpeed = 16
                humanoid.JumpPower = 50
                for _, part in pairs(obj:GetDescendants()) do
                    if part:IsA("BasePart") then part.Anchored = false end
                end
            end
        end
    end
end

local function tpToNPC(targetName)
    local char = LocalPlayer.Character
    if not char or not char:FindFirstChild("HumanoidRootPart") then return end
    targetName = string.lower(targetName)
    local targetRoot = nil
    for _, obj in pairs(workspace:GetDescendants()) do
        if obj:IsA("Model") and not Players:GetPlayerFromCharacter(obj) then
            local humanoid = obj:FindFirstChildOfClass("Humanoid")
            local rootPart = obj:FindFirstChild("HumanoidRootPart") or obj:FindFirstChild("Head")
            if humanoid and rootPart and string.match(string.lower(obj.Name), targetName) then
                targetRoot = rootPart
                break
            end
        end
    end
    if targetRoot then
        char.HumanoidRootPart.CFrame = targetRoot.CFrame + Vector3.new(0, 3, 0)
    end
end

local function bringNPC(targetName)
    local char = LocalPlayer.Character
    if not char or not char:FindFirstChild("HumanoidRootPart") then return end
    local playerPos = char.HumanoidRootPart.CFrame
    targetName = string.lower(targetName)
    for _, obj in pairs(workspace:GetDescendants()) do
        if obj:IsA("Model") and not Players:GetPlayerFromCharacter(obj) then
            local humanoid = obj:FindFirstChildOfClass("Humanoid")
            local rootPart = obj:FindFirstChild("HumanoidRootPart") or obj:FindFirstChild("Head")
            if humanoid and rootPart and string.match(string.lower(obj.Name), targetName) then
                rootPart.CFrame = playerPos + Vector3.new(0, 3, -3)
            end
        end
    end
end

local function tpToPlayer(targetName)
    local char = LocalPlayer.Character
    if not char or not char:FindFirstChild("HumanoidRootPart") then return end
    targetName = string.lower(targetName)
    local targetPlayer = nil
    for _, p in pairs(Players:GetPlayers()) do
        if p ~= LocalPlayer and string.match(string.lower(p.Name), targetName) then
            targetPlayer = p
            break
        end
    end
    if targetPlayer and targetPlayer.Character and targetPlayer.Character:FindFirstChild("HumanoidRootPart") then
        char.HumanoidRootPart.CFrame = targetPlayer.Character.HumanoidRootPart.CFrame + Vector3.new(0, 3, 0)
    end
end

local function serverHop()
    local servers = {}
    local success, result = pcall(function()
        local url = "https://games.roblox.com/v1/games/" .. game.PlaceId .. "/servers/Public?sortOrder=Asc&limit=100"
        return HttpService:JSONDecode(game:HttpGet(url))
    end)
    if success and result and result.data then
        for _, server in ipairs(result.data) do
            if server.playing and server.maxPlayers and server.playing < server.maxPlayers and server.id ~= game.JobId then
                table.insert(servers, server.id)
            end
        end
        if #servers > 0 then
            TeleportService:TeleportToPlaceInstance(game.PlaceId, servers[math.random(1, #servers)], LocalPlayer)
        else
            TeleportService:Teleport(game.PlaceId, LocalPlayer)
        end
    else
        TeleportService:Teleport(game.PlaceId, LocalPlayer)
    end
end

local function boostFPS()
    settings().Rendering.QualityLevel = Enum.QualityLevel.Level01
    Lighting.GlobalShadows = false
    Lighting.FogEnd = 9e9
    for _, v in pairs(workspace:GetDescendants()) do
        if v:IsA("BasePart") then
            v.Material = Enum.Material.SmoothPlastic
            v.Reflectance = 0
        elseif v:IsA("Decal") or v:IsA("Texture") then
            v.Transparency = 1
        elseif v:IsA("ParticleEmitter") or v:IsA("Fire") or v:IsA("Smoke") or v:IsA("Sparkles") then
            v.Enabled = false
        end
    end
end

local function removeFog()
    Lighting.FogEnd = 9e9
    Lighting.FogStart = 9e9
    for _, v in pairs(Lighting:GetChildren()) do
        if v:IsA("Atmosphere") or v:IsA("Sky") then v:Destroy() end
    end
end

local function giveTPTool()
    if tpToolInstance and tpToolInstance.Parent then return end
    local tool = Instance.new("Tool")
    tool.Name = "🎯 TP Tool"
    tool.RequiresHandle = false
    tool.CanBeDropped = false
    tool.Activated:Connect(function()
        local char = LocalPlayer.Character
        local mouse = LocalPlayer:GetMouse()
        if char and char:FindFirstChild("HumanoidRootPart") and mouse.Target then
            char.HumanoidRootPart.CFrame = CFrame.new(mouse.Hit.Position + Vector3.new(0, 3, 0))
        end
    end)
    tool.Parent = LocalPlayer:WaitForChild("Backpack")
    tpToolInstance = tool
end

local function maxZoomCamera()
    LocalPlayer.CameraMaxZoomDistance = 999999
end

-- UI CUSTOM SPEED
local SpeedContainer = Instance.new("Frame")
SpeedContainer.Parent = ButtonContainer
SpeedContainer.BackgroundColor3 = Color3.fromRGB(35, 35, 48)
SpeedContainer.Size = UDim2.new(1, 0, 0, 85)
Instance.new("UICorner", SpeedContainer).CornerRadius = UDim.new(0, 8)

local SpeedBox = Instance.new("TextBox")
SpeedBox.Parent = SpeedContainer
SpeedBox.BackgroundColor3 = Color3.fromRGB(25, 25, 35)
SpeedBox.Position = UDim2.new(0, 10, 0, 10)
SpeedBox.Size = UDim2.new(1, -20, 0, 30)
SpeedBox.Font = Enum.Font.GothamMedium
SpeedBox.PlaceholderText = "Enter WalkSpeed (Max inf)..."
SpeedBox.Text = ""
SpeedBox.TextColor3 = Color3.fromRGB(255, 255, 255)
SpeedBox.PlaceholderColor3 = Color3.fromRGB(150, 150, 150)
SpeedBox.TextSize = 13
Instance.new("UICorner", SpeedBox).CornerRadius = UDim.new(0, 6)

local SpeedActionBtn = Instance.new("TextButton")
SpeedActionBtn.Parent = SpeedContainer
SpeedActionBtn.BackgroundColor3 = Color3.fromRGB(255, 140, 0)
SpeedActionBtn.Position = UDim2.new(0, 10, 0, 48)
SpeedActionBtn.Size = UDim2.new(1, -20, 0, 30)
SpeedActionBtn.Font = Enum.Font.GothamBold
SpeedActionBtn.Text = "⚡ Set WalkSpeed"
SpeedActionBtn.TextColor3 = Color3.fromRGB(255, 255, 255)
SpeedActionBtn.TextSize = 13
Instance.new("UICorner", SpeedActionBtn).CornerRadius = UDim.new(0, 6)

SpeedActionBtn.MouseButton1Click:Connect(function()
    local val = tonumber(SpeedBox.Text)
    if val then
        if val > 500 then val = 500 end
        local char = LocalPlayer.Character
        if char and char:FindFirstChild("Humanoid") then
            char.Humanoid.WalkSpeed = val
        end
    end
end)

-- UI CUSTOM JUMP
local JumpContainer = Instance.new("Frame")
JumpContainer.Parent = ButtonContainer
JumpContainer.BackgroundColor3 = Color3.fromRGB(35, 35, 48)
JumpContainer.Size = UDim2.new(1, 0, 0, 85)
Instance.new("UICorner", JumpContainer).CornerRadius = UDim.new(0, 8)

local JumpBox = Instance.new("TextBox")
JumpBox.Parent = JumpContainer
JumpBox.BackgroundColor3 = Color3.fromRGB(25, 25, 35)
JumpBox.Position = UDim2.new(0, 10, 0, 10)
JumpBox.Size = UDim2.new(1, -20, 0, 30)
JumpBox.Font = Enum.Font.GothamMedium
JumpBox.PlaceholderText = "Enter JumpPower (Max inf)..."
JumpBox.Text = ""
JumpBox.TextColor3 = Color3.fromRGB(255, 255, 255)
JumpBox.PlaceholderColor3 = Color3.fromRGB(150, 150, 150)
JumpBox.TextSize = 13
Instance.new("UICorner", JumpBox).CornerRadius = UDim.new(0, 6)

local JumpActionBtn = Instance.new("TextButton")
JumpActionBtn.Parent = JumpContainer
JumpActionBtn.BackgroundColor3 = Color3.fromRGB(0, 180, 216)
JumpActionBtn.Position = UDim2.new(0, 10, 0, 48)
JumpActionBtn.Size = UDim2.new(1, -20, 0, 30)
JumpActionBtn.Font = Enum.Font.GothamBold
JumpActionBtn.Text = "🦘 Set JumpPower"
JumpActionBtn.TextColor3 = Color3.fromRGB(255, 255, 255)
JumpActionBtn.TextSize = 13
Instance.new("UICorner", JumpActionBtn).CornerRadius = UDim.new(0, 6)

JumpActionBtn.MouseButton1Click:Connect(function()
    local val = tonumber(JumpBox.Text)
    if val then
        if val > 500 then val = 500 end
        local char = LocalPlayer.Character
        if char and char:FindFirstChild("Humanoid") then
            char.Humanoid.UseJumpPower = true
            char.Humanoid.JumpPower = val
        end
    end
end)

createButton("AirwalkBtn", "☁️ Airwalk", function() airwalkActive = not airwalkActive end)
createButton("NoclipBtn", "🧱Noclip", function() noclipActive = not noclipActive end)
createButton("FullbrightBtn", "✴️Fullbright", function() toggleFullbright(not fullbrightActive) end)
createButton("ESPBtn", "👤ESP Player", function() toggleESP(not espActive) end)
createButton("ESPNameBtn", "🏷️ESP Player Name", function() toggleESPName(not espNameActive) end)
createButton("ESPNPCBtn", "🤖ESP NPC Name", function() toggleESPNPC(not espNPCActive) end)

-- UI TP Player
local TPPlayerContainer = Instance.new("Frame")
TPPlayerContainer.Parent = ButtonContainer
TPPlayerContainer.BackgroundColor3 = Color3.fromRGB(35, 35, 48)
TPPlayerContainer.Size = UDim2.new(1, 0, 0, 85)
Instance.new("UICorner", TPPlayerContainer).CornerRadius = UDim.new(0, 8)

local TPPlayerBox = Instance.new("TextBox")
TPPlayerBox.Parent = TPPlayerContainer
TPPlayerBox.BackgroundColor3 = Color3.fromRGB(25, 25, 35)
TPPlayerBox.Position = UDim2.new(0, 10, 0, 10)
TPPlayerBox.Size = UDim2.new(1, -20, 0, 30)
TPPlayerBox.Font = Enum.Font.GothamMedium
TPPlayerBox.PlaceholderText = "Enter Player Name to TP..."
TPPlayerBox.Text = ""
TPPlayerBox.TextColor3 = Color3.fromRGB(255, 255, 255)
TPPlayerBox.PlaceholderColor3 = Color3.fromRGB(150, 150, 150)
TPPlayerBox.TextSize = 13
Instance.new("UICorner", TPPlayerBox).CornerRadius = UDim.new(0, 6)

local TPPlayerActionBtn = Instance.new("TextButton")
TPPlayerActionBtn.Parent = TPPlayerContainer
TPPlayerActionBtn.BackgroundColor3 = Color3.fromRGB(255, 140, 0)
TPPlayerActionBtn.Position = UDim2.new(0, 10, 0, 48)
TPPlayerActionBtn.Size = UDim2.new(1, -20, 0, 30)
TPPlayerActionBtn.Font = Enum.Font.GothamBold
TPPlayerActionBtn.Text = "👤 Teleport to Player"
TPPlayerActionBtn.TextColor3 = Color3.fromRGB(255, 255, 255)
TPPlayerActionBtn.TextSize = 13
Instance.new("UICorner", TPPlayerActionBtn).CornerRadius = UDim.new(0, 6)

TPPlayerActionBtn.MouseButton1Click:Connect(function()
    if TPPlayerBox.Text ~= "" then tpToPlayer(TPPlayerBox.Text) end
end)

-- UI TP NPC
local TPNPCContainer = Instance.new("Frame")
TPNPCContainer.Parent = ButtonContainer
TPNPCContainer.BackgroundColor3 = Color3.fromRGB(35, 35, 48)
TPNPCContainer.Size = UDim2.new(1, 0, 0, 85)
Instance.new("UICorner", TPNPCContainer).CornerRadius = UDim.new(0, 8)

local TPNPCBox = Instance.new("TextBox")
TPNPCBox.Parent = TPNPCContainer
TPNPCBox.BackgroundColor3 = Color3.fromRGB(25, 25, 35)
TPNPCBox.Position = UDim2.new(0, 10, 0, 10)
TPNPCBox.Size = UDim2.new(1, -20, 0, 30)
TPNPCBox.Font = Enum.Font.GothamMedium
TPNPCBox.PlaceholderText = "Enter NPC Name to TP..."
TPNPCBox.Text = ""
TPNPCBox.TextColor3 = Color3.fromRGB(255, 255, 255)
TPNPCBox.PlaceholderColor3 = Color3.fromRGB(150, 150, 150)
TPNPCBox.TextSize = 13
Instance.new("UICorner", TPNPCBox).CornerRadius = UDim.new(0, 6)

local TPNPCActionBtn = Instance.new("TextButton")
TPNPCActionBtn.Parent = TPNPCContainer
TPNPCActionBtn.BackgroundColor3 = Color3.fromRGB(0, 180, 216)
TPNPCActionBtn.Position = UDim2.new(0, 10, 0, 48)
TPNPCActionBtn.Size = UDim2.new(1, -20, 0, 30)
TPNPCActionBtn.Font = Enum.Font.GothamBold
TPNPCActionBtn.Text = "🤖 Teleport to NPC"
TPNPCActionBtn.TextColor3 = Color3.fromRGB(255, 255, 255)
TPNPCActionBtn.TextSize = 13
Instance.new("UICorner", TPNPCActionBtn).CornerRadius = UDim.new(0, 6)

TPNPCActionBtn.MouseButton1Click:Connect(function()
    if TPNPCBox.Text ~= "" then tpToNPC(TPNPCBox.Text) end
end)

-- UI Freeze NPC
local FreezeContainer = Instance.new("Frame")
FreezeContainer.Parent = ButtonContainer
FreezeContainer.BackgroundColor3 = Color3.fromRGB(35, 35, 48)
FreezeContainer.Size = UDim2.new(1, 0, 0, 85)
Instance.new("UICorner", FreezeContainer).CornerRadius = UDim.new(0, 8)

local FreezeBox = Instance.new("TextBox")
FreezeBox.Parent = FreezeContainer
FreezeBox.BackgroundColor3 = Color3.fromRGB(25, 25, 35)
FreezeBox.Position = UDim2.new(0, 10, 0, 10)
FreezeBox.Size = UDim2.new(1, -20, 0, 30)
FreezeBox.Font = Enum.Font.GothamMedium
FreezeBox.PlaceholderText = "Enter NPC Name to Freeze..."
FreezeBox.Text = ""
FreezeBox.TextColor3 = Color3.fromRGB(255, 255, 255)
FreezeBox.PlaceholderColor3 = Color3.fromRGB(150, 150, 150)
FreezeBox.TextSize = 13
Instance.new("UICorner", FreezeBox).CornerRadius = UDim.new(0, 6)

local FreezeActionBtn = Instance.new("TextButton")
FreezeActionBtn.Parent = FreezeContainer
FreezeActionBtn.BackgroundColor3 = Color3.fromRGB(0, 162, 255)
FreezeActionBtn.Position = UDim2.new(0, 10, 0, 48)
FreezeActionBtn.Size = UDim2.new(1, -20, 0, 30)
FreezeActionBtn.Font = Enum.Font.GothamBold
FreezeActionBtn.Text = "❄️ Freeze NPC"
FreezeActionBtn.TextColor3 = Color3.fromRGB(255, 255, 255)
FreezeActionBtn.TextSize = 13
Instance.new("UICorner", FreezeActionBtn).CornerRadius = UDim.new(0, 6)

FreezeActionBtn.MouseButton1Click:Connect(function()
    if FreezeBox.Text ~= "" then freezeNPC(FreezeBox.Text) end
end)

-- UI Unfreeze NPC
local UnfreezeContainer = Instance.new("Frame")
UnfreezeContainer.Parent = ButtonContainer
UnfreezeContainer.BackgroundColor3 = Color3.fromRGB(35, 35, 48)
UnfreezeContainer.Size = UDim2.new(1, 0, 0, 85)
Instance.new("UICorner", UnfreezeContainer).CornerRadius = UDim.new(0, 8)

local UnfreezeBox = Instance.new("TextBox")
UnfreezeBox.Parent = UnfreezeContainer
UnfreezeBox.BackgroundColor3 = Color3.fromRGB(25, 25, 35)
UnfreezeBox.Position = UDim2.new(0, 10, 0, 10)
UnfreezeBox.Size = UDim2.new(1, -20, 0, 30)
UnfreezeBox.Font = Enum.Font.GothamMedium
UnfreezeBox.PlaceholderText = "Enter NPC Name to Unfreeze..."
UnfreezeBox.Text = ""
UnfreezeBox.TextColor3 = Color3.fromRGB(255, 255, 255)
UnfreezeBox.PlaceholderColor3 = Color3.fromRGB(150, 150, 150)
UnfreezeBox.TextSize = 13
Instance.new("UICorner", UnfreezeBox).CornerRadius = UDim.new(0, 6)

local UnfreezeActionBtn = Instance.new("TextButton")
UnfreezeActionBtn.Parent = UnfreezeContainer
UnfreezeActionBtn.BackgroundColor3 = Color3.fromRGB(0, 204, 102)
UnfreezeActionBtn.Position = UDim2.new(0, 10, 0, 48)
UnfreezeActionBtn.Size = UDim2.new(1, -20, 0, 30)
UnfreezeActionBtn.Font = Enum.Font.GothamBold
UnfreezeActionBtn.Text = "☀️ Unfreeze NPC"
UnfreezeActionBtn.TextColor3 = Color3.fromRGB(255, 255, 255)
UnfreezeActionBtn.TextSize = 13
Instance.new("UICorner", UnfreezeActionBtn).CornerRadius = UDim.new(0, 6)

UnfreezeActionBtn.MouseButton1Click:Connect(function()
    if UnfreezeBox.Text ~= "" then unfreezeNPC(UnfreezeBox.Text) end
end)

-- UI Bring NPC
local BringContainer = Instance.new("Frame")
BringContainer.Parent = ButtonContainer
BringContainer.BackgroundColor3 = Color3.fromRGB(35, 35, 48)
BringContainer.Size = UDim2.new(1, 0, 0, 85)
Instance.new("UICorner", BringContainer).CornerRadius = UDim.new(0, 8)

local BringBox = Instance.new("TextBox")
BringBox.Parent = BringContainer
BringBox.BackgroundColor3 = Color3.fromRGB(25, 25, 35)
BringBox.Position = UDim2.new(0, 10, 0, 10)
BringBox.Size = UDim2.new(1, -20, 0, 30)
BringBox.Font = Enum.Font.GothamMedium
BringBox.PlaceholderText = "Enter NPC Name to Bring..."
BringBox.Text = ""
BringBox.TextColor3 = Color3.fromRGB(255, 255, 255)
BringBox.PlaceholderColor3 = Color3.fromRGB(150, 150, 150)
BringBox.TextSize = 13
Instance.new("UICorner", BringBox).CornerRadius = UDim.new(0, 6)

local BringActionBtn = Instance.new("TextButton")
BringActionBtn.Parent = BringContainer
BringActionBtn.BackgroundColor3 = Color3.fromRGB(204, 0, 204)
BringActionBtn.Position = UDim2.new(0, 10, 0, 48)
BringActionBtn.Size = UDim2.new(1, -20, 0, 30)
BringActionBtn.Font = Enum.Font.GothamBold
BringActionBtn.Text = "🧲 Bring NPC Here"
BringActionBtn.TextColor3 = Color3.fromRGB(255, 255, 255)
BringActionBtn.TextSize = 13
Instance.new("UICorner", BringActionBtn).CornerRadius = UDim.new(0, 6)

BringActionBtn.MouseButton1Click:Connect(function()
    if BringBox.Text ~= "" then bringNPC(BringBox.Text) end
end)

createButton("InfiniteYieldBtn", "⚙️Infinite Yield Admin", function()
    pcall(function() loadstring(game:HttpGet('https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source'))() end)
end)

-- TOMBOL ANTIFLING INTEGRATED
createButton("AntiFlingBtn", "🛡️Anti-Fling Script", function()
    pcall(function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/sytcal/antifling/main/9999"))()
    end)
end)

-- TOMBOL INVISIBLE SCRIPT
createButton("InvisibleBtn", "👻 Invisible", function()
    pcall(function()
        loadstring(game:HttpGet("https://pastebin.com/raw/a76SWZ3V"))()
    end)
end)

-- TOMBOL F3X INTEGRATED
createButton("F3XBtn", "🛠️ Give F3X", function()
    pcall(function()
        loadstring(game:GetObjects("rbxassetid://6695644299")[1].Source)()
    end)
end)

-- TOMBOL MOVE ROBLOX INTEGRATED
createButton("MoveRobloxBtn", "🎬Move Roblox", function()
    pcall(function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/panchooo677/Nynyn-/refs/heads/main/README.md"))()
    end)
end)

-- TOMBOL FREE EMOTE INTEGRATED
createButton("FreeEmoteBtn", "💃Free Emote", function()
    pcall(function()
        loadstring(game:HttpGet("https://rawscripts.net/raw/Universal-Script-7yd7-I-Emote-Script-48024"))()
    end)
end)

-- TOMBOL TIGERX 3.5 INTEGRATED
createButton("TigerXBtn", "🐯TigerX 3.5", function()
    pcall(function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/balintTheDevX/Tiger-X-V3/main/Tiger%20X%20V3.5%20Fixed"))()
    end)
end)

-- TOMBOL SECURE DEX & REMOTE SPY INTEGRATED
createButton("SecureDexBtn", "💻dex", function()
    pcall(function()
        loadstring(game:HttpGet("https://rawscripts.net/raw/Universal-Script-SECURE-DEX-AND-REMOTE-SPY-205256"))()
    end)
end)

-- TAMBAHAN SCRIPT BARU DARI GITHUB (PANCHOOO677)
createButton("CustomScriptBtn", "⭐Extra Scriptblox", function()
    pcall(function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/panchooo677/Btbthy/refs/heads/main/README.md"))()
    end)
end)

-- TOMBOL QUANTUM ONYX (NO KEY / AUTO FARM)
createButton("QuantumOnyxBtn", "💎blox fruit Quantum Onyx", function()
    pcall(function()
        loadstring(game:HttpGet("https://rawscripts.net/raw/Universal-Script-Quantum-Onyx-Project-32118"))()
    end)
end)

-- TOMBOL KRIM SCRIPT
createButton("KrimScriptBtn", "☠️kill NPC", function()
    pcall(function()
        loadstring(game:HttpGet("https://pastefy.app/lXaYlxWd/raw"))()
    end)
end)

-- TOMBOL FLY ADMIN INTEGRATED
createButton("FlyAdminBtn", "✈️Fly Admin Script", function()
    pcall(function()
        loadstring(game:HttpGet("https://rawscripts.net/raw/Universal-Script-Fake-Admin-Fly-Script-143792"))()
    end)
end)

-- TOMBOL SERVERPRO INTEGRATED
createButton("ServerProBtn", "👾(Server Browser)", function()
    pcall(function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/RealBatu20/AI-Scripts-2025/refs/heads/main/ServerBrowserImproved.lua"))()
    end)
end)

createButton("ServerHopBtn", "🌐 Server Hop", function() serverHop() end)
createButton("FPSBoostBtn", "🚀 FPS Booster", function() boostFPS() end)
createButton("NoFogBtn", "🌫️ Remove Fog", function() removeFog() end)
createButton("TPToolBtn", "🎯 Give TP Tool (Click TP)", function() giveTPTool() end)
createButton("MaxZoomBtn", "🔍 Max Camera Zoom", function() maxZoomCamera() end)
createButton("ResetBtn", "🔄 Reset Character", function()
    airwalkActive = false
    noclipActive = false
    toggleFullbright(false)
    toggleESP(false)
    toggleESPName(false)
    toggleESPNPC(false)
    if tpToolInstance then tpToolInstance:Destroy() tpToolInstance = nil end
    if LocalPlayer.Character and LocalPlayer.Character:FindFirstChild("Humanoid") then
        LocalPlayer.Character.Humanoid.Health = 0
    end
end)
