-- 👑 PROJECT MASTERRLX – EMOTE GUI DELUXE (INTRO LOGO VERSION) 👑
-- Dibuat khusus untuk AnjaszRelaxz / MasterLeadRLX
-- Versi Final GitHub Release

local Players = game:GetService("Players")
local StarterGui = game:GetService("StarterGui")
local player = Players.LocalPlayer

-- 🌟 INTRO LOGO (ID: 106628403485337)
local ScreenGui = Instance.new("ScreenGui")
ScreenGui.Name = "MasterRLX_Intro"
ScreenGui.ResetOnSpawn = false
ScreenGui.Parent = player:WaitForChild("PlayerGui")

local Logo = Instance.new("ImageLabel")
Logo.Size = UDim2.new(1, 0, 1, 0)
Logo.BackgroundTransparency = 1
Logo.Image = "rbxassetid://106628403485337"
Logo.ImageTransparency = 1
Logo.Parent = ScreenGui

-- 🎬 Efek Fade In
for i = 1, 20 do
	Logo.ImageTransparency = 1 - (i / 20)
	task.wait(0.05)
end
task.wait(2.5)

-- 🎬 Efek Fade Out
for i = 1, 20 do
	Logo.ImageTransparency = i / 20
	task.wait(0.05)
end
ScreenGui:Destroy()

-- 🔗 LOAD SCRIPT UTAMA (DARI GIST KAMU)
loadstring(game:HttpGet("https://gist.githubusercontent.com/g4247921-cmd/a2c1f75feea2575fba0eb732c275ad17/raw/"))()

-- 💃 LOAD EMOTE GUI (PROJECT MASTERRLX)
loadstring(game:HttpGet("https://raw.githubusercontent.com/7yd7/Hub/refs/heads/Branch/GUIS/Emotes.lua"))()

-- ✅ NOTIFIKASI SELESAI
StarterGui:SetCore("SendNotification", {
	Title = "👑 Project MasterRLX",
	Text = "Intro selesai — semua sistem aktif!",
	Duration = 5
})
