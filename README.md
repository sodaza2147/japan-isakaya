# japan-isakaya
japanese-restaurant/
├── index.html
├── menu.html
├── booking.html
├── css/
│   └── style.css
├── js/
│   ├── main.js
│   └── booking.js
├── images/
│   ├── sushi.jpg
│   └── ramen.jpg
└── README.md
<!DOCTYPE html>
<html lang="th">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>ร้านอาหารญี่ปุ่น SAKURA</title>
  <link rel="stylesheet" href="css/style.css" />
</head>
<body>
  <header>
    <h1>🍣 ร้านอาหารญี่ปุ่น SAKURA</h1>
    <nav>
      <a href="index.html" class="active">หน้าแรก</a>
      <a href="menu.html">เมนู</a>
      <a href="booking.html">จองโต๊ะ</a>
    </nav>
  </header>

  <main>
    <section class="hero">
      <h2>ยินดีต้อนรับสู่ร้าน SAKURA</h2>
      <p>อาหารญี่ปุ่นแท้ ๆ รสชาติต้นตำรับ บรรยากาศอบอุ่น</p>
      <a href="menu.html" class="btn">ดูเมนูอาหาร</a>
    </section>
  </main>

  <footer>
    <p>© 2025 ร้าน SAKURA | เปิดบริการทุกวัน 11:00 - 22:00</p>
  </footer>

  <script src="js/main.js"></script>
</body>
</html>
<!DOCTYPE html>
<html lang="th">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>เมนู - ร้านอาหารญี่ปุ่น SAKURA</title>
  <link rel="stylesheet" href="css/style.css" />
</head>
<body>
  <header>
    <h1>🍣 ร้านอาหารญี่ปุ่น SAKURA</h1>
    <nav>
      <a href="index.html">หน้าแรก</a>
      <a href="menu.html" class="active">เมนู</a>
      <a href="booking.html">จองโต๊ะ</a>
    </nav>
  </header>

  <main>
    <h2>เมนูแนะนำ</h2>
    <div class="menu-list">
      <div class="menu-item">
        <img src="images/sushi.jpg" alt="ซูชิรวม" />
        <h3>ซูชิรวม</h3>
        <p>ปลาดิบสดใหม่ เสิร์ฟพร้อมวาซาบิ</p>
        <span class="price">฿350</span>
      </div>
      <div class="menu-item">
        <img src="images/ramen.jpg" alt="ราเมนต้นตำรับ" />
        <h3>ราเมนต้นตำรับ</h3>
        <p>น้ำซุปกลมกล่อม เส้นเหนียวนุ่ม</p>
        <span class="price">฿250</span>
      </div>
      <!-- เพิ่มเมนูอื่น ๆ ได้ตามต้องการ -->
    </div>
  </main>

  <footer>
    <p>© 2025 ร้าน SAKURA | เปิดบริการทุกวัน 11:00 - 22:00</p>
  </footer>

  <script src="js/main.js"></script>
</body>
</html>
