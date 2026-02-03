<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Nikhitha 💖 Valentine</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <style>
    body {
      background: linear-gradient(135deg, #141E30, #243B55);
      font-family: "Courier New", monospace;
      overflow: hidden;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
      color: #00ffd5;
    }

    .heart {
      position: absolute;
      color: #ff6bcb;
      font-size: 18px;
      animation: float 6s linear infinite;
      opacity: 0.8;
    }

    @keyframes float {
      0% { transform: translateY(100vh); opacity: 0; }
      50% { opacity: 1; }
      100% { transform: translateY(-10vh); opacity: 0; }
    }

    .terminal {
      background: #000;
      border-radius: 14px;
      padding: 25px;
      width: 90%;
      max-width: 430px;
      box-shadow: 0 0 30px rgba(255,107,203,0.6);
    }

    .header {
      color: #ff6bcb;
      margin-bottom: 10px;
      font-size: 14px;
    }

    .code {
      font-size: 14px;
      line-height: 1.6;
      white-space: pre-wrap;
    }

    .buttons {
      margin-top: 20px;
      text-align: center;
      display: none;
    }

    button {
      background: #00ffd5;
      border: none;
      padding: 10px 20px;
      margin: 5px;
      border-radius: 8px;
      font-weight: bold;
      cursor: pointer;
    }
  </style>
</head>

<body>

<div class="terminal">
  <div class="header">💖</div>
  <div id="code" class="code"></div>

  <div class="buttons" id="buttons">
    <button onclick="yes()">YES 💖</button>
    <button onclick="no()">NO 😏</button>
  </div>
</div>

<script>
  function createHeart() {
    const heart = document.createElement("div");
    heart.className = "heart";
    heart.innerHTML = "💖";
    heart.style.left = Math.random() * 100 + "vw";
    document.body.appendChild(heart);
    setTimeout(() => heart.remove(), 6000);
  }
  setInterval(createHeart, 400);

  const text = `
Hey Nikhitha ❤️ will you be my valentine 🙂
`;

  let i = 0;
  const target = document.getElementById("code");

  function typeEffect() {
    if (i < text.length) {
      target.innerHTML += text.charAt(i);
      i++;
      setTimeout(typeEffect, 40);
    } else {
      document.getElementById("buttons").style.display = "block";
    }
  }

  function yes() {
    alert("Yay...Best decision ever 💖\nHappy Valentine’s Day, Nikki 🌹\n Love you babyluu💕");
  }

  function no() {
    alert("No is not acceptable 😅");
  }

  typeEffect();
</script>

</body>
</html>
