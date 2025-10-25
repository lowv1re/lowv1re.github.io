<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>lowv1re</title>
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <style>
    html, body {
      margin: 0;
      padding: 0;
      height: 100%;
      background-color: #000;
      color: #fff;
      font-family: Arial, Helvetica, sans-serif;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
    }
    h1 {
      font-size: 10vw;
      margin: 0;
      line-height: 1;
    }
    .footer {
      position: absolute;
      bottom: 20px;
      width: 100%;
      text-align: center;
      font-size: 1.5vw;
      opacity: 0.6;
      letter-spacing: 2px;
    }
    @media (max-width: 600px) {
      h1 { font-size: 15vw; }
      .footer { font-size: 3vw; }
    }
  </style>
</head>
<body>
  <h1>better than you</h1>
  <div class="footer">total fucking darkness</div>

  <!-- Счётчик посещений для тебя -->
  <script>
    // Секретный ключ для просмотра счетчика
    const secretKey = "2911"; // можешь поменять на любой свой
    const params = new URLSearchParams(window.location.search);

    if(params.get("key") === secretKey){
      // Получаем текущий счётчик из localStorage
      let count = localStorage.getItem("visits") || 0;
      count++;
      localStorage.setItem("visits", count);

      // Создаём элемент для отображения
      const counter = document.createElement("div");
      counter.style.position = "absolute";
      counter.style.top = "20px";
      counter.style.right = "20px";
      counter.style.color = "#fff";
      counter.style.fontSize = "2vw";
      counter.style.fontFamily = "Arial, sans-serif";
      counter.innerText = "Visits: " + count;

      // Добавляем на страницу
      document.body.appendChild(counter);
    }
  </script>
</body>
</html>
