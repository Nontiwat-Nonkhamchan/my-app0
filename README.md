# NextJs CRUD สำหรับข้อมูลนักศึกษา

ระบบจัดการข้อมูลนักศึกษา (Create / Read / Update / Delete) พัฒนาด้วย **Next.js (App Router)** และใช้ **Prisma + SQLite** เป็นฐานข้อมูล

## ✨ ฟีเจอร์

- ➕ เพิ่มข้อมูลนักศึกษาใหม่ (Create)
- 📋 แสดงรายชื่อนักศึกษาทั้งหมด (Read)
- ✏️ แก้ไขข้อมูลนักศึกษา (Update)
- 🗑️ ลบข้อมูลนักศึกษา (Delete)

## 🛠️ เทคโนโลยีที่ใช้

| เทคโนโลยี | รายละเอียด |
| --- | --- |
| [Next.js](https://nextjs.org) 16 | React Framework (App Router) |
| [React](https://react.dev) 19 | UI Library |
| [Prisma](https://www.prisma.io) | ORM สำหรับจัดการฐานข้อมูล |
| SQLite (better-sqlite3) | ฐานข้อมูลแบบไฟล์ (`dev.db`) |
| [Tailwind CSS](https://tailwindcss.com) 4 | จัดการ Style |

## 📁 โครงสร้างโปรเจกต์

```
my-app_1/
├── app/              # หน้าเว็บและ API routes (Next.js App Router)
├── prisma/           # Prisma schema
├── public/           # ไฟล์ static
├── dev.db            # ฐานข้อมูล SQLite
├── package.json
└── README.md
```

## ⚙️ สิ่งที่ต้องมีก่อนติดตั้ง

- [Node.js](https://nodejs.org) เวอร์ชัน 18 ขึ้นไป (แนะนำ LTS)
- npm (มาพร้อมกับ Node.js)
- [Git](https://git-scm.com)

## 🚀 วิธีการติดตั้ง

**1. Clone โปรเจกต์**

```bash
git clone https://github.com/Nattaphoom-Saensiriphokh/my-app_1.git
cd my-app_1
```

**2. ติดตั้ง dependencies**

```bash
npm install
```

**3. ตั้งค่าไฟล์ `.env`**

สร้างไฟล์ `.env` ไว้ที่โฟลเดอร์ root ของโปรเจกต์ แล้วใส่ค่าดังนี้

```env
DATABASE_URL="file:./dev.db"
```

**4. เตรียมฐานข้อมูลด้วย Prisma**

```bash
npx prisma generate
npx prisma db push
```

**5. รันโปรเจกต์ในโหมดพัฒนา**

```bash
npm run dev
```

เปิดเบราว์เซอร์ไปที่ [http://localhost:3000](http://localhost:3000)

## 📖 วิธีการใช้งาน

1. **ดูรายชื่อนักศึกษา** – เปิดหน้าแรกเพื่อดูข้อมูลนักศึกษาทั้งหมดในตาราง
2. **เพิ่มนักศึกษา** – กดปุ่มเพิ่มข้อมูล กรอกรายละเอียดนักศึกษา แล้วกดบันทึก
3. **แก้ไขข้อมูล** – กดปุ่มแก้ไขที่รายการที่ต้องการ แก้ไขข้อมูล แล้วกดบันทึก
4. **ลบข้อมูล** – กดปุ่มลบที่รายการที่ต้องการ แล้วยืนยันการลบ

## 📜 คำสั่งที่ใช้บ่อย

| คำสั่ง | ความหมาย |
| --- | --- |
| `npm run dev` | รันเซิร์ฟเวอร์สำหรับพัฒนา |
| `npm run build` | Build โปรเจกต์สำหรับ production |
| `npm run start` | รันโปรเจกต์ที่ build แล้ว |
| `npm run lint` | ตรวจสอบโค้ดด้วย ESLint |
| `npx prisma studio` | เปิดหน้าจัดการข้อมูลในฐานข้อมูลผ่านเบราว์เซอร์ |

## 👤 ผู้พัฒนา

- **Nattaphoom Saensiriphokh** – [GitHub](https://github.com/Nattaphoom-Saensiriphokh)

## 📚 อ้างอิง

- [Next.js Documentation](https://nextjs.org/docs)
- [Prisma Documentation](https://www.prisma.io/docs)
