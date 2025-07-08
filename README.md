<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Happy Birthday Mishu 💖</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background-color: #ffe6f0;
      font-family: 'Comic Sans MS', cursive;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      overflow: hidden;
    }
    .container {
      text-align: center;
      padding: 20px;
    }
    #message {
      display: none;
      animation: fadeIn 2s ease-in-out forwards;
    }
    button {
      padding: 15px 30px;
      font-size: 18px;
      background-color: #ffb6c1;
      color: white;
      border: none;
      border-radius: 20px;
      cursor: pointer;
    }
    img {
      width: 150px;
      margin-top: 20px;
    }
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }
  </style>
</head>
<body>
  <div class="container">
    <div id="intro">
      <h2>🎁 Click to Open 🎁</h2>
      <button onclick="showMessage()">Open Me</button>
    </div>

    <div id="message">
      <h1>💗 Happy Birthday, Mishu! 💗</h1>
      <p>You're getting older, hehehe &gt;&lt;<br>
      Still cute tho 💕</p>
      <p>Hope you live long and get rich 💸<br>
      So you can treat me every day because I'm broke 😭</p>
      <p>Stay healthy always 🧸💖</p>
      <img src="https://media.giphy.com/media/H4DjXQXamtTiIuCcRU/giphy.gif" alt="Bear Hug">
      <p>⚙️⚙️⚙️ Love from your broke bestie 💖⚙️⚙️⚙️</p>
    </div>
  </div>

  <script>
    function showMessage() {
      document.getElementById('intro').style.display = 'none';
      document.getElementById('message').style.display = 'block';
    }
  </script>
</body>
</html>
