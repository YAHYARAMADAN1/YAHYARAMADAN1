<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Game Store</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      margin: 0;
      padding: 0;
      background-color: #1e1e2f;
      color: #fff;
    }

    header {
      background-color: #111;
      padding: 20px;
      text-align: center;
    }

    h1 {
      margin: 0;
      font-size: 36px;
    }

    .games {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 20px;
      padding: 30px;
    }

    .game-card {
      background-color: #2c2c3e;
      border-radius: 10px;
      padding: 15px;
      width: 200px;
      text-align: center;
      box-shadow: 0 0 10px #000;
    }

    .game-card img {
      width: 100%;
      border-radius: 8px;
    }

    .game-card button {
      margin-top: 10px;
      background-color: #00c853;
      border: none;
      color: white;
      padding: 10px;
      width: 100%;
      border-radius: 5px;
      cursor: pointer;
      transition: background 0.3s;
    }

    .game-card button:hover {
      background-color: #00a843;
    }

    .contact {
      background-color: #111;
      padding: 30px;
    }

    .contact h2 {
      text-align: center;
    }

    form {
      max-width: 400px;
      margin: auto;
      display: flex;
      flex-direction: column;
      gap: 10px;
    }

    input, textarea {
      padding: 10px;
      border-radius: 5px;
      border: none;
    }

    input[type="submit"] {
      background-color: #00b0ff;
      color: white;
      cursor: pointer;
    }

    input[type="submit"]:hover {
      background-color: #008ecf;
    }

    footer {
      text-align: center;
      padding: 20px;
      background-color: #222;
      color: #aaa;
    }
  </style>
</head>
<body>

  <header>
    <h1>🎮 Game Store 🎮</h1>
    <p>أفضل الألعاب في مكان واحد</p>
  </header>

  <section class="games">
    <!-- لعبة 1 -->
    <div class="game-card">
      <img src="https://via.placeholder.com/200x120?text=Game+1" alt="Game 1">
      <h3>لعبة 1</h3>
      <a href="https://yahyaramadan.itch.io/my-car" target="_blank">
        <button>الدخول إلى اللعبة</button>
      </a>
    </div>

    <!-- لعبة 2 -->
    <div class="game-card">
      <img src="https://via.placeholder.com/200x120?text=Game+2" alt="Game 2">
      <h3>لعبة 2</h3>
      <button onclick="buyGame('لعبة 2')">شراء</button>
    </div>

    <!-- لعبة 3 -->
    <div class="game-card">
      <img src="https://via.placeholder.com/200x120?text=Game+3" alt="Game 3">
      <h3>لعبة 3</h3>
      <button onclick="buyGame('لعبة 3')">شراء</button>
    </div>
  </section>

  <section class="contact">
    <h2>📩 تواصل معنا</h2>
    <form onsubmit="return sendMessage()">
      <input type="text" id="name" placeholder="اسمك" required>
      <input type="email" id="email" placeholder="بريدك الإلكتروني" required>
      <textarea id="message" placeholder="اكتب رسالتك هنا..." rows="4" required></textarea>
      <input type="submit" value="إرسال">
    </form>
  </section>

  <footer>
    &copy; 2025 Game Store. جميع الحقوق محفوظة.
  </footer>

  <script>
    function buyGame(gameName) {
      alert("شكراً لشرائك " + gameName + "!");
    }

    function sendMessage() {
      const name = document.getElementById('name').value;
      alert("شكرًا يا " + name + "! تم استلام رسالتك.");
      return false; // يمنع إعادة تحميل الصفحة
    }
  </script>

</body>
</html>
