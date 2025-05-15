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
<!DOCTYPE html>
<html lang="th">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>จองโต๊ะ - ร้านอาหารญี่ปุ่น SAKURA</title>
  <link rel="stylesheet" href="css/style.css" />
</head>
<body>
  <header>
    <h1>🍣 ร้านอาหารญี่ปุ่น SAKURA</h1>
    <nav>
      <a href="index.html">หน้าแรก</a>
      <a href="menu.html">เมนู</a>
      <a href="booking.html" class="active">จองโต๊ะ</a>
    </nav>
  </header>

  <main>
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
  </main>

  <footer>
    <p>© 2025 ร้าน SAKURA | เปิดบริการทุกวัน 11:00 - 22:00</p>
  </footer>

  <script src="https://www.gstatic.com/firebasejs/9.22.1/firebase-app-compat.js"></script>
  <script src="https://www.gstatic.com/firebasejs/9.22.1/firebase-database-compat.js"></script>
  <script src="js/booking.js"></script>
</body>
</html>
/* Reset */
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
  background: url('../images/sushi.jpg') center/cover no-repeat;
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

/* ฟอร์มจองโต๊ะ */
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

/* Footer */
footer {
  background-color: #222;
  color: white;
  text-align: center;
  padding: 14px 0;
  font-size: 0.9rem;
}

/* Responsive */
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
// ใช้สำหรับหน้า index.html และ menu.html
// ในนี้อาจจะใส่ฟังก์ชันสำหรับอนาคต
console.log("Script main loaded");
// กำหนดวันขั้นต่ำของ input date ให้เป็นวันปัจจุบัน
const dateInput = document.getElementById('date');
const today = new Date().toISOString().split('T')[0];
dateInput.min = today;

// Firebase Config (ให้คุณไปสร้าง Firebase Project แล้วแทนที่ config นี้)
const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_PROJECT_ID.firebaseapp.com",
  databaseURL: "https://YOUR_PROJECT_ID-default-rtdb.firebaseio.com",
  projectId: "YOUR_PROJECT_ID",
  storageBucket: "YOUR_PROJECT_ID.appspot.com",
  messagingSenderId: "YOUR_SENDER_ID",
  appId: "YOUR_APP_ID"
};

// Initialize Firebase
firebase.initializeApp(firebaseConfig);
const database = firebase.database();

const form = document.getElementById('booking-form');
const message = document.getElementById('booking-message');

form.addEventListener('submit', (e) => {
  e.preventDefault();

  // ดึงค่าจากฟอร์ม
  const name = form.name.value.trim();
  const phone = form.phone.value.trim();
  const date = form.date.value;

  if (!name || !phone || !date) {
    message.style.color = 'red';
    message.textContent = "กรุณากรอกข้อมูลให้ครบถ้วน";
    return;
  }

  // สร้าง object สำหรับบันทึก
  const bookingData = {
    name,
    phone,
    date,
    timestamp: Date.now()
  };

  // เขียนข้อมูลไปที่ Firebase
  const newBookingKey = database.ref().child('bookings').push().key;
  const updates = {};
  updates['/bookings/' + newBookingKey] = bookingData;

  database.ref().update(updates)
    .then(() => {
      message.style.color = 'green';
      message.textContent = "✅ จองโต๊ะเรียบร้อยแล้ว! ขอบคุณค่ะ";
      form.reset();
      form.date.min = today; // รีเซ็ตวันขั้นต่ำอีกครั้ง
    })
    .catch((error) => {
      message.style.color = 'red';
      message.textContent = "❌ เกิดข้อผิดพลาด: " + error.message;
    });
});
{
  "rules": {
    ".read": true,
    ".write": true
  }
}
git init
git add .
git commit -m "Initial commit for Japanese restaurant website"
git branch -M main
git remote add origin https://github.com/username/japanese-restaurant.git
git push -u origin main
