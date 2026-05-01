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

/* hearts animation */
.heart {
    position: fixed;
    bottom: -10px;
    color: pink;
    animation: floatUp 5s linear infinite;
}
@keyframes floatUp {
    0% { transform: translateY(0); opacity: 1; }
    100% { transform: translateY(-100vh); opacity: 0; }
}

.container {
    margin-top: 100px;
}

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

<!-- 🎵 Background Music -->
<audio id="bgMusic" loop>
  <source src="music.mp3" type="audio/mpeg">
</audio>

<!-- ❤️ Hearts -->
<script>
setInterval(() => {
    let heart = document.createElement("div");
    heart.className = "heart";
    heart.innerHTML = "💖";
    heart.style.left = Math.random() * 100 + "vw";
    heart.style.fontSize = (Math.random() * 20 + 10) + "px";
    document.body.appendChild(heart);

    setTimeout(() => {
        heart.remove();
    }, 5000);
}, 300);
</script>

<!-- Screen 1 -->
<div class="container" id="screen1">
    <div class="to-name">To Afruza❣️❣️</div>
    <br>
    <button class="continue" onclick="nextScreen()">Continue ❤️</button>
</div>

<!-- Screen 2 -->
<div class="container" id="screen2" style="display:none;">
    <h2 id="message"></h2>
    <button class="continue" onclick="finalScreen()">Next 💌</button>
</div>

<!-- Screen 3 -->
<div class="container" id="screen3" style="display:none;">
    <h1>Hey ❤️</h1>
    <h2>Will you be mine? 💖</h2>

    <button class="yes" onclick="yesClick()">Yes 😍</button>
    <button class="no" onmouseover="moveButton()">No 😜</button>
</div>

<script>

// 👉 Apna message yaha likho
let text = "Jab se tum meri life me aayi ho... sab kuch special lagne laga ❤️ Tumhari smile, tumhari baatein... sab kuch mujhe pasand hai 💖 Main tumhe sach me pasand karta hu... kya tum meri banogi? 😍";

function nextScreen() {
    document.getElementById("screen1").style.display = "none";
    document.getElementById("screen2").style.display = "block";
    document.getElementById("bgMusic").play(); // music start
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

// typing effect
let i = 0;
function typeEffect() {
    if (i < text.length) {
        document.getElementById("message").innerHTML += text.charAt(i);
        i++;
        setTimeout(typeEffect, 40);
    }
}
</script>

</body>
</html>