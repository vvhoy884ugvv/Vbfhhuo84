local Rayfield = loadstring(game:HttpGet('https://raw.githubusercontent.com/vvhoy884ugvv/hgcdghcvjh/refs/heads/main/sfvd.txt'))() 

local Window = Rayfield:CreateWindow({
   Name = "🐉Hydra.VIP (Fit Piece 2)🐉",
   LoadingTitle = "Made By HydraX",
   LoadingSubtitle = "By HydraX",
   ConfigurationSaving = {
      Enabled = true,
      FolderName = nil,
      FileName = "HydraVIP"
   },
   Discord = {
      Enabled = true,
      Invite = "dvdge._",
      RememberJoins = true
   },
   BackgroundColor = Color3.fromRGB(255, 255, 255),
   TextColor = Color3.fromRGB(0, 0, 0)
})

Rayfield:Notify({
   Title = "🐉Hydra.VIP (Fit Piece 2)🐉 INJECTED",
   Content = "Thank you so much for using my script!",
   Duration = 6.5,
   Image = 448362458,
   Actions = {
      Ignore = {
         Name = "Close",
         Callback = function()
         print("Notification closed")
      end
   },
},
})

-- قسم Special
local SpecialTab = Window:CreateTab("🐉Special", 448362458)
local SpecialSection = SpecialTab:CreateSection("Special")

SpecialTab:CreateButton({
   Name = "CidV2",
   Callback = function()
      local args = {
         [1] = "CidV2"
      }
      game:GetService("ReplicatedStorage").Remotes2.Inventory:FireServer(unpack(args))
   end
})

SpecialTab:CreateButton({
   Name = "Cid",
   Callback = function()
      local args = {
         [1] = "Cid"
      }
      game:GetService("ReplicatedStorage").Remotes2.Inventory:FireServer(unpack(args))
   end
})

-- قسم Inf
local InfTab = Window:CreateTab("🐉Inf", 448362458)
local InfSection = InfTab:CreateSection("Inf")

InfTab:CreateButton({
   Name = "Inf Money",
   Callback = function()
      local args = {
         [1] = "Buy",
         [2] = "",
         [3] = -999999999999999999
      }
      game:GetService("ReplicatedStorage").Shop:FireServer(unpack(args))
   end
})

-- قسم Swords
local SwordsTab = Window:CreateTab("🐉Swords", 448362458)
local SwordsSection = SwordsTab:CreateSection("Swords")

local swords = {
   {Name = "Axe", Command = "Axe"},
   {Name = "Spear", Command = "Spear"},
   {Name = "Claws", Command = "Claws"},
   {Name = "Bisento", Command = "Bisento"},
   {Name = "Asta", Command = "Asta"},
   {Name = "Rengoku", Command = "Rengoku"},
   {Name = "Aizen V1", Command = "Aizen"},
   {Name = "Aizen V2", Command = "AizenV2"},
   {Name = "Sung", Command = "Sung"}
}

for _, sword in pairs(swords) do
   SwordsTab:CreateButton({
      Name = sword.Name,
      Callback = function()
         local args = {
            [1] = sword.Command
         }
         game:GetService("ReplicatedStorage").Remotes2.Inventory:FireServer(unpack(args))
      end
   })
end

-- قسم Shop
local ShopTab = Window:CreateTab("🐉Shop", 448362458)
local ShopSection = ShopTab:CreateSection("Shop")

ShopTab:CreateButton({
   Name = "Yoru",
   Callback = function()
      local args = {
         [1] = "Yoru"
      }
      game:GetService("ReplicatedStorage").Remotes2.Inventory:FireServer(unpack(args))
   end
})
