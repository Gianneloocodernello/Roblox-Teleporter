# Roblox-Teleporter
A Lua code on how to create a teleporter

local teleporter = script.Parent
local destination = game.Workspace:FindFirstChild("Destination")

teleporter.Touched:Connect(function(hit)
    local character = hit.Parent
    local humanoid = character:FindFirstChildOfClass("Humanoid")
    if humanoid and destination then
        character:SetPrimaryPartCFrame(destination.CFrame)
    end
end)


(Name the part "Teleporter" then name the part to which the player would be teleported to "Destination")
