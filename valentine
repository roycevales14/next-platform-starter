<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Flora 💖</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      display: flex;
      justify-content: center;
      align-items: center;
      font-family: 'Segoe UI', sans-serif;
      overflow: hidden;
    }

    .card {
      background: white;
      padding: 45px 55px;
      border-radius: 25px;
      text-align: center;
      box-shadow: 0 20px 40px rgba(0,0,0,0.2);
      z-index: 2;
    }

    h1 {
      color: #e63946;
      margin-bottom: 10px;
    }

    p {
      color: #555;
      margin-bottom: 25px;
      font-size: 16px;
    }

    button {
      padding: 15px 35px;
      font-size: 18px;
      border: none;
      border-radius: 30px;
      cursor: pointer;
    }

    .yes {
      background: #e63946;
      color: white;
    }

    .yes:hover {
      transform: scale(1.1);
    }

    .no {
      background: #adb5bd;
      color: white;
      position: absolute;
    }

    /* Success screen */
    .success {
      display: none;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      text-align: center;
    }

    /* Floating hearts */
    .heart {
      position: absolute;
      bottom: -20px;
      font-size: 22px;
      animation: floatUp 6s linear infinite;
      opacity: 0.8;
    }

    @keyframes floatUp {
      0% { transform: translateY(0); opacity: 0; }
      10% { opacity: 1; }
      100% { transform: translateY(-110vh); opacity: 0; }
    }
  </style>
</head>
<body>

  <!-- Background Music -->
  <audio autoplay loop>
    <source src="https://www.bensound.com/bensound-music/bensound-romantic.mp3" type="audio/mpeg">
  </audio>

  <div class="card" id="mainCard">
    <h1>Flora, will you be my Valentine? 💖</h1>
    <p>You don’t really have a choice 😌</p>
    <button class="yes" onclick="sayYes()">Yes 💕</button>
    <button class="no" id="noBtn">No 🙈</button>
  </div>

  <div class="card success" id="successCard">
    <h1>YAY!! 💕🌹</h1>
    <p>See you on Valentine’s Day 😘<br>You’re officially my Valentine 💘</p>
  </div>

  <script>
    function sayYes() {
      document.getElementById("mainCard").style.display = "none";
      document.getElementById("successCard").style.display = "flex";
    }

    const noBtn = document.getElementById("noBtn");

    noBtn.addEventListener("mouseenter", () => {
      const maxX = window.innerWidth - noBtn.offsetWidth;
      const maxY = window.innerHeight - noBtn.offsetHeight;

      noBtn.style.left = Math.random() * maxX + "px";
      noBtn.style.top = Math.random() * maxY + "px";
    });

    // Floating hearts generator
    function createHeart() {
      const heart = document.createElement("div");
      heart.className = "heart";
      heart.innerHTML = "💖";
      heart.style.left = Math.random() * 100 + "vw";
      heart.style.animationDuration = (Math.random() * 3 + 4) + "s";
      document.body.appendChild(heart);

      setTimeout(() => heart.remove(), 7000);
    }

    setInterval(createHeart, 500);
  </script>

</body>
</html>