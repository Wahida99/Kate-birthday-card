# Kate-birthday-card
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Happy 25th Birthday Kate!</title>
  <style>
    body {
      background: linear-gradient(135deg, #ff9a9e, #fad0c4, #fbc2eb, #a18cd1);
      font-family: 'Comic Sans MS', cursive, sans-serif;
      text-align: center;
      color: #fff;
      padding: 40px;
      overflow-x: hidden;
      position: relative;
      height: 100vh;
      overflow: hidden;
    }
    h1 {
      font-size: 3.2em;
      text-shadow: 2px 2px #ff6f91;
      margin-bottom: 20px;
    }
    .flowers, .chocolates {
      font-size: 2em;
      margin: 15px 0;
      animation: sparkle 2s infinite;
    }
    @keyframes sparkle {
      0%, 100% { opacity: 1; }
      50% { opacity: 0.6; }
    }
    p {
      font-size: 1.4em;
    }
    .signature {
      margin-top: 30px;
      font-size: 1.3em;
      font-style: italic;
      color: #ffe5ec;
    }
    /* Floating hearts */
    .heart {
      position: absolute;
      font-size: 1.8em;
      color: #ffb6c1;
      animation: floatHearts 6s linear infinite;
    }
    @keyframes floatHearts {
      0% { transform: translateY(100vh) scale(0.8); opacity: 0; }
      20% { opacity: 1; }
      100% { transform: translateY(-10vh) scale(1.2); opacity: 0; }
    }
    /* Floating balloons */
    .balloon {
      position: absolute;
      font-size: 2.5em;
      animation: floatBalloons 8s linear infinite;
    }
    @keyframes floatBalloons {
      0% { transform: translateY(100vh); opacity: 1; }
      100% { transform: translateY(-20vh); opacity: 0; }
    }
  </style>
</head>
<body>
  <h1>🎉 Happy 25th Birthday, Kate! 🎂</h1>

  <div class="flowers">💐 💐 💐</div>
  <div class="chocolates">🍫 Dubai Chocolate to sweeten your day 🍫</div>

  <p>May your day sparkle with joy, love, and endless laughter. ✨</p>

  <p class="signature">— From your friend, Wahi 💌</p>

  <audio autoplay loop>
    <source src="https://files.freemusicarchive.org/storage-freemusicarchive-org/music/no_curator/Podington_Bear/Happier/Podington_Bear_-_Daydream.mp3" type="audio/mpeg">
  </audio>

  <script>
    // Floating hearts
    function createHeart() {
      const heart = document.createElement('div');
      heart.classList.add('heart');
      heart.textContent = '💖';
      heart.style.left = Math.random() * 100 + 'vw';
      heart.style.animationDuration = (4 + Math.random() * 3) + 's';
      document.body.appendChild(heart);
      setTimeout(() => {
        heart.remove();
      }, 7000);
    }
    setInterval(createHeart, 800);

    // Floating balloons
    function createBalloon() {
      const balloon = document.createElement('div');
      balloon.classList.add('balloon');
      const balloons = ['🎈','🎉','🎊'];
      balloon.textContent = balloons[Math.floor(Math.random() * balloons.length)];
      balloon.style.left = Math.random() * 100 + 'vw';
      balloon.style.animationDuration = (6 + Math.random() * 4) + 's';
      document.body.appendChild(balloon);
      setTimeout(() => {
        balloon.remove();
      }, 10000);
    }
    setInterval(createBalloon, 1200);
  </script>
</body>
</html>
