<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Selamat Ulang Tahun Jenny 🎉</title>
  <style>
    body {
      margin: 0;
      font-family: 'Poppins', sans-serif;
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      color: #333;
      text-align: center;
      overflow-x: hidden;
    }
    .container {
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      padding: 20px;
    }
    h1 {
      font-size: 3rem;
      margin-bottom: 10px;
      animation: fadeInDown 1.5s ease;
    }
    h2 {
      font-weight: 400;
      margin-bottom: 20px;
      animation: fadeIn 2s ease;
    }
    .card {
      background: rgba(255, 255, 255, 0.85);
      border-radius: 20px;
      padding: 30px;
      max-width: 600px;
      box-shadow: 0 20px 40px rgba(0,0,0,0.15);
      animation: scaleIn 1.2s ease;
    }
    .card p {
      font-size: 1.1rem;
      line-height: 1.7;
    }
    .from {
      margin-top: 25px;
      font-style: italic;
      font-weight: 500;
    }
    .heart {
      font-size: 2.5rem;
      animation: beat 1.5s infinite;
      margin-top: 15px;
    }
    footer {
      margin-top: 40px;
      font-size: 0.9rem;
      opacity: 0.8;
    }
    @keyframes fadeInDown {
      from { opacity: 0; transform: translateY(-30px); }
      to { opacity: 1; transform: translateY(0); }
    }
    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }
    @keyframes scaleIn {
      from { transform: scale(0.8); opacity: 0; }
      to { transform: scale(1); opacity: 1; }
    }
    @keyframes beat {
      0%, 100% { transform: scale(1); }
      50% { transform: scale(1.2); }
    }
    .slideshow { position: relative; }
  .slide { display: none; font-size: 1.1rem; line-height: 1.7; animation: fadeIn 1.5s ease; }
  .slide.active { display: block; }
</style>
</head>
<body>
  <!-- Musik Ulang Tahun -->
  <audio id="bgMusic" autoplay loop>
    <source src="happy-birthday.mp3" type="audio/mpeg">
    Browser kamu tidak mendukung audio.
  </audio>

  <button onclick="toggleMusic()" style="position:fixed;top:20px;right:20px;padding:10px 15px;border:none;border-radius:20px;background:#ff6f91;color:white;font-weight:bold;cursor:pointer;box-shadow:0 5px 15px rgba(0,0,0,0.2);">
    🎶 Musik
  </button>

  <script>
    const music = document.getElementById('bgMusic');
    function toggleMusic() {
      if (music.paused) {
        music.play();
      } else {
        music.pause();
      }
    }
      let slides = document.querySelectorAll('.slide');
    let index = 0;
    setInterval(() => {
      slides[index].classList.remove('active');
      index = (index + 1) % slides.length;
      slides[index].classList.add('active');
    }, 4000);
  </script>
  <div class="container">
    <h1>Selamat Ulang Tahun 🎂</h1>
    <h2>Jenny Auralia Januarte</h2>

    <div class="card">
  <div class="slideshow">
    <div class="slide active">
      <p>🎉 Selamat ulang tahun yang ke-21, Jenny! 🎉<br>Hari ini adalah tentang kamu dan semua hal indah yang kamu bawa ke dunia.</p>
    </div>
    <div class="slide">
      <p>🤍 Terima kasih telah lahir ke dunia ini dan telah menjadi sahabat terbaikku.<br>Tawa, cerita, dan kenangan kita tak ternilai.</p>
    </div>
    <div class="slide">
      <p>🌟 Di usia barumu ini, semoga semua mimpi dan harapanmu perlahan menjadi nyata.</p>
    </div>
    <div class="slide">
      <p>💫 Tetaplah menjadi Jenny yang kuat, baik hati, dan penuh cahaya.<br>Kamu lebih hebat dari yang kamu kira.</p>
    </div>
    <div class="slide">
      <p>💖 Dengan penuh sayang,<br><strong>Amanda</strong></p>
    </div>
  </div>
</div>
      <div class="heart">💖</div>
    </div>

    <footer>
      Dibuat khusus untuk Jenny • 12 Januari 2004
    </footer>
  </div>
</body>
</html>
