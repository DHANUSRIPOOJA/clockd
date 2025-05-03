# clockd
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Digital Clock</title>
  <style>
    body {
      font-family: sans-serif;
      text-align: center;
      padding-top: 50px;
      background-color: #ffe4f2; /* light pink */
      color: #333;
      transition: 0.3s;
    }

    h1 {
      font-size: 36px;
      color: #d81b60;
    }

    #clock {
      font-size: 48px;
      margin: 30px auto;
      padding: 20px 40px;
      background-color: #ffc1e3;
      border-radius: 10px;
      display: inline-block;
    }

    .mode-btn {
      background-color: #ff80ab;
      color: white;
      border: none;
      padding: 12px 24px;
      font-size: 16px;
      border-radius: 8px;
      cursor: pointer;
    }

    body.dark {
      background-color: #2c2c2c;
      color: #ffe4f2;
    }

    body.dark #clock {
      background-color: #ff4081;
    }

    body.dark .mode-btn {
      background-color: #ffb6c1;
      color: #2c2c2c;
    }
  </style>
</head>
<body>
  <h1>🕒 Digital Clock</h1>
  <div id="clock">00:00:00</div><br><br>
  <button onclick="toggleMode()" class="mode-btn">Toggle Night Mode</button>

  <script>
    // Clock
    setInterval(() => {
      const now = new Date();
      document.getElementById("clock").innerText = now.toLocaleTimeString();
    }, 1000);

    // Dark/Light Toggle
    function toggleMode() {
      document.body.classList.toggle("dark");
    }
  </script>
</body>
</html>
```
