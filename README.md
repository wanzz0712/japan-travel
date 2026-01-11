<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>11月大阪賞楓計畫 🍁</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        body { background-color: #fff5f5; font-family: "PingFang TC", "Microsoft JhengHei", sans-serif; }
        .hero-section { background: linear-gradient(rgba(0,0,0,0.4), rgba(0,0,0,0.4)), url('https://images.unsplash.com/photo-1545569341-9eb8b30979d9?auto=format&fit=crop&w=1200&q=80'); background-size: cover; background-position: center; height: 300px; display: flex; align-items: center; justify-content: center; color: white; border-radius: 0 0 30px 30px; }
        .day-card { background: white; border-radius: 20px; box-shadow: 0 10px 20px rgba(0,0,0,0.05); transition: 0.3s; border-left: 5px solid #e53e3e; }
        .day-card:hover { transform: translateY(-5px); }
        .badge { background: #fed7d7; color: #9b2c2c; padding: 4px 12px; border-radius: 99px; font-size: 12px; font-weight: bold; }
    </style>
</head>
<body class="pb-10">

    <div class="hero-section text-center">
        <div>
            <h1 class="text-4xl font-bold mb-2">大阪賞楓之旅</h1>
            <p class="text-lg opacity-90">11月限定 · 紅葉與美食的饗宴</p>
        </div>
    </div>

    <div class="max-w-4xl mx-auto px-4 -mt-10">
        <div class="bg-white p-6 rounded-2xl shadow-xl mb-8 border border-red-100">
            <h2 class="text-red-700 font-bold mb-4 flex items-center">💱 即時匯率換算 (1 JPY ≈ 0.215 TWD)</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                <div>
                    <label class="text-xs text-gray-500">輸入日圓 (JPY)</label>
                    <input type="number" id="jpy" value="10000" class="w-full p-3 border rounded-xl bg-gray-50 text-xl font-bold text-gray-700" oninput="convert()">
                </div>
                <div class="flex items-center justify-center">
                    <div class="text-center">
                        <p class="text-xs text-gray-400">約合台幣</p>
                        <p id="twd" class="text-3xl font-black text-red-500">NT$ 2,150</p>
                    </div>
                </div>
            </div>
        </div>

        <div class="space-y-6">
            <h2 class="text-2xl font-bold text-gray-800 mb-4 ml-2">📍 行程總覽</h2>
            
            <div class="day-card p-6">
                <span class="badge">Day 1</span>
                <h3 class="text-xl font-bold mt-2 text-gray-800">難波心齋橋：繁華之夜</h3>
                <p class="text-gray-600 mt-2 text-sm leading-relaxed">抵達關西機場 → 搭乘南海電鐵 Rapi:t 直達難波 → 逛心齋橋筋商店街 → 道頓堀固力果跑跑人合照 → 晚餐吃金龍拉麵或本家章魚燒。</p>
            </div>

            <div class="day-card p-6">
                <span class="badge">Day 2</span>
                <h3 class="text-xl font-bold mt-2 text-gray-800">大阪城公園與梅田夜景</h3>
                <p class="text-gray-600 mt-2 text-sm leading-relaxed">早上前往大阪城天守閣看銀杏與楓葉 → 黑門市場吃烤和牛與生魚片 → 下午逛梅田百貨區 → 晚上去阿倍野展望台 HARUKAS 300 俯瞰百萬夜景。</p>
            </div>

            <div class="day-card p-6">
                <span class="badge">Day 3</span>
                <h3 class="text-xl font-bold mt-2 text-gray-800">京都紅葉專屬：楓葉之后</h3>
                <p class="text-gray-600 mt-2 text-sm leading-relaxed">搭京阪電車前往京都 → 清水寺賞楓 → 二年坂與三年坂散策 → 傍晚前往永觀堂欣賞被譽為「紅葉永觀」的極致夜楓。</p>
            </div>

            <div class="day-card p-6">
                <span class="badge">Day 4</span>
                <h3 class="text-xl font-bold mt-2 text-gray-800">環球影城 USJ 全日狂歡</h3>
                <p class="text-gray-600 mt-2 text-sm leading-relaxed">一早進入環球影城 → 重點攻略超級任天堂世界 (Mario) → 11月會有聖誕季節預熱表演 → 晚上在環球影城步行街享受晚餐。</p>
            </div>

            <div class="day-card p-6">
                <span class="badge">Day 5</span>
                <h3 class="text-xl font-bold mt-2 text-gray-800">最後採買與臨空城 Outlet</h3>
                <p class="text-gray-600 mt-2 text-sm leading-relaxed">早上在難波補貨藥妝 → 前往機場旁的臨空城 Outlet 進行最後大採買 → 帶著滿滿戰利品搭機返台。</p>
            </div>
        </div>
    </div>

    <script>
        function convert() {
            const jpy = document.getElementById('jpy').value;
            const rate = 0.215; // 假設匯率
            document.getElementById('twd').innerText = 'NT$ ' + Math.round(jpy * rate).toLocaleString();
        }
    </script>
</body>
</html>
