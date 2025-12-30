# Provider (Xizmat ko'rsatuvchi) Sahifalari

> Catering xizmatlarini bajaruvchi xodimlar uchun
> Providerlar faqat o'zlariga tayinlangan vazifalarni ko'radi
> Mijoz ma'lumotlari (ism, telefon) ko'rinmaydi

## Sahifalar Ro'yxati

| # | Sahifa | Route | Tavsif |
|---|--------|-------|--------|
| 01 | Login | `/provider/login` | Tizimga kirish |
| 02 | Dashboard | `/provider/dashboard` | Bosh panel |
| 03 | My Tasks | `/provider/tasks` | Vazifalar ro'yxati |
| 04 | Task Detail | `/provider/tasks/:id` | Vazifa tafsiloti |
| 05 | Calendar | `/provider/calendar` | Ish kalendari |
| 06 | Earnings | `/provider/earnings` | Daromadlar |
| 07 | Profile | `/provider/profile` | Shaxsiy kabinet |
| 08 | Notifications | `/provider/notifications` | Bildirishnomalar |

## Navigatsiya (Mobile)

```
┌─────────────────────────────────────────────────────────────┐
│                                                             │
│     🏠          📋          📅          💰          👤     │
│    Home        Tasks      Calendar    Earnings    Profile   │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

## Provider Roli

- Tashkilot tomonidan tayinlanadi
- Faqat o'z vazifalarini ko'radi
- Mijoz shaxsiy ma'lumotlarini ko'rmaydi
- Vazifa statusini yangilashi mumkin
- O'z daromadlarini kuzatadi
