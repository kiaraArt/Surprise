<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Happy Birthday Mishu 💖</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Comic+Neue:wght@400;700&display=swap');
    body {
      margin: 0;
      background: #ffe6f0;
      font-family: 'Comic Neue', cursive, sans-serif;
      overflow: hidden;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      color: #d6336c;
      position: relative;
    }
    .page {
      display: none;
      flex-direction: column;
      align-items: center;
      text-align: center;
      max-width: 400px;
      padding: 20px;
      animation: fadeIn 1s ease forwards;
    }
    .active {
      display: flex;
    }
    button {
      background-color: #ffb6c1;
      border: none;
      padding: 15px 30px;
      font-size: 1.2rem;
      border-radius: 30px;
      cursor: pointer;
      color: white;
      margin-top: 20px;
      box-shadow: 0 0 10px #ff9abf;
      transition: background-color 0.3s ease;
    }
    button:hover {
      background-color: #ff88a5;
    }
    h1 {
      margin: 0;
      font-size: 2.5rem;
      text-shadow: 2px 2px #ffc1d3;
    }
    p {
      font-size: 1.2rem;
      margin: 15px 0;
      line-height: 1.5;
    }
    img.bear {
      width: 150px;
      margin-top: 15px;
      border-radius: 15px;
      box-shadow: 0 0 15px #ffb6c1;
    }
    /* Hearts floating */
    .heart {
      position: fixed;
      width: 25px;
      height: 25px;
      background: #ff6f91;
      clip-path: polygon(
        50% 0%,
        61% 10%,
        68% 20%,
        68% 30%,
        50% 55%,
        32% 30%,
        32% 20%,
        39% 10%
      );
      animation: floatUp 5s linear infinite;
      opacity: 0.8;
      pointer-events: none;
    }
    @keyframes floatUp {
      0% {
        transform: translateY(0) scale(1);
        opacity: 0.8;
      }
      100% {
        transform: translateY(-600px) scale(1.2);
        opacity: 0;
      }
    }
    @keyframes fadeIn {
      from {opacity: 0; transform: translateY(20px);}
      to {opacity: 1; transform: translateY(0);}
    }
    /* Music controls */
    #musicControl {
      position: fixed;
      top: 10px;
      right: 10px;
      background: #ffb6c1;
      border: none;
      border-radius: 50%;
      width: 40px;
      height: 40px;
      cursor: pointer;
      box-shadow: 0 0 8px #ff9abf;
      color: white;
      font-size: 18px;
      display: flex;
      justify-content: center;
      align-items: center;
      user-select: none;
      z-index: 10;
    }
    #musicControl:hover {
      background: #ff88a5;
    }
  </style>
</head>
<body>

  <button id="musicControl" title="Toggle Music">🔈</button>

  <div id="page1" class="page active">
    <h1>🎁 Open Me 🎁</h1>
    <button onclick="nextPage()">Open</button>
  </div>

  <div id="page2" class="page">
    <h1>Getting older, hehe &lt;&gt;</h1>
    <p>But still my forever cute 💕</p>
    <button onclick="nextPage()">Next</button>
  </div>

  <div id="page3" class="page">
    <h1>Happy Birthday, Mishu! 💖</h1>
    <p>Hope you live long and get rich 💸 so you can spoil me every day! 😘</p>
    <p>Stay healthy always, my soft bear 🧸💗</p>
    <img class="bear" src="https://media.giphy.com/media/H4DjXQXamtTiIuCcRU/giphy.gif" alt="Bear Hug" />
    <button onclick="restart()">❤️ Restart ❤️</button>
  </div>

  <audio id="bgMusic" loop>
    <source src="https://cdn.pixabay.com/download/audio/2021/10/28/audio_c4d1d75ed3.mp3?filename=soft-piano-ambient-10764.mp3" type="audio/mpeg" />
    Your browser does not support the audio element.
  </audio>

  <script>
    let currentPage = 1;
    const totalPages = 3;

    function nextPage() {
      document.getElementById(`page${currentPage}`).classList.remove('active');
      currentPage++;
      if (currentPage > totalPages) currentPage = 1;
      document.getElementById(`page${currentPage}`).classList.add('active');
    }

    function restart() {
      document.getElementById(`page${currentPage}`).classList.remove('active');
      currentPage = 1;
      document.getElementById(`page${currentPage}`).classList.add('active');
    }

    // Music control
    const music = document.getElementById('bgMusic');
    const musicControl = document.getElementById('musicControl');
    let musicPlaying = false;

    musicControl.addEventListener('click', () => {
      if(musicPlaying) {
        music.pause();
        musicPlaying = false;
        musicControl.textContent = '🔈';
      } else {
        music.play();
        musicPlaying = true;
        musicControl.textContent = '🔊';
      }
    });

    // Optional: Autoplay music on load if allowed
    window.onload = () => {
      music.play().then(() => {
        musicPlaying = true;
        musicControl.textContent = '🔊';
      }).catch(() => {
        musicPlaying = false;
        musicControl.textContent = '🔈';
      });
      createHearts();
    }

    // Floating hearts effect
    function createHearts() {
      const colors = ['#ff6f91', '#ff85a1', '#ffb3c6', '#ff88a5', '#ff5c7c'];
      const heartsCount = 15;

      for(let i=0; i < heartsCount; i++) {
        const heart = document.createElement('div');
        heart.classList.add('heart');
        heart.style.left = Math.random() * window.innerWidth + 'px';
        heart.style.animationDelay = (Math.random() * 5) + 's';
        heart.style.background = colors[Math.floor(Math.random() * colors.length)];
        heart.style.width = (15 + Math.random() * 15) + 'px';
        heart.style.height = heart.style.width;
        heart.style.animationDuration = (3 + Math.random() * 3) + 's';
        document.body.appendChild(heart);

        // Remove heart after animation
        heart.addEventListener('animationend', () => {
          heart.remove();
          createHearts(); // create a new heart
        });
      }
    }
  </script>
</body>
</html>
