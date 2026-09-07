# UI Prototype

ตัวอย่างโครงหน้า Project Info ด้วย TypeScript, React และ Vinext สำหรับทบทวนหน้าตา เมนู และภาษาไทย/อังกฤษ ใช้ข้อมูลจำลองและบทบาท Demo Admin เท่านั้น ยังไม่เชื่อม PostgreSQL หรือระบบบัญชีจริง

## Local development

ใช้ Node.js ตาม `engines` ใน `package.json` และ pnpm พร้อม lockfile ที่แนบมา

```text
cd prototype
pnpm install
pnpm dev --host 127.0.0.1
```

หาก pnpm ขออนุมัติ dependency build scripts ให้ตรวจรายการด้วย `pnpm approve-builds` และอนุมัติเฉพาะรายการที่เชื่อถือได้ก่อนติดตั้งต่อ ค่าใน `pnpm-workspace.yaml` จาก scaffold ยังรอการตัดสินใจส่วนนี้

## Validation and limitations

- TypeScript check ผ่านในเครื่องมือที่สร้าง prototype: `node node_modules/typescript/bin/tsc --noEmit`
- การติดตั้งหยุดด้วย `ERR_PNPM_IGNORED_BUILDS` สำหรับ esbuild, sharp และ workerd
- การเปิด dev server ถูกจำกัดการสร้าง process และคำขออนุญาตรันถูกปฏิเสธ จึงยังไม่ยืนยันการแสดงผลหรือ interaction ในเบราว์เซอร์
- Production build และ lint ยังไม่ได้ตรวจ ต้องตรวจหลังเตรียม dependencies บนเครื่องพัฒนาให้พร้อม
- ปุ่มเพิ่มลูกค้าและออกจากระบบแสดงข้อความจำลอง ไม่มีการบันทึกข้อมูลหรือ session จริง
- Prototype ยังไม่ครบทุก acceptance criterion ใน [App Layout](../docs/ui/app-layout.md) โดยเฉพาะการจำลองหลายบทบาทและการตรวจ UI บนหลายขนาดจอ

คำสั่งตรวจเมื่อพร้อม: `pnpm exec tsc --noEmit`, `pnpm lint` และ `pnpm build`
