# aradhya--valentine-<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Aradhya ❤️</title>

<style>
body {
  margin: 0;
  height: 100vh;
  background: linear-gradient(135deg, #ff758c, #ff1e56);
  display: flex;
  justify-content: center;
  align-items: center;
  font-family: 'Segoe UI', sans-serif;
  overflow: hidden;
  color: white;
}

.card {
  background: rgba(255,255,255,0.18);
  padding: 30px;
  border-radius: 25px;
  text-align: center;
  width: 90%;
  max-width: 420px;
  backdrop-filter: blur(12px);
  z-index: 2;
}

h1 { font-size: 2.2em; }

.photo {
  width: 130px;
  height: 130px;
  border-radius: 50%;
  object-fit: cover;
  border: 4px solid white;
  margin: 15px 0;
}

#typing {
  font-size: 1.3em;
  margin: 15px 0;
  min-height: 40px;
}

.countdown {
  font-size: 1.1em;
  margin: 15px 0;
}

.signature {
  margin-top: 20px;
  font-style: italic;
}

.petal {
  position: absolute;
  top: -50px;
  font-size: 24px;
  animation: fall linear infinite;
}

@keyframes fall {
  to {
    transform: translateY(110vh) rotate(360deg);
    opacity: 0;
  }
}
</style>
</head>

<body>

<!-- 🎶 Music -->
<audio autoplay loop>
  <source src="https://cdn.pixabay.com/audio/2023/03/07/audio_4c4d7db8b6.mp3">
</audio>

<div class="card">
  <h1>Happy Valentine’s Day ❤️</h1>

  <!-- 📸 ADD HER PHOTO -->
  <img src="aradhya.jpg" class="photo" alt="Aradhya">

  <div id="typing"></div>

  <div class="countdown" id="countdown"></div>

  <p>
    Aradhya, you are my favorite chapter,
    my calm in chaos, and my forever choice.
  </p>

  <div class="signature">
    Forever yours,<br>
    <strong>Sachin 💕</strong>
  </div>
</div>

<script>
/* I LOVE YOU typing */
const text = "I Love You Aradhya ❤️";
let i = 0;
setInterval(() => {
  if (i < text.length) {
    document.getElementById("typing").innerHTML += text.charAt(i);
    i++;
  }
}, 120);

/* Countdown */
const valentine = new Date("Feb 14, 2026 00:00:00").getTime();
setInterval(() => {
  const now = new Date().getTime();
  const diff = valentine - now;
  const d = Math.floor(diff / (1000*60*60*24));
  const h = Math.floor((diff%(1000*60*60*24))/(1000*60*60));
  const m = Math.floor((diff%(1000*60*60))/(1000*60));
  document.getElementById("countdown").innerHTML =
    `⏳ ${d} Days ${h} Hours ${m} Minutes left`;
}, 1000);

/* Rose petals */
setInterval(() => {
  const petal = document.createElement("div");
  petal.className = "petal";
  petal.innerHTML = "🌹";
  petal.style.left = Math.random() * 100 + "vw";
  petal.style.animationDuration = (Math.random()*3+4) + "s";
  document.body.appendChild(petal);
  setTimeout(() => petal.remove(), 7000);
}, 400);
</script>

</body>
</html>
