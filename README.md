# 🔑 Token Extractor — Chrome Extension

Extension สำหรับดึง Token จาก localStorage ของเว็บที่กำหนด พร้อม UI โทนฟ้า Pastel สวยงาม

---

## ✨ ฟีเจอร์

- 🔵 ดึง Token จาก `localStorage` อัตโนมัติ
- 🌐 จำกัดให้ใช้ได้เฉพาะ Domain ที่อนุญาต
- 🧹 ลบ `'` และ `"` ออกจาก Token อัตโนมัติ
- 🔴 เตือนด้วยสีแดงเมื่อเจอ `"` ใน Token
- 📋 ปุ่ม Copy Token ในคลิกเดียว

---

## 📦 วิธีติดตั้ง

### 1. ดาวน์โหลด

```
กด Code → Download ZIP แล้วแตกไฟล์ออก
```

หรือใช้ Git:

```bash
git clone https://github.com/YOUR_USERNAME/token-extractor-extension.git
```

### 2. เปิด Chrome Extensions

ไปที่ URL นี้ในช่อง address bar:

```
chrome://extensions/
```

### 3. เปิด Developer Mode

มุมบนขวา → เปิด **Developer mode**

### 4. Load Extension

กด **Load unpacked** → เลือกโฟลเดอร์ `token-extractor-extension`

### 5. เสร็จแล้ว ✅

ไอคอน 🔑 จะปรากฏที่ toolbar ของ Chrome

---

## ⚙️ ตั้งค่า Domain ที่อนุญาต

เปิดไฟล์ `popup.js` แล้วแก้ตรงนี้:

```js
const ALLOWED_URLS = [
  'https://your-site.com',   // ← เปลี่ยนเป็น domain ที่ต้องการ
  // 'https://another-site.com', // เพิ่ม domain ได้หลายอัน
];
```

> รองรับทุก path เช่น `your-site.com/login`, `your-site.com/dashboard` ก็ใช้ได้หมด

---

## 🖥️ วิธีใช้งาน

1. เปิดเว็บที่อยู่ใน whitelist
2. คลิกไอคอน 🔑 ที่ toolbar
3. กด **EXTRACT TOKEN**
4. Token จะปรากฏในกล่อง → กด **Copy** เพื่อคัดลอก

---

## ⚠️ หมายเหตุ

- Extension นี้ใช้ **Developer Mode** จึงอาจมี popup เตือนจาก Chrome ตอนเปิดเครื่อง ซึ่งเป็นเรื่องปกติ
- ใช้ได้เฉพาะ **Google Chrome** และ browser ที่ใช้ Chromium engine (Edge, Brave ฯลฯ)
- ไม่รองรับ Firefox

---

## 📁 โครงสร้างไฟล์

```
token-extractor-extension/
├── manifest.json    # Config ของ Extension
├── popup.html       # UI หน้าต่าง popup
├── popup.js         # Logic การดึง Token
└── icon.png         # ไอคอน
```

---

> Made with 💙 · โทนสี Pastel Blue
