<!DOCTYPE html>
<html lang="zh-Hant">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <!-- 教學：這裡是瀏覽器分頁上顯示的網站名稱，可以自行修改 -->
  <title>擺渡時光｜塘藏故事</title>
  <link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css" />
  <style>
    * { box-sizing: border-box; }
    body {
      margin: 0;
      font-family: "Noto Sans TC", Arial, sans-serif;
      color: #2f2f2f;
      background: #faf7f0;
      line-height: 1.7;
    }
    header {
      background: linear-gradient(rgba(58, 45, 32, 0.45), rgba(58, 45, 32, 0.45)),
        url("https://images.unsplash.com/photo-1500530855697-b586d89ba3ee?auto=format&fit=crop&w=1600&q=80") center/cover;
      color: white;
      min-height: 430px;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      padding: 40px 20px;
    }
    header h1 {
      font-size: 46px;
      margin: 0 0 12px;
      letter-spacing: 2px;
    }
    header p {
      font-size: 20px;
      margin: 0;
    }
    nav {
      position: sticky;
      top: 0;
      z-index: 10;
      background: #6f4e37;
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      padding: 12px;
      gap: 16px;
    }
    nav a {
      color: white;
      text-decoration: none;
      font-weight: 600;
      font-size: 15px;
    }
    section {
      max-width: 1100px;
      margin: auto;
      padding: 70px 20px;
    }
    .section-title {
      text-align: center;
      margin-bottom: 36px;
    }
    .section-title h2 {
      font-size: 32px;
      color: #5b3f2f;
      margin: 0;
    }
    .section-title p {
      color: #777;
      margin-top: 6px;
    }
    .intro {
      background: white;
      padding: 32px;
      border-radius: 20px;
      box-shadow: 0 8px 24px rgba(0,0,0,0.08);
      text-align: center;
    }
    .cards {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(230px, 1fr));
      gap: 22px;
    }
    .card {
      background: white;
      border-radius: 20px;
      overflow: hidden;
      box-shadow: 0 8px 22px rgba(0,0,0,0.08);
      transition: transform 0.25s ease;
    }
    .card:hover { transform: translateY(-6px); }
    .card img {
      width: 100%;
      height: 180px;
      object-fit: cover;
    }
    .card-content {
      padding: 20px;
    }
    .card h3 {
      margin: 0 0 8px;
      color: #5b3f2f;
    }
    .tag {
      display: inline-block;
      background: #efe2cf;
      color: #6f4e37;
      padding: 4px 10px;
      border-radius: 99px;
      font-size: 13px;
      margin-bottom: 10px;
    }
    .storymap {
      display: grid;
      grid-template-columns: 1fr 1.15fr;
      gap: 24px;
      align-items: start;
    }
    .story-list {
      display: flex;
      flex-direction: column;
      gap: 18px;
    }
    .story-card {
      background: white;
      border-radius: 20px;
      padding: 22px;
      box-shadow: 0 8px 22px rgba(0,0,0,0.08);
      cursor: pointer;
      border: 2px solid transparent;
      transition: 0.25s ease;
    }
    .story-card:hover,
    .story-card.active {
      border-color: #8a5a44;
      transform: translateY(-3px);
    }
    .story-card h3 {
      margin: 6px 0 8px;
      color: #5b3f2f;
    }
    .story-card p {
      margin: 0;
    }
    #map {
      height: 620px;
      border-radius: 24px;
      box-shadow: 0 8px 24px rgba(0,0,0,0.12);
      position: sticky;
      top: 72px;
      overflow: hidden;
    }
    @media (max-width: 850px) {
      .storymap { grid-template-columns: 1fr; }
      #map { position: relative; top: 0; height: 420px; }
    }
    .route {
      background: #fff;
      border-left: 6px solid #8a5a44;
      padding: 22px 26px;
      border-radius: 16px;
      margin-bottom: 18px;
      box-shadow: 0 6px 18px rgba(0,0,0,0.06);
    }
    table {
      width: 100%;
      border-collapse: collapse;
      background: white;
      border-radius: 18px;
      overflow: hidden;
      box-shadow: 0 8px 22px rgba(0,0,0,0.08);
    }
    th, td {
      padding: 16px;
      border-bottom: 1px solid #eee;
      text-align: left;
    }
    th {
      background: #6f4e37;
      color: white;
    }
    footer {
      background: #4a382d;
      color: white;
      text-align: center;
      padding: 36px 20px;
    }
    .button {
      display: inline-block;
      margin-top: 22px;
      padding: 12px 24px;
      background: #8a5a44;
      color: white;
      text-decoration: none;
      border-radius: 99px;
      font-weight: 700;
    }
  </style>
</head>
<body>
  <!-- =====================================================
    新手修改教學
    1. 想改網站大標題：找 <h1>...</h1>
    2. 想改副標題：找 header 裡的 <p>...</p>
    3. 想改景點名稱：找 <h3>...</h3>
    4. 想改景點介紹：找 <p>...</p>
    5. 想改地圖位置：改 data-lat 和 data-lng
       data-lat = 緯度，例如 23.9600
       data-lng = 經度，例如 120.5700
    6. 不熟程式時，不要刪掉 <div>、</div>、<script>
  ===================================================== -->
  <header id="home">
    <!-- 教學：這裡是首頁最上方的大標題 -->
    <h1>擺渡時光｜塘藏故事</h1>
    <!-- 教學：這裡是中文副標題，也就是首頁標語 -->
    <p>慢遊擺塘，遇見葡萄、信仰與鄉村生活</p>
    <a href="#attractions" class="button">開始探索 Explore</a>
  </header>

  <!-- 教學：這裡是網站上方選單，href="#about" 代表點擊後會跳到 id="about" 的區塊 -->
  <nav>
    <a href="#about">關於擺塘 About</a>
    <a href="#attractions">景點導覽 Attractions</a>
    <a href="#market">市集資訊 Market</a>
    <a href="#route">遊程推薦 Route</a>
    <a href="#contact">聯絡我們 Contact</a>
  </nav>

  <section id="about">
    <div class="section-title">
      <h2>關於擺塘｜About Batang</h2>
      <p>地方故事、農村生活與文化記憶的匯集</p>
    </div>
    <div class="intro">
      <p>擺塘村為一處融合農業特色、地方信仰與鄉村生活記憶的聚落。本網站以數位導覽方式整合在地景點、寺廟文化、農產特色與市集資訊，讓居民與遊客能更深入認識地方故事，發現擺塘村的日常之美。</p>
    </div>
  </section>

  <!-- =====================================================
    景點導覽區塊 StoryMap 教學
    左邊是景點卡片，右邊是互動地圖。
    點擊景點卡片後，地圖會移動到該景點座標。

    每一個景點卡片都長這樣：

    <div class="story-card" data-lat="緯度" data-lng="經度" data-zoom="地圖縮放">
      <span class="tag">分類名稱</span>
      <h3>景點名稱｜英文名稱</h3>
      <p>景點介紹文字</p>
    </div>

    修改重點：
    data-lat：放 Google 地圖查到的緯度
    data-lng：放 Google 地圖查到的經度
    data-zoom：地圖遠近，15~17 最常用，數字越大越近
  ===================================================== -->
<section id="attractions">
  <div class="section-title">
    <h2>景點導覽｜Attractions</h2>
    <p>點擊左側景點卡片，右側地圖會自動移動到對應位置</p>
  </div>

  <div class="storymap">
    <div class="story-list">

      <div class="story-card active" data-lat="23.984396545409314" data-lng="120.55957403768117" data-zoom="16">
        <span class="tag">Beliefs & Stories</span>
        <h3>信仰與故事①｜Beliefs & Stories</h3>
        <p>廟埕、香火與節慶，陪伴著居民走過農忙歲月，也保存著地方最真實的人情與故事。</p>
      </div>

      <div class="story-card" data-lat="23.98756251199652" data-lng="120.5577258837089" data-zoom="16">
        <span class="tag">Beliefs & Stories</span>
        <h3>信仰與故事②｜Beliefs & Stories</h3>
        <p>地方信仰空間不只是祭拜場所，也是居民交流、凝聚情感與延續文化的重要核心。</p>
      </div>

      <div class="story-card" data-lat="23.974853761810476" data-lng="120.56559629535225" data-zoom="16">
        <span class="tag">Beliefs & Stories</span>
        <h3>信仰與故事③｜Beliefs & Stories</h3>
        <p>透過廟宇與地方故事，可以看見擺塘村居民與土地之間長久累積的生活記憶。</p>
      </div>

      <div class="story-card" data-lat="23.987936624836724" data-lng="120.55707128001008" data-zoom="16">
        <span class="tag">Beliefs & Stories</span>
        <h3>信仰與故事④｜Beliefs & Stories</h3>
        <p>信仰承載地方文化，也讓遊客能從故事中理解擺塘村的日常與人情。</p>
      </div>

      <div class="story-card" data-lat="23.985737533116836" data-lng="120.55667866651686" data-zoom="16">
        <span class="tag">Rural Landscape</span>
        <h3>葡萄園景觀①｜Grape Vineyard</h3>
        <p>走進葡萄園與田園小徑，感受擺塘村農業景觀與鄉村日常風貌。</p>
      </div>

      <div class="story-card" data-lat="23.984885632162012" data-lng="120.55365999535238" data-zoom="16">
        <span class="tag">Rural Landscape</span>
        <h3>葡萄園景觀②｜Grape Vineyard</h3>
        <p>葡萄園展現擺塘村的產業特色，也呈現農村與土地共生的生活樣貌。</p>
      </div>

      <div class="story-card" data-lat="23.985678718912066" data-lng="120.55667866651686" data-zoom="16">
        <span class="tag">Rural Landscape</span>
        <h3>葡萄園景觀③｜Grape Vineyard</h3>
        <p>沿著農路漫步，可以看見葡萄產業與鄉村風景交織出的地方特色。</p>
      </div>

      <div class="story-card" data-lat="23.98640409222695" data-lng="120.55578817315883" data-zoom="16">
        <span class="tag">Rural Landscape</span>
        <h3>葡萄園景觀④｜Grape Vineyard</h3>
        <p>此處適合觀察農村景觀、拍攝田園風光，感受擺塘村慢活氛圍。</p>
      </div>

      <div class="story-card" data-lat="23.983315621971478" data-lng="120.55375008000988" data-zoom="16">
        <span class="tag">Rural Landscape</span>
        <h3>葡萄園景觀⑤｜Grape Vineyard</h3>
        <p>葡萄園景觀不只是農業生產空間，也是擺塘村重要的地方風景記憶。</p>
      </div>

      <div class="story-card" data-lat="23.98090645809134" data-lng="120.55779548000973" data-zoom="16">
        <span class="tag">Rural Landscape</span>
        <h3>葡萄園景觀⑥｜Grape Vineyard</h3>
        <p>透過葡萄園與田園景觀，遊客能更貼近擺塘村的農村生活與產業文化。</p>
      </div>

      <div class="story-card" data-lat="23.984396545409314" data-lng="120.55957403768117" data-zoom="16">
        <span class="tag">Farm Experience</span>
        <h3>農遊體驗｜Farm Experience</h3>
        <p>結合葡萄產業、農產品特產與地方體驗活動，讓遊客認識農村產業文化。</p>
      </div>

    </div>

    <div id="map"></div>
  </div>
</section>

<section id="route">
  <div class="section-title">
    <h2>遊程推薦｜Travel Route</h2>
    <p>適合遊客與居民共同參與的慢遊路線</p>
  </div>

  <div class="route">
    <h3>半日遊 Half-Day Trip</h3>
    <p>廟宇巡禮 → 葡萄園景觀 → 社區發展協會手作體驗 → 鄉村小徑散步</p>
  </div>
</section>
  </section>

  <section id="contact">
    <div class="section-title">
      <h2>聯絡我們｜Contact</h2>
      <p>歡迎認識擺塘村，探索更多地方故事</p>
    </div>
    <div class="intro">
      <p>若有活動合作、導覽需求或地方資訊補充，歡迎與擺塘村社區發展協會聯繫。</p>
      <p>Phone：04-8526097 </p>
   <a class="button" 
href="https://maps.app.goo.gl/WFNc9L1HomHLRcth8" 
target="_blank">
Google 地圖導航
</a>
  </section>

  <footer>
    <p>© 2026 擺塘村數位導覽平台 Batang Village Digital Guide</p>
  </footer>
  <!-- =====================================================
    地圖功能區塊教學
    這裡使用 Leaflet 地圖套件。
    如果你只是改景點名稱、介紹、座標，通常不需要改下面的 JavaScript。
  ===================================================== -->
  <script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"></script>
  <script>
    // 教學：這裡是地圖一開始顯示的位置。
    // [23.9600, 120.5700] 是預設中心點座標，15 是地圖縮放程度。
    const map = L.map('map').setView([23.985472655233988, 120.55972260884549], 15);

    L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
      maxZoom: 19,
      attribution: '© OpenStreetMap'
    }).addTo(map);

    const cards = document.querySelectorAll('.story-card');
    const markers = [];

    // 教學：這段會自動讀取每一張 story-card 的 data-lat 和 data-lng，並在地圖上建立標記。
    cards.forEach((card) => {
      const lat = parseFloat(card.dataset.lat);
      const lng = parseFloat(card.dataset.lng);
      const title = card.querySelector('h3').innerText;
      const desc = card.querySelector('p').innerText;

      const marker = L.marker([lat, lng]).addTo(map).bindPopup(`<b>${title}</b><br>${desc}`);
      markers.push(marker);

      card.addEventListener('click', () => {
        cards.forEach(c => c.classList.remove('active'));
        card.classList.add('active');
        map.flyTo([lat, lng], parseInt(card.dataset.zoom), {
          duration: 1.2
        });
        marker.openPopup();
      });
    });

    markers[0].openPopup();
  </script>
</body>
</html>
