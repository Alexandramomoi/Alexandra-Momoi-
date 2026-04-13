<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Alex's Cute World 💖</title>

<!-- Cute font -->
<link href="https://fonts.googleapis.com/css2?family=Pacifico&display=swap" rel="stylesheet">

<style>
  body {
    margin: 0;
    padding: 0;
    background: linear-gradient(135deg, #ffd6e7, #e0c3fc);
    font-family: 'Pacifico', cursive;
    text-align: center;
    overflow-x: hidden;
  }

  h1 {
    color: #ff4da6;
    margin-top: 30px;
  }

  p {
    color: #555;
  }

  .card {
    background: white;
    margin: 30px auto;
    padding: 20px;
    border-radius: 20px;
    width: 80%;
    max-width: 400px;
    box-shadow: 0 0 15px rgba(0,0,0,0.1);
  }

  button {
    background-color: #ff99cc;
    border: none;
    padding: 10px 20px;
    border-radius: 20px;
    cursor: pointer;
    font-family: 'Pacifico', cursive;
    transition: 0.3s;
  }

  button:hover {
    background-color: #ff66b2;
    transform: scale(1.1);
  }

  /* Floating hearts */
  .heart {
    position: fixed;
    bottom: -10px;
    font-size: 20px;
    animation: floatUp 5s linear infinite;
  }

  @keyframes floatUp {
    0% {
      transform: translateY(0);
      opacity: 1;
    }
    100% {
      transform: translateY(-100vh);
      opacity: 0;
    }
  }
</style>
</head>

<body>

<h1>Welcome to Alex's World 💕</h1>
<p>✨ Cute vibes only ✨</p>

<div class="card">
  <h2>About Me 🌸</h2>
  <p>Hi! I'm Alex 💖 I love cute things, music, and fun websites!</p>
</div>

<div class="card">
  <h2>My Links 🔗</h2>
  <button onclick="window.open('https://instagram.com')">Instagram</button>
  <button onclick="window.open('https://discord.com')">Discord</button>
</div>

<div class="card">
  <h2>Fun Button 🎀</h2>
  <button onclick="showMessage()">Click me 💕</button>
</div>

<!-- Music -->
<audio autoplay loop>
  <source src="https://www.bensound.com/bensound-music/bensound-sunny.mp3" type="audio/mp3">
</audio>

<script>
  function showMessage() {
    alert("You're amazing 💖✨");
  }

  // Create floating hearts
  setInterval(() => {
    let heart = document.createElement("div");
    heart.classList.add("heart");
    heart.innerHTML = "💖";
    heart.style.left = Math.random() * 100 + "vw";
    heart.style.fontSize = (Math.random() * 20 + 10) + "px";

    document.body.appendChild(heart);

    setTimeout(() => {
      heart.remove();
    }, 5000);
  }, 500);
</script>

</body>
</html>
