# Valentine-
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Abhay’s Valentine 💌</title>

  <style>
    body {
      margin: 0;
      height: 100vh;
      background: linear-gradient(135deg, #ffdde1, #ee9ca7);
      display: flex;
      justify-content: center;
      align-items: center;
      font-family: "Poppins", sans-serif;
    }

    .container {
      background: white;
      padding: 30px;
      border-radius: 20px;
      text-align: center;
      width: 90%;
      max-width: 420px;
      box-shadow: 0 20px 40px rgba(0,0,0,0.2);
    }

    h1 {
      margin-bottom: 10px;
    }

    p {
      color: #444;
    }

    .btns {
      margin-top: 20px;
      position: relative;
    }

    button {
      padding: 12px 28px;
      border: none;
      border-radius: 30px;
      font-size: 18px;
      cursor: pointer;
    }

    #yes {
      background: #ff4d6d;
      color: white;
      margin-right: 10px;
    }

    #no {
      background: #ddd;
      position: absolute;
    }

    .hidden {
      display: none;
    }

    .quiz button {
      display: block;
      width: 100%;
      margin: 10px 0;
      background: #ffe6eb;
    }
  </style>
</head>

<body>
  <div class="container">

    <!-- GIF -->
    <img src="https://media.tenor.com/6xJ9s6ZC0uQAAAAC/mochi.gif" width="150" />

    <h1>Soch le achhe se 🙄</h1>
    <p>Itni jaldi “No” mat bolna 😌</p>

    <!-- QUIZ -->
    <div class="quiz" id="quiz">
      <h3>Mini Game 🎮</h3>
      <p>How well do you know Abhay?</p>

      <button onclick="wrong()">He is very serious 😐</button>
      <button onclick="right()">He pretends serious but is soft 🥹</button>
      <button onclick="wrong()">He has no emotions 🤡</button>
    </div>

    <!-- PROPOSAL -->
    <div class="hidden" id="proposal">
      <h2>Okay… one last question 💖</h2>
      <p>Will you be my Valentine?</p>

      <div class="btns">
        <button id="yes" onclick="yesClicked()">Yes 💕</button>
        <button id="no">No 🙄</button>
      </div>
    </div>

    <!-- FINAL -->
    <div class="hidden" id="final">
      <h1>YAYYYY 😭❤️</h1>
      <p>You just made Abhay the happiest person 💘</p>
    </div>

  </div>

  <script>
    function wrong() {
      alert("Galat 😏 Try again!");
    }

    function right() {
      document.getElementById("quiz").classList.add("hidden");
      document.getElementById("proposal").classList.remove("hidden");
    }

    const noBtn = document.getElementById("no");
    noBtn.addEventListener("mouseover", () => {
      const x = Math.random() * 200 - 100;
      const y = Math.random() * 200 - 100;
      noBtn.style.transform = `translate(${x}px, ${y}px)`;
    });

    function yesClicked() {
      document.getElementById("proposal").classList.add("hidden");
      document.getElementById("final").classList.remove("hidden");
    }
  </script>

</body>
</html>
