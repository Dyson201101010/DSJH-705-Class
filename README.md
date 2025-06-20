# DSJH-705-Class
index.html
<!DOCTYPE html>
<html lang="zh-TW">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>DSJH 705班級群組</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: #dff1ff;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      display: flex;
      flex-direction: column;
      align-items: center;
      min-height: 100vh;
    }

    .glass {
      background: rgba(255, 255, 255, 0.25);
      box-shadow: 0 8px 32px 0 rgba(31, 38, 135, 0.37);
      backdrop-filter: blur(8px);
      -webkit-backdrop-filter: blur(8px);
      border-radius: 20px;
      border: 1px solid rgba(255, 255, 255, 0.18);
      padding: 30px 40px;
      margin: 40px 0;
      width: 90%;
      max-width: 600px;
      text-align: center;

      opacity: 0;
      transform: translateY(30px);
      transition: opacity 0.6s ease-out, transform 0.6s ease-out;
    }

    .glass.show {
      opacity: 1;
      transform: translateY(0);
    }

    h1 {
      font-size: 36px;
      color: #003366;
      margin-bottom: 10px;
    }

    .subtitle {
      font-size: 14px;
      color: #555;
      margin-top: 0;
    }

    h2 {
      font-size: 28px;
      color: #003366;
      margin-bottom: 10px;
    }

    p {
      font-size: 18px;
      color: #222;
      line-height: 1.6;
    }

    .footer {
      margin-top: auto;
      padding: 20px;
      font-size: 14px;
      color: #555;
    }
  </style>
</head>
<body>

  <!-- 標題與副標題 -->
  <div class="glass reveal">
    <h1>DSJH 705班級群組</h1>
    <p class="subtitle">此網站為私人網站，請勿直接盜用</p>
  </div>

  <!-- 重要行程表 -->
  <div class="glass reveal">
    <h2>重要行程表</h2>
    <p>目前無內容。</p>
  </div>

  <!-- 班級學生資訊表 -->
  <div class="glass reveal">
    <h2>班級學生資訊表</h2>
    <p>本班共有 <strong>26位學生</strong>。</p>
    <p>
      班長：12號<br>
      副班長：2號<br>
      風紀股長：21號<br>
      副風紀股長：3號<br>
      總務股長：24號<br>
      副總務股長：23號
    </p>
  </div>

  <!-- 免責聲明 -->
  <div class="footer">
    此網站並非DSJH所有，請勿侵權
  </div>

  <!-- 滾動動畫 -->
  <script>
    const reveals = document.querySelectorAll('.reveal');

    function checkReveal() {
      for (let i = 0; i < reveals.length; i++) {
        const windowHeight = window.innerHeight;
        const elementTop = reveals[i].getBoundingClientRect().top;
        const revealPoint = 100;

        if (elementTop < windowHeight - revealPoint) {
          reveals[i].classList.add('show');
        }
      }
    }

    window.addEventListener('scroll', checkReveal);
    window.addEventListener('load', checkReveal);
  </script>

</body>
</html>
