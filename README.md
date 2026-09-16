# เว็บเช็กชื่อ (Check Name)

เว็บแอปเช็กชื่อ / เช็กชื่อเข้าเรียน ทำงานได้ทั้งคอมและมือถือ ไม่ต้องติดตั้งอะไร

## คุณสมบัติ
- ➕ เพิ่มหัวข้อใหม่ได้ไม่จำกัด (ห้อง/คลาส/กิจกรรม)
- 👤 เพิ่ม/ลบรายชื่อ และเช็กสถานะ มา / ขาด / ลา
- 📊 สรุปยอดอัตโนมัติ
- 🎲 สุ่มแบ่งกลุ่ม (สูงสุด 5 กลุ่ม)
- 📨 ส่งผลเข้า Discord ได้ (แต่ละหัวข้อตั้ง Webhook แยกกันได้)
- 💾 บันทึกข้อมูลอัตโนมัติในเครื่อง (localStorage)

## วิธีนำขึ้น GitHub Pages

### แบบง่าย (ผ่านเว็บ GitHub)
1. ไปที่ https://github.com/new → ตั้งชื่อ repo เช่น `check-name` → Create repository
2. ในหน้า repo → กด **Add file → Upload files** → ลากไฟล์ `index.html` (และ `README.md`) ลงไป → Commit changes
3. ไปที่ **Settings → Pages** → ช่อง Branch เลือก `main` → โฟลเดอร์ `/ (root)` → Save
4. รอสักครู่ เว็บจะออนไลน์ที่ `https://<username>.github.io/check-name/`

### แบบใช้ Git (คำสั่ง)
```bash
git init
git add index.html README.md
git commit -m "Add check-name web app"
git branch -M main
git remote add origin https://github.com/<username>/check-name.git
git push -u origin main
```
จากนั้นเปิด GitHub Pages ใน Settings → Pages ตามขั้นตอนข้างบน

> ℹ️ ไฟล์ต้องชื่อ `index.html` เท่านั้น GitHub Pages ถึงจะเปิดหน้าแรกให้อัตโนมัติ
