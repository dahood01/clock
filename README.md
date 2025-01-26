# clock
imagine if ninja got a low taper fade
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Digital Clock</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      background-color: #282c34;
      color: white;
      display: flex;
      flex-direction: column;
      justify-content: center;
      height: 100vh;
      margin: 0;
    }
    #clock {
      font-size: 5rem;
      margin-top: 20px;
    }
  </style>
</head>
<body>
  <h1>Digital Clock</h1>
  <div id="clock"></div>

  <script>
    function updateClock() {
      const now = new Date();
      const hours = String(now.getHours()).padStart(2, '0');
      const minutes = String(now.getMinutes()).padStart(2, '0');
      const seconds = String(now.getSeconds()).padStart(2, '0');

      const time = `${hours}:${minutes}:${seconds}`;
      document.getElementById('clock').textContent = time;
    }

    // Update the clock every second
    setInterval(updateClock, 1000);
    updateClock(); // Call it immediately to display the time right away
  </script>
</body>
</html>
