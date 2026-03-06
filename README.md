# danny-api-tester

Workspace สำหรับทดสอบ API ด้วย [Bruno](https://www.usebruno.com/) (รูปแบบ OpenCollection 1.0.0)

## Collections

| Collection   | คำอธิบาย |
|-------------|----------|
| **BigData** | API ชุด Big Data — login, company, auditor, financial, GHG, project, IOT, Carbon Credit, ฯลฯ (ใช้ cookies หลัง login) |
| **NEW DEMP** | API ชุด DEMP — AUTH, Profile, Auditor Register, ฯลฯ |

## วิธีใช้

1. ติดตั้ง [Bruno](https://www.usebruno.com/downloads) (CLI หรือ GUI)
2. เปิด workspace นี้ใน Bruno (โฟลเดอร์ที่มี `workspace.yml`)
3. สำหรับ **BigData**: login ก่อน แล้ว Bruno จะ set cookies ให้อัตโนมัติ
4. สลับ base URL ตาม environment ได้ใน collection (DEV / LOCALHOST / PROD)

## โครงสร้าง

```
danny-api-tester/
├── workspace.yml      # กำหนด collections และ docs
├── README.md
└── collections/
    ├── BigData/
    └── NEW DEMP/
```

## หมายเหตุ

- Big Data API ใช้ cookies ใน headers — หลัง login แล้วจะ autoset cookies สำหรับ request ถัดไป
- ใช้สำหรับรัน request, ตรวจ response และทดสอบ flow ระหว่าง dev / localhost / prod
