# เว็บเช็กชื่อ (Modern Attendance System)

เว็บแอปหน้าเดียว (Single Page Web App) สำหรับเช็กชื่อ / บันทึกการเข้าเรียน ออกแบบทันสมัยด้วย HTML + CSS ล้วน พร้อมไอคอน FontAwesome และฟอนต์ Kanit

## 🚀 การใช้งาน

เปิดไฟล์ `index.html` ด้วยเบราว์เซอร์ได้เลย ไม่ต้องติดตั้งอะไรเพิ่ม

## 🌐 เผยแพร่ด้วย GitHub Pages

### วิธีที่ 1: อัตโนมัติด้วย GitHub Actions (แนะนำ)

โปรเจกต์นี้มีไฟล์ `.github/workflows/deploy.yml` มาให้แล้ว เพียงเข้าไปที่ **Settings → Pages → Source** แล้วเลือก **GitHub Actions** จากนั้นทุกครั้งที่ push ขึ้น `main` เว็บจะเดพลอยใหม่อัตโนมัติ

### วิธีที่ 2: ตั้งค่าแบบเดิม

1. ไปที่ **Settings → Pages**
2. ที่หัวข้อ **Source** เลือก **Deploy from a branch** → Branch `main` → โฟลเดอร์ `/ (root)`
3. กด **Save** แล้วรอสักครู่ เว็บจะออนไลน์ที่ `https://<username>.github.io/<repo-name>/`

## 📦 วิธีอัปโหลดขึ้น GitHub (ผ่านคำสั่ง Git)

```bash
git init
git add .
git commit -m "Initial commit: attendance system"
git branch -M main
git remote add origin https://github.com/<username>/<repo-name>.git
git push -u origin main
```

## 🔥 ทำให้เพื่อเห็นข้อมูลร่วมกัน (ตั้งค่า Firebase)

> โดยค่าเริ่มต้น เว็บเก็บข้อมูลไว้ในเครื่องของแต่ละคนเท่านั้น (LocalStorage) เพื่อนจึงมองไม่เห็นข้อมูลเดียวกัน ถ้าอยากให้ทุกคนเห็นข้อมูลชุดเดียวกัน ให้ตั้งค่า Firebase ตามขั้นตอนด้านล่าง (ฟรี)

1. ไปที่ <https://console.firebase.google.com> → **Add project** สร้างโปรเจกต์ใหม่ (จะปิด Google Analytics ก็ได้)
2. เมนูซ้าย → **Build → Realtime Database** → **Create Database** → เลือกโซนใกล้คุณ → เลือก **Start in test mode** → Enable
3. ไปที่ **Project settings** (ไอคอนเฟืองมุมขวาบน) → เลื่อนลงมาส่วน **Your apps** → กดไอคอน **</>** (Web) → ตั้งชื่อแอป → Register
4. คัดลอกค่า `firebaseConfig` ที่ได้มา นำไปวางแทนในไฟล์ `index.html` ตรงส่วน `const FIREBASE_CONFIG = { ... }` (แทนค่า `PASTE_...` ทั้งหมด)
   - สำคัญ: ต้องมีบรรทัด `databaseURL` ด้วย (เช่น `https://xxxx-default-rtdb.firebaseio.com`) — ถ้าค่า config ที่คัดมาไม่มี ให้คัดจากหน้า Realtime Database มาใส่เอง
5. บันทึกและ push ขึ้น GitHub — เสร็จแล้ว! ทุกคนที่เปิดลิงก์เดียวกันจะเห็นและแก้ข้อมูลชุดเดียวกันแบบเรียลไทม์

> ⚠️ **ข้อควรระวังเรื่องความปลอดภัย:** โหมด test mode เปิดให้ใครก็ตามที่มีลิงก์อ่าน/เขียนข้อมูลได้ เหมาะกับกลุ่มเพื่อนเล็ก ๆ เท่านั้น อย่าใส่ข้อมูลสำคัญ/ความลับ หากต้องการความปลอดภัยมากขึ้น ควรตั้ง Rules / ระบบล็อกอินเพิ่ม

## 🛠 เทคโนโลยีที่ใช้

- HTML5
- CSS3
- FontAwesome 6
- Google Fonts (Kanit)
- Firebase Realtime Database (ทางเลือก — สำหรับแชร์ข้อมูลข้ามเครื่อง)

## 📄 License

MIT
