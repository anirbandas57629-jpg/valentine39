# valentine65
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Be My Valentine 💖</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      background: #0f172a;
      font-family: Arial, sans-serif;
      color: white;
    }

    .card {
      background: #020617;
      padding: 40px;
      border-radius: 16px;
      text-align: center;
      width: 320px;
    }

    h1 span {
      color: #22c55e;
    }

    img {
      width: 160px;
      margin: 20px 0;
    }

    .buttons {
      margin-top: 20px;
      display: flex;
      justify-content: center;
      gap: 20px;
    }

    button {
      border: none;
      padding: 12px 24px;
      font-size: 16px;
      border-radius: 8px;
      cursor: pointer;
      transition: all 0.3s ease;
    }

    .yes-button {
      background: #22c55e;
      color: black;
      font-weight: bold;
    }

    .no-button {
      background: #ef4444;
      color: white;
    }
  </style>
</head>
<body>

  <div class="card">
    <h1>Be My <span>Valentine</span> 💘</h1>

    <img src="https://media.tenor.com/2roX3uxz_68AAAAi/bear-love.gif" alt="cute bear">

    <p id="message">Will you be my Valentine?</p>

    <div class="buttons">
      <button class="yes-button" onclick="handleYes()">Yes</button>
      <button class="no-button" onclick="handleNo()">No</button>
    </div>
  </div>

  <script>
    const messages = [
      "Are you sure? 😢",
      "Think again 🥺",
      "Don’t break my heart 💔",
      "Last chance 😭",
      "Okay… still no? 🥹"
    ];

    let index = 0;

    function handleNo() {
      const noBtn = document.querySelector(".no-button");
      const yesBtn = document.querySelector(".yes-button");
      const msg = document.getElementById("message");

      msg.textContent = messages[index];
      index = (index + 1) % messages.length;

      let size = window.getComputedStyle(yesBtn).fontSize;
      let currentSize = parseFloat(size);
      yesBtn.style.fontSize = (currentSize * 1.3) + "px";
    }

    function handleYes() {
      document.body.innerHTML = `
        <div style="
          display:flex;
          justify-content:center;
          align-items:center;
          height:100vh;
          background:#020617;
          color:white;
          flex-direction:column;
          font-family:Arial;
        ">
          <h1>Knew you would say YES! 💖</h1>
          <img src="https://media.tenor.com/YTw87WdiaasAAAAi/tkthao219-bubududu.gif" width="200">
        </div>
      `;
    }
  </script>

</body>
</html>
