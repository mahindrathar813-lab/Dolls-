<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Teddy Day 💖</title>

<link href="https://fonts.googleapis.com/css2?family=Pacifico&family=Poppins:wght@300;500&display=swap" rel="stylesheet">

<style>
body {
    margin: 0;
    font-family: 'Poppins', sans-serif;
    background: linear-gradient(135deg, #ffd6e8, #ffc2dd, #ffb3d9);
    text-align: center;
    color: white;
    overflow-x: hidden;
}
h1 {
    font-family: 'Pacifico', cursive;
    margin-top: 30px;
    text-shadow: 2px 2px 10px #ff69b4;
}
.container { padding: 20px; }
.btn {
    margin-top: 20px;
    padding: 12px 25px;
    border: none;
    border-radius: 30px;
    background: #ff4da6;
    color: white;
    font-size: 18px;
    cursor: pointer;
}
.hidden { display: none; }
video {
    width: 85%;
    max-width: 360px;
    border-radius: 20px;
    margin-top: 20px;
}
.teddy {
    position: fixed;
    top: -50px;
    font-size: 28px;
    animation: fall linear infinite;
}
@keyframes fall {
    to { transform: translateY(110vh); }
}
</style>
</head>

<body>

<div class="container" id="home">
    <h1>Happy Teddy Day My Teddy 🧸💖</h1>
    <p>Tum meri life ka sabse soft, cutest aur warm hug ho 💕</p>
    <h2>🧸 Teddy aapka intezaar kar raha hai 🧸</h2>
    <button class="btn" onclick="showSurprise()">Click for Your Teddy 🎁</button>
</div>

<div class="container hidden" id="surprise">
    <h1>Yeh Raha Aapka Teddy 🧸💞</h1>
    <p>Yeh teddy meri taraf se ek tight warm hug hai 🤗</p>

    <video src="teddy.mp4" autoplay loop muted playsinline></video>

    <p>Happy Teddy Day meri sabse pyaari si jaan 💖</p>
</div>

<script>
function showSurprise() {
    document.getElementById("home").classList.add("hidden");
    document.getElementById("surprise").classList.remove("hidden");
}

function createTeddy() {
    const teddy = document.createElement("div");
    teddy.className = "teddy";
    teddy.innerHTML = "🧸";
    teddy.style.left = Math.random() * window.innerWidth + "px";
    teddy.style.animationDuration = (3 + Math.random() * 5) + "s";
    document.body.appendChild(teddy);
    setTimeout(() => teddy.remove(), 8000);
}
setInterval(createTeddy, 500);
</script>

</body>
</html>
