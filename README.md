<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>¡ÁCIDO HACKEADO!</title>
  <style>
    body {
      background-color: #000;
      color: lime;
      font-family: 'Courier New', Courier, monospace;
      text-align: center;
      margin-top: 100px;
    }
    h1 {
      font-size: 3em;
      color: red;
    }
    .countdown {
      font-size: 2em;
      margin-top: 30px;
      animation: blink 0.8s infinite;
    }
    @keyframes blink {
      50% { opacity: 0; }
    }
  </style>
</head>
<body>
  <h1>⚠️ ¡ÁCIDO HACKEADO! ⚠️</h1>
  <p>Estamos accediendo a tus datos personales...</p>
  <div class="countdown" id="count">1</div>

  <script>
    let count = 1;
    const counter = document.getElementById('count');

    const interval = setInterval(() => {
      count++;
      counter.textContent = count;
      if (count >= 3) {
        clearInterval(interval);
        // Intenta cerrar la pestaña
        window.close();
      }
    }, 1000);
  </script>
</body>
</html>
