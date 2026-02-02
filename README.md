<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Valentine 💖</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      font-family: Arial, sans-serif;
    }

    .container {
      text-align: center;
      background: white;
      padding: 40px;
      border-radius: 20px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.2);
    }

    h1 {
      color: #ff4d6d;
      margin-bottom: 30px;
    }

    button {
      padding: 12px 25px;
      font-size: 18px;
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
      width: 250px;
      margin-top: 20px;
      border-radius: 15px;
    }
  </style>
</head>
<body>

  <div class="container" id="questionBox">
    <h1>Will you be my Valentine? 💖</h1>
    <button id="yesBtn">Yes ❤️</button>
    <button id="noBtn">No 😜</button>
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

    noBtn.addEventListener("mouseover", () => {
      const x = Math.random() * (window.innerWidth - noBtn.offsetWidth);
      const y = Math.random() * (window.innerHeight - noBtn.offsetHeight);
      noBtn.style.left = x + "px";
      noBtn.style.top = y + "px";
    });

    yesBtn.addEventListener("click", () => {
      questionBox.classList.add("hidden");
      loveBox.classList.remove("hidden");
    });
  </script>

</body>
</html>
