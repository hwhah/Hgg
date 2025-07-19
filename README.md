local player = game.Players.LocalPlayer

-- Cria a interface
local screenGui = Instance.new("ScreenGui", player.PlayerGui)
screenGui.Name = "VotacaoMenu"

local frame = Instance.new("Frame", screenGui)
frame.Size = UDim2.new(0, 300, 0, 200)
frame.Position = UDim2.new(0.5, -150, 0.5, -100)
frame.BackgroundColor3 = Color3.fromRGB(40, 40, 40)
frame.AnchorPoint = Vector2.new(0.5, 0.5)

local title = Instance.new("TextLabel", frame)
title.Size = UDim2.new(1, 0, 0, 40)
title.Position = UDim2.new(0, 0, 0, 0)
title.Text = "VOTAÇÃO"
title.Font = Enum.Font.SourceSansBold
title.TextSize = 28
title.TextColor3 = Color3.new(1, 1, 1)
title.BackgroundTransparency = 1

local info = Instance.new("TextLabel", frame)
info.Size = UDim2.new(1, 0, 0, 30)
info.Position = UDim2.new(0, 0, 0, 45)
info.Text = "Participantes:"
info.Font = Enum.Font.SourceSans
info.TextSize = 20
info.TextColor3 = Color3.new(1, 1, 1)
info.BackgroundTransparency = 1

local participants = {player.Name, "Jogador2", "Jogador3"}
local votes = {}

for i, name in ipairs(participants
