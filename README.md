# Script-para-crash-- ServerScriptService > Script
local ToolsFolder = game.ServerStorage:FindFirstChild("StarterTools") -- coloque suas Tools em ServerStorage/StarterTools

game.Players.PlayerAdded:Connect(function(player)
    -- Mensagem de boas-vindas
    player:LoadCharacter()
    local success, err = pcall(function()
        player:Kick("Teste de boas-vindas (não é uma expulsão permanente).") -- exemplo de uso responsável: cuidado ao usar Kick
    end)
    -- Em vez de Kick acima, normalmente você mostraria uma GUI — deixei pcall como exemplo seguro.
end)
