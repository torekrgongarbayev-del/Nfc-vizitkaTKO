<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Loading...</title>
  <style>
    body {
      background: #000;
      color: #0f0;
      font-family: 'Courier New', monospace;
      padding: 40px;
      margin: 0;
      height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      overflow: hidden;
    }
    .loader {
      font-size: 2rem;
      margin: 20px;
    }
    @keyframes blink {
      0%, 100% { opacity: 1; }
      50% { opacity: 0.3; }
    }
    .blink {
      animation: blink 1.5s step-end infinite;
    }
    #screamer {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: #000;
      display: none;
      z-index: 9999;
      justify-content: center;
      align-items: center;
    }
    #screamer img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
    #screamer audio {
      display: none;
    }
  </style>
</head>
<body>
  <!-- Нормальный экран -->
  <h1 class="glitch">SKELETON</h1>
  <p>Твой 'успех' — мой обычный вторник.</p>
  <div class="loader">:: CONNECTING... <span class="blink">_</span></div>

  <!-- Скример (скрыт) -->
  <div id="screamer">
    <img src="https://i.imgur.com/5HTTq6P.gif" alt="SCREAM"> <!-- Можно заменить на страшное фото -->
    <audio autoplay>
      <source src="https://www.soundjay.com/horror/sounds/scream-02.mp3" type="audio/mpeg">
    </audio>
  </div>

  <script>
    // Через 3 секунды — скример
    setTimeout(() => {
      document.getElementById('screamer').style.display = 'flex';
      
      // Через 1.5 сек после скримера — переход к реальному профилю
      setTimeout(() => {
        window.location.href = 'https://t.me/quantum667';
      }, 1500);
    }, 3000);
  </script>
</body>
</html>
