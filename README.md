<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Valentine 💖</title>

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

    .container {
      width: 100%;
      max-width: 380px;
      text-align: center;
      background: white;
      padding: 25px;
      border-radius: 20px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.2);
      position: relative;
    }

    h1 {
      color: #ff4d6d;
      margin-bottom: 20px;
      font-size: 1.6rem;
    }

    h2 {
      font-size: 1.2rem;
    }

    .buttons {
      margin-top: 20px;
    }

    button {
      width: 120px;
      padding: 12px;
      font-size: 16px;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      margin: 10px;
    }

    #yesBtn {
      background-color: #ff4d6d;
      color: white;
    }

    #noBtn {
      background-color: #6c757d;
      color: white;
      position: absolute;
    }

    .hidden {
      display: none;
    }

    img {
      width: 100%;
      max-width: 250px;
      margin-top: 20px;
      border-radius: 15px;
    }

    /* Small screens */
    @media (max-width: 480px) {
      h1 {
        font-size: 1.4rem;
      }
      button {
        width: 100px;
        font-size: 15px;
      }
    }
  </style>
</head>

<body>

  <div class="container" id="questionBox">
    <h1>Will you be my Valentine? 💖</h1>

    <div class="buttons">
      <button id="yesBtn">Yes ❤️</button>
      <button id="noBtn">No 😜</button>
    </div>
  </div>

  <div class="container hidden" id="loveBox">
    <h1>Best decision ever 💕</h1>
    <h2>I love you Payal 😘❤️</h2>
    <img src="https://media.giphy.com/media/MDJ9IbxxvDUQM/giphy.gif" alt="Love Gif">
  </div>

  <script>
    const noBtn = document.getElementById("noBtn");
    const yesBtn = document.getElementById("yesBtn");
    const questionBox = document.getElementById("questionBox");
    const loveBox = document.getElementById("loveBox");

    function moveNoButton() {
      const container = questionBox.getBoundingClientRect();
      const x = Math.random() * (container.width - noBtn.offsetWidth);
      const y = Math.random() * (container.height - noBtn.offsetHeight);
      noBtn.style.left = x + "px";
      noBtn.style.top = y + "px";
    }

    // Works on mobile + desktop
    noBtn.addEventListener("mouseover", moveNoButton);
    noBtn.addEventListener("touchstart", moveNoButton);

    yesBtn.addEventListener("click", () => {
      questionBox.classList.add("hidden");
      loveBox.classList.remove("hidden");
    });
  </script>

</body>
</html>
