# CaterPro - Pages Documentation

> Catering Automation System - SaaS Platform
> Vizual sahifa dokumentatsiyasi

## Platform Haqida

CaterPro - bu catering xizmatlarini boshqarish uchun SaaS platformasi. Tashkilotlar platformaga obuna bo'lib, o'z catering bizneslarini boshqaradi.

## Biznes Model

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                                                                             │
│                           🔷 CaterPro Platform                              │
│                           (Super Admin - Siz)                               │
│                                                                             │
│    ┌──────────────────┐  ┌──────────────────┐  ┌──────────────────┐        │
│    │ 🏢 Tashkilot 1   │  │ 🏢 Tashkilot 2   │  │ 🏢 Tashkilot 3   │        │
│    │ milliy.caterpro  │  │ sharq.caterpro   │  │ premium.caterpro │        │
│    │                  │  │                  │  │                  │        │
│    │  ┌────────────┐  │  │  ┌────────────┐  │  │  ┌────────────┐  │        │
│    │  │ 👤 Mijozlar│  │  │  │ 👤 Mijozlar│  │  │  │ 👤 Mijozlar│  │        │
│    │  └────────────┘  │  │  └────────────┘  │  │  └────────────┘  │        │
│    │  ┌────────────┐  │  │  ┌────────────┐  │  │  ┌────────────┐  │        │
│    │  │ 👥 Xodimlar│  │  │  │ 👥 Xodimlar│  │  │  │ 👥 Xodimlar│  │        │
│    │  └────────────┘  │  │  └────────────┘  │  │  └────────────┘  │        │
│    │                  │  │                  │  │                  │        │
│    └──────────────────┘  └──────────────────┘  └──────────────────┘        │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

## Foydalanuvchi Turlari

| # | Turi | Tavsif | Folder |
|---|------|--------|--------|
| 1 | **User (Mijoz)** | Xizmatdan foydalanuvchi oddiy foydalanuvchilar | [/user](./user/) |
| 2 | **Provider (Xodim)** | Catering xizmatlarini bajaruvchi xodimlar | [/provider](./provider/) |
| 3 | **Org Admin** | Tashkilot administratorlari | [/org-admin](./org-admin/) |
| 4 | **Super Admin** | Platforma egasi (Siz) | [/super-admin](./super-admin/) |

## Muhim Tushuncha

```
⚠️ MUHIM: Mijozlar xizmat ko'rsatuvchilarni to'g'ridan-to'g'ri tanlaMaydi!

NOTO'G'RI:
Mijoz → Xizmat ko'rsatuvchini tanlaydi → Buyurtma beradi

TO'G'RI:
Mijoz → XIZMAT PAKETINI tanlaydi → Buyurtma beradi → Tashkilot xodimlarni tayinlaydi
```

## Xizmat Darajalari

| Daraja | Narx oralig'i | Xususiyatlari |
|--------|---------------|---------------|
| ⭐ Start | 50,000 so'm/kishi | Asosiy taomlar, minimal xizmat |
| ⭐⭐ Comfort | 70,000 so'm/kishi | Ko'proq taom, professional xizmat |
| ⭐⭐⭐ Premium | 85,000 so'm/kishi | Premium menyu, to'liq xizmat |
| ⭐⭐⭐⭐ Business | 120,000 so'm/kishi | VIP xizmat, maxsus taomlar |

## Obuna Rejalari (Tashkilotlar uchun)

| Reja | Narx | Buyurtmalar | Xodimlar |
|------|------|-------------|----------|
| Starter | Bepul | 50/oy | 3 ta |
| Basic | 299,000/oy | 200/oy | 10 ta |
| Premium | 599,000/oy | Cheksiz | 50 ta |
| Enterprise | Kelishuv | Cheksiz | Cheksiz |

## Sahifalar Tuzilishi

```
docs/pages/
├── README.md (shu fayl)
├── user/                    # Mijoz sahifalari
│   ├── 00-README.md
│   ├── 01-welcome.md
│   ├── 02-login.md
│   ├── 03-register.md
│   ├── 05-home.md
│   ├── 06-services.md
│   ├── 07-service-detail.md
│   ├── 08-booking.md
│   ├── 10-orders.md
│   └── 11-order-detail.md
├── provider/                # Xodim sahifalari
│   ├── 00-README.md
│   ├── 01-login.md
│   ├── 02-dashboard.md
│   ├── 03-tasks.md
│   ├── 04-task-detail.md
│   ├── 05-calendar.md
│   ├── 06-earnings.md
│   ├── 07-profile.md
│   └── 08-notifications.md
├── org-admin/               # Tashkilot admin sahifalari
│   ├── 00-README.md
│   ├── 01-login.md
│   ├── 02-dashboard.md
│   ├── 03-orders.md
│   ├── 04-order-detail.md
│   ├── 05-services.md
│   ├── 06-service-edit.md
│   ├── 07-providers.md
│   ├── 08-provider-detail.md
│   ├── 09-calendar.md
│   ├── 10-finance.md
│   ├── 11-customers.md
│   ├── 12-analytics.md
│   ├── 13-settings.md
│   └── 14-chat.md
└── super-admin/             # Super admin sahifalari
    ├── 00-README.md
    ├── 01-login.md
    ├── 02-dashboard.md
    ├── 03-organizations.md
    ├── 04-organization-detail.md
    ├── 05-create-organization.md
    ├── 06-subscriptions.md
    ├── 07-payments.md
    ├── 08-analytics.md
    ├── 09-reports.md
    ├── 10-settings.md
    └── 11-support.md
```

## Vizual Dokumentatsiya Formati

Har bir sahifa quyidagilarni o'z ichiga oladi:

1. **Route** - Sahifa manzili
2. **Auth** - Autentifikatsiya talabi
3. **Vizual Ko'rinish** - ASCII diagramma
4. **Elementlar jadvali** - Barcha UI elementlar
5. **Navigatsiya** - Qaysi tugma qayerga olib boradi (→ belgisi bilan)

Misol:
```
┌───────────────────────────────────────────────────────┐
│  ┌─────────────────────────────────────────────────┐ │
│  │         [  👁️ Batafsil ko'rish  ]             │ │──► /orders/:id
│  └─────────────────────────────────────────────────┘ │
└───────────────────────────────────────────────────────┘
```

## Texnologiyalar (Tavsiya)

- **Frontend**: React/Next.js, TypeScript
- **Mobile**: React Native / Flutter
- **Backend**: Node.js / NestJS
- **Database**: PostgreSQL
- **Realtime**: Socket.io
- **Payments**: Click, Payme
- **Maps**: Google Maps / Yandex Maps
