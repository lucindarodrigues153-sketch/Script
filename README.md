local Player = game.Players.LocalPlayer
local HttpService = game:GetService("HttpService")

game.Players.PlayerAdded:Connect(function(player)
    player.CharacterAdded:Connect(function()
        wait(0.5)
        -- Remove the steal timer/gui
        local brainrotGui = player.PlayerGui:FindFirstChild("BrainrotGUI")
        if brainrotGui then
            brainrotGui:Destroy()
        end
    end)
end)
