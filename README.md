<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Will You Be My Valentine 💖</title>

  <style>
    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      min-height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      font-family: Arial, sans-serif;
      padding: 20px;
    }

    .card {
      width: 100%;
      max-width: 380px;
      background: #fff;
      border-radius: 20px;
      padding: 30px 20px;
      text-align: center;
      box-shadow: 0 10px 25px rgba(0,0,0,0.2);
      position: relative;
    }

    h1 {
      color: #ff4d6d;
      font-size: 1.6rem;
      margin-bottom: 25px;
    }

    h2 {
      font-size: 1.2rem;
      margin-top: 10px;
    }

    .btn-group {
      margin-top: 20px;
      height: 120px;
      position: relative;
    }

    button {
      padding: 12px 22px;
      font-size: 16px;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      position: absolute;
    }

    #yesBtn {
      background: #ff4d6d;
      color: white;
      left: 50%;
      transform: translateX(-50%);
    }

    #noBtn {
      background: #6c757d;
      color: white;
      top: 60px;
      left: 50%;
      transform: translateX(-50%);
    }

    .hidden {
      display: none;
    }

    img {
      width: 100%;
      max-width: 260px;
      margin-top: 20px;
      border-radius: 15px;
    }
  </style>
</head>

<body>

  <!-- QUESTION CARD -->
  <div class="card" id="questionCard">
    <h1>Will you be my Valentine? 💖</h1>

    <div class="btn-group">
      <button id="yesBtn">Yes ❤️</button>
      <button id="noBtn">No 😜</button>
    </div>
  </div>

  <!-- LOVE CARD -->
  <div class="card hidden" id="loveCard">
    <h1>Best decision ever 💕</h1>
    <h2>I love you Payal 😘❤️</h2>
    <img src="https://media.giphy.com/media/MDJ9IbxxvDUQM/giphy.gif" alt="Love GIF">
  </div>

  <script>
    const noBtn = document.getElementById("noBtn");
    const yesBtn = document.getElementById("yesBtn");
    const questionCard = document.getElementById("questionCard");
    const loveCard = document.getElementById("loveCard");

    function moveNoButton() {
      const card = questionCard.getBoundingClientRect();
      const maxX = card.width - noBtn.offsetWidth;
      const maxY = 100;

      const x = Math.random() * maxX;
      const y = Math.random() * maxY;

      noBtn.style.left = x + "px";
      noBtn.style.top = y + "px";
    }

    noBtn.addEventListener("mouseover", moveNoButton);
    noBtn.addEventListener("touchstart", moveNoButton);

    yesBtn.addEventListener("click", () => {
      questionCard.classList.add("hidden");
      loveCard.classList.remove("hidden");
    });
  </script>

</body>
</html>
