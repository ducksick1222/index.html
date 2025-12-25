# index.html
<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <title>自動搜尋系統</title>
    <style>
        body { font-family: 'Microsoft JhengHei', sans-serif; display: flex; justify-content: center; align-items: center; height: 100vh; margin: 0; background-color: #f1f3f4; }
        .card { background: white; padding: 40px; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1); text-align: center; max-width: 400px; }
        h1 { color: #d93025; font-size: 24px; margin-bottom: 10px; }
        p { color: #5f6368; font-size: 18px; line-height: 1.6; }
        .loading { margin-top: 20px; font-size: 14px; color: #1a73e8; font-weight: bold; }
    </style>
</head>
<body>
    <div class="card">
        <h1>請問自己 Google 很難嗎？</h1>
        <p>正在幫你搜尋：<br><strong>「9、10月發票還可以領嗎？」</strong></p>
        <div class="loading" id="countdown">3 秒後跳轉至搜尋結果...</div>
    </div>

    <script>
        var seconds = 3;
        var countdown = document.getElementById('countdown');
        var timer = setInterval(function() {
            seconds--;
            if (seconds <= 0) {
                clearInterval(timer);
                window.location.href = "https://www.google.com/search?q=9%E3%80%8110%E6%9C%88%E7%99%BC%E7%A5%A8%E9%82%84%E5%8F%AF%E4%BB%A5%E9%A0%98%E5%97%8E%EF%BC%9F";
            } else {
                countdown.innerText = seconds + " 秒後跳轉至搜尋結果...";
            }
        }, 1000);
    </script>
</body>
</html>
