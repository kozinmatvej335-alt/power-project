[12.03.2026 23:35] #𝓟𝓞𝓦𝓔𝓡𝓜𝓞𝓓 POWERLAY ᛜᛄᛄᛋᛪⰓᛁᚤᚳ: <!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<title>POWER PROJECT</title>

<style>

body{
margin:0;
background:black;
color:white;
font-family:Arial;
text-align:center;
}

.title{
font-size:70px;
margin-top:20px;
animation:move 7s linear infinite;
text-shadow:0 0 20px white;
}

@keyframes move{
0%{transform:translateX(-100%)}
100%{transform:translateX(100%)}
}

.menu button{
background:white;
color:black;
border:none;
padding:10px 20px;
margin:5px;
border-radius:8px;
cursor:pointer;
}

.search input{
padding:10px;
width:250px;
border-radius:8px;
border:none;
}

.section{
display:none;
width:85%;
margin:auto;
margin-top:30px;
}

.script{
background:#111;
padding:20px;
margin-top:20px;
border-radius:10px;
text-align:left;
}

pre{
background:#000;
padding:15px;
border-radius:8px;
color:#00ff9d;
overflow:auto;
}

.copy{
background:white;
color:black;
border:none;
padding:6px 14px;
border-radius:6px;
cursor:pointer;
margin-top:10px;
}

footer{
margin-top:40px;
padding:20px;
}

#creator{
margin-top:10px;
font-size:20px;
}

</style>
</head>

<body>

<div class="title">POWER PROJECT</div>

<div id="creator"></div>

<div class="menu">

<button onclick="show('gui')">GUI</button>
<button onclick="show('player')">Player</button>
<button onclick="show('systems')">Systems</button>
<button onclick="show('effects')">Effects</button>
<button onclick="show('admin')">Admin</button>

</div>

<div class="search">
<input id="search" placeholder="Search script..." onkeyup="searchScript()">
</div>

<!-- GUI -->

<div id="gui" class="section">

<div class="script">
<h2>GUI Menu</h2>
<pre id="g1">
local gui = Instance.new("ScreenGui")
gui.Parent = game.Players.LocalPlayer.PlayerGui
</pre>
<button class="copy" onclick="copy('g1')">Copy Script</button>
</div>

<div class="script">
<h2>Create Frame</h2>
<pre id="g2">
local frame = Instance.new("Frame")
frame.Size = UDim2.new(0,300,0,200)
frame.Parent = gui
</pre>
<button class="copy" onclick="copy('g2')">Copy Script</button>
</div>

<div class="script">
<h2>Toggle GUI</h2>
<pre id="g3">
frame.Visible = not frame.Visible
</pre>
<button class="copy" onclick="copy('g3')">Copy Script</button>
</div>

</div>

<!-- PLAYER -->

<div id="player" class="section">

<div class="script">
<h2>Speed Boost</h2>
<pre id="p1">
game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = 40
</pre>
<button class="copy" onclick="copy('p1')">Copy Script</button>
</div>

<div class="script">
<h2>Jump Boost</h2>
<pre id="p2">
game.Players.LocalPlayer.Character.Humanoid.JumpPower = 100
</pre>
<button class="copy" onclick="copy('p2')">Copy Script</button>
</div>

<div class="script">
<h2>Reset Character</h2>
<pre id="p3">
game.Players.LocalPlayer:LoadCharacter()
</pre>
<button class="copy" onclick="copy('p3')">Copy Script</button>
</div>

<div class="script">
<h2>Teleport Player</h2>
<pre id="p4">
game.Players.LocalPlayer.Character:MoveTo(Vector3.new(0,50,0))
</pre>
<button class="copy" onclick="copy('p4')">Copy Script</button>
</div>

</div>

<!-- SYSTEMS -->

<div id="systems" class="section">

<div class="script">
<h2>Leaderstats Coins</h2>
<pre id="s1">
game.Players.PlayerAdded:Connect(function(player)

local stats = Instance.new("Folder")
stats.Name="leaderstats"
stats.Parent=player

local coins=Instance.new("IntValue")
coins.Name="Coins"
coins.Parent=stats

end)
</pre>
<button class="copy" onclick="copy('s1')">Copy Script</button>
</div>

<div class="script">
<h2>Coin Collect</h2>
<pre id="s2">
script.Parent.Touched:Connect(function(hit)

local player=game.Players:GetPlayerFromCharacter(hit.Parent)

if player then
player.leaderstats.Coins.Value += 1
script.Parent:Destroy()
end

end)
</pre>
<button class="copy" onclick="copy('s2')">Copy Script</button>
</div>

<div class="script">
<h2>Give Coins</h2>
<pre id="s3">
player.leaderstats.Coins.Value += 10
</pre>
<button class="copy" onclick="copy('s3')">Copy Script</button>
</div>

</div>

<!-- EFFECTS -->
[12.03.2026 23:35] #𝓟𝓞𝓦𝓔𝓡𝓜𝓞𝓓 POWERLAY ᛜᛄᛄᛋᛪⰓᛁᚤᚳ: <div id="effects" class="section"> <div class="script">
<h2>Day Night Cycle</h2>
<pre id="e1">
while true do
game.Lighting.ClockTime += 0.1
wait(1)
end
</pre>
<button class="copy" onclick="copy('e1')">Copy Script</button>
</div>

<div class="script">
<h2>Explosion Effect</h2>
<pre id="e2">
local explosion = Instance.new("Explosion")
explosion.Position = Vector3.new(0,10,0)
explosion.Parent = workspace
</pre>
<button class="copy" onclick="copy('e2')">Copy Script</button>
</div>

<div class="script">
<h2>Fire Effect</h2>
<pre id="e3">
local fire = Instance.new("Fire")
fire.Parent = workspace.Part
</pre>
<button class="copy" onclick="copy('e3')">Copy Script</button>
</div>

</div>

<!-- ADMIN -->

<div id="admin" class="section">

<div class="script">
<h2>Kick Player</h2>
<pre id="a1">
game.Players.PlayerAdded:Connect(function(player)

if player.Name == "BadPlayer" then
player:Kick("Removed by admin")
end

end)
</pre>
<button class="copy" onclick="copy('a1')">Copy Script</button>
</div>

<div class="script">
<h2>Give Admin Tool</h2>
<pre id="a2">
local tool = game.ServerStorage.AdminTool:Clone()
tool.Parent = player.Backpack
</pre>
<button class="copy" onclick="copy('a2')">Copy Script</button>
</div>

</div>

<footer>
Сотрудничество: @powerlayhub
</footer>

<script>

const creator=document.getElementById("creator")

setInterval(()=>{
creator.innerText="Создатель: POWERLAY"
setTimeout(()=>{creator.innerText=""},5000)
},10000)

function show(id){
document.querySelectorAll(".section").forEach(s=>{
s.style.display="none"
})
document.getElementById(id).style.display="block"
}

function copy(id){
let text=document.getElementById(id).innerText
navigator.clipboard.writeText(text)
alert("Script copied")
}

function searchScript(){
let input=document.getElementById("search").value.toLowerCase()
let scripts=document.querySelectorAll(".script")

scripts.forEach(s=>{
let text=s.innerText.toLowerCase()
if(text.includes(input)){
s.style.display="block"
}else{
s.style.display="none"
}
})
}

</script>

</body>
</html>
