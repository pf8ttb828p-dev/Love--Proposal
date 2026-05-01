index.html<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For Afruza ❤️</title>

<style>
body {
    margin: 0;
    font-family: Arial, sans-serif;
    background: linear-gradient(to right, #ff4b2b, #ff416c);
    color: white;
    text-align: center;
    overflow: hidden;
}

.container { margin-top: 100px; }

.to-name {
    font-size: 50px;
    font-weight: bold;
    animation: glow 1.5s infinite alternate;
}

@keyframes glow {
    from { text-shadow: 0 0 10px white; }
    to { text-shadow: 0 0 25px yellow; }
}

button {
    padding: 12px 25px;
    margin: 15px;
    font-size: 18px;
    border: none;
    border-radius: 8px;
    cursor: pointer;
}

.continue { background: #3b82f6; }
.yes { background: #22c55e; }
.no { background: #ef4444; position: absolute; }
</style>
</head>

<body>

<!-- 🎵 SOFT MUSIC -->
<audio id="bgMusic" loop>
  <source src="https://cdn.pixabay.com/download/audio/2022/03/15/audio_c8c8a73467.mp3?filename=soft-piano-ambient-110397.mp3" type="audio/mpeg">
</audio>

<div class="container" id="screen1">
    <div class="to-name">To Afruza❣️❣️</div>
    <br>
    <button class="continue" onclick="nextScreen()">Continue ❤️</button>
</div>

<div class="container" id="screen2" style="display:none;">
    <h2 id="message"></h2>
    <button class="continue" onclick="finalScreen()">Next 💌</button>
</div>

<div class="container" id="screen3" style="display:none;">
    <h2>WILL U BE MY FOR FOREVER AND EVER❤️‍🩹❤️‍🩹</h2>
    <button class="yes" onclick="yesClick()">Yes 😍</button>
    <button class="no" onmouseover="moveButton()">No 😜</button>
</div>

<script>

let text = `Out of all the constellations in the sky, you are the brightest star that caught my eyes 💫

Pehle tum bas achhi lagi…
phir dheere dheere tum meri aadat ban gayi 💖

Ab lagta hai din tab tak complete nahi hota jab tak tumse baat na ho…

Tumhari smile me ek alag hi sukoon hai 😊
Aur tumhari baaton me wo feeling hai jo mujhe har baar tumhare paas le aati hai ❤️

I really like you... and maybe more than that 💌`;

function nextScreen() {
    document.getElementById("screen1").style.display = "none";
    document.getElementById("screen2").style.display = "block";

    let music = document.getElementById("bgMusic");
    music.volume = 0.25;
    music.play();

    typeEffect();
}

function finalScreen() {
    document.getElementById("screen2").style.display = "none";
    document.getElementById("screen3").style.display = "block";
}

function yesClick() {
    document.body.innerHTML = "<h1 style='margin-top:100px;'>I love you Afruza ❤️😍</h1>";
}

function moveButton() {
    let btn = document.querySelector('.no');
    btn.style.top = Math.random() * window.innerHeight + "px";
    btn.style.left = Math.random() * window.innerWidth + "px";
}

let i = 0;
function typeEffect() {
    if (i < text.length) {
        document.getElementById("message").innerHTML += text.charAt(i);
        i++;
        setTimeout(typeEffect, 30);
    }
}

</script>

</body>
</html>