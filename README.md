<!DOCTYPE html>
<html lang="th">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>ร้านอาหารญี่ปุ่น SAKURA</title>
<style>
  /* CSS */
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }
  body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background-color: #fff8f0;
    color: #333;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
  }
  header {
    background-color: #ffccd5;
    padding: 20px;
    text-align: center;
  }
  nav {
    margin-top: 10px;
  }
  nav a {
    margin: 0 12px;
    text-decoration: none;
    color: #800020;
    font-weight: bold;
    padding-bottom: 4px;
    cursor: pointer;
  }
  nav a.active,
  nav a:hover {
    border-bottom: 2px solid #800020;
  }
  main {
    flex: 1;
    padding: 30px 20px;
    max-width: 900px;
    margin: 0 auto;
    width: 100%;
  }
  .hero {
    background: url('images/sushi.jpg') center/cover no-repeat;
    color: white;
    padding: 80px 20px;
    border-radius: 10px;
    text-shadow: 1px 1px 5px #222;
  }
  .hero h2 {
    font-size: 2.8rem;
    margin-bottom: 10px;
  }
  .hero p {
    font-size: 1.4rem;
    margin-bottom: 20px;
  }
  .btn {
    background-color: #800020;
    color: white;
    padding: 14px 28px;
    border: none;
    border-radius: 6px;
    cursor: pointer;
    text-decoration: none;
    font-size: 1.1rem;
  }
  .btn:hover {
    background-color: #550015;
  }
  .menu-list {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 24px;
  }
  .menu-item {
    background: white;
    border-radius: 14px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.12);
    padding: 20px;
    width: 260px;
    text-align: center;
  }
  .menu-item img {
    width: 100%;
    border-radius: 12px;
  }
  .menu-item h3 {
    margin-top: 14px;
    margin-bottom: 6px;
    color: #800020;
  }
  .menu-item p {
    font-size: 0.95rem;
    color: #555;
  }
  .price {
    margin-top: 8px;
    font-weight: bold;
    color: #e60023;
    font-size: 1.2rem;
  }
  form {
    max-width: 400px;
    margin: 0 auto;
    background: white;
    padding: 30px;
    border-radius: 12px;
    box-shadow: 0 4px 12px rgba(0,0,0,0.15);
    display: flex;
    flex-direction: column;
  }
  form label {
    margin-top: 16px;
    margin-bottom: 6px;
    font-weight: 600;
    color: #800020;
  }
  form input {
    padding: 10px;
    font-size: 1rem;
    border: 1.8px solid #ccc;
    border-radius: 8px;
    transition: border-color 0.3s;
  }
  form input:focus {
    border-color: #800020;
    outline: none;
  }
  form button {
    margin-top: 24px;
    padding: 12px;
    font-size: 1.1rem;
    background-color: #800020;
    color: white;
    border: none;
    border-radius: 8px;
    cursor: pointer;
  }
  form button:hover {
    background-color: #550015;
  }
  #booking-message {
    text-align: center;
    margin-top: 20px;
    font-weight: bold;
    color: green;
  }
  footer {
    background-color: #222;
    color: white;
    text-align: center;
    padding: 14px 0;
    font-size: 0.9rem;
  }
  @media (max-width: 600px) {
    .menu-list {
      flex-direction: column;
      align-items: center;
    }
    .menu-item {
      width: 90%;
    }
    .hero {
      padding: 40px 20px;
      font-size: 1rem;
    }
  }
  .hidden {
    display: none;
  }
</style>
</head>
<body>
<header>
  <h1>🍣 ร้านอาหารญี่ปุ่น SAKURA</h1>
  <nav>
    <a id="nav-home" class="active">หน้าแรก</a>
    <a id="nav-menu">เมนู</a>
    <a id="nav-booking">จองโต๊ะ</a>
  </nav>
</header>

<main>
  <!-- หน้าแรก -->
  <section id="page-home" class="page-section">
    <div class="hero">
      <h2>ยินดีต้อนรับสู่ร้าน SAKURA</h2>
      <p>อาหารญี่ปุ่นแท้ ๆ รสชาติต้นตำรับ บรรยากาศอบอุ่น</p>
      <button class="btn" id="btn-to-menu">ดูเมนูอาหาร</button>
    </div>
  </section>

  <!-- เมนู -->
  <section id="page-menu" class="page-section hidden">
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
    </div>
  </section>

  <!-- จองโต๊ะ -->
  <section id="page-booking" class="page-section hidden">
    <h2>แบบฟอร์มจองโต๊ะ</h2>
    <form id="booking-form">
      <label for="name">ชื่อ-นามสกุล:</label>
      <input type="text" id="name" name="name" required />

      <label for="phone">เบอร์โทรศัพท์:</label>
      <input type="tel" id="phone" name="phone" required pattern="[0-9]{9,10}" placeholder="ตัวเลข 9-10 หลัก" />

      <label for="date">วันที่จอง:</label>
      <input type="date" id="date" name="date" required min="" />

      <button type="submit">จองโต๊ะ</button>
    </form>
    <p id="booking-message"></p>
  </section>
</main>

<footer>
  <p>© 2025 ร้าน SAKURA | เปิดบริการทุกวัน 11:00 - 22:00</p>
</footer>

<!-- Firebase SDK -->
<script src="https://www.gstatic.com/firebasejs/9.22.1/firebase-app-compat.js"></script>
<script src="https://www.gstatic.com/firebasejs/9.22.1/firebase-database-compat.js"></script>

<script>
  // การจัดการ navigation แบบง่าย
  const navHome = document.getElementById('nav-home');
  const navMenu = document.getElementById('nav-menu');
  const navBooking = document.getElementById('nav-booking');
  const btnToMenu = document.getElementById('btn-to-menu');

  const pageHome = document.getElementById('page-home');
  const pageMenu = document.getElementById('page-menu');
  const pageBooking = document.getElementById('page-booking');

  function showPage(pageId) {
    [pageHome, pageMenu, pageBooking].forEach(section => {
      section.classList.add('hidden');
    });
    [navHome, navMenu, navBooking].forEach(nav => {
      nav.classList.remove('active');
    });
    if (pageId === 'home') {
      pageHome.classList.remove('hidden');
      navHome.classList.add('active');
    } else if (pageId === 'menu') {
      page
