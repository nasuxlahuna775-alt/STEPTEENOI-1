# ระบบจัดการค่าปรับแก๊ง (Fine Management System)

เว็บแอปหน้าเดียว (Single Page Web App) สำหรับบันทึกและจัดการค่าปรับ สร้างด้วย HTML + Tailwind CSS พร้อมไอคอน FontAwesome และ SweetAlert2

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
git commit -m "Initial commit: fine management system"
git branch -M main
git remote add origin https://github.com/<username>/<repo-name>.git
git push -u origin main
```

## 🛠 เทคโนโลยีที่ใช้

- HTML5
- Tailwind CSS (CDN)
- FontAwesome 6
- SweetAlert2
- Choices.js
- Google Fonts (Kanit)

## 📄 License

MIT
