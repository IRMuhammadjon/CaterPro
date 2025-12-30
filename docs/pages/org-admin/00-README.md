# Organization Admin (Tashkilot Administratori) Sahifalari

> Catering tashkilotini boshqaruvchi administratorlar uchun
> Xizmatlar, buyurtmalar, xodimlar, moliya boshqaruvi

## Sahifalar Ro'yxati

| # | Sahifa | Route | Tavsif |
|---|--------|-------|--------|
| 01 | Login | `/admin/login` | Admin kirish |
| 02 | Dashboard | `/admin/dashboard` | Bosh panel |
| 03 | Orders | `/admin/orders` | Buyurtmalar ro'yxati |
| 04 | Order Detail | `/admin/orders/:id` | Buyurtma tafsiloti |
| 05 | Services | `/admin/services` | Xizmatlar boshqaruvi |
| 06 | Service Edit | `/admin/services/:id` | Xizmat tahrirlash |
| 07 | Providers | `/admin/providers` | Xodimlar ro'yxati |
| 08 | Provider Detail | `/admin/providers/:id` | Xodim tafsiloti |
| 09 | Calendar | `/admin/calendar` | Umumiy kalendar |
| 10 | Finance | `/admin/finance` | Moliya boshqaruvi |
| 11 | Customers | `/admin/customers` | Mijozlar ro'yxati |
| 12 | Analytics | `/admin/analytics` | Analitika |
| 13 | Settings | `/admin/settings` | Sozlamalar |
| 14 | Chat | `/admin/chat` | Mijozlar bilan chat |

## Navigatsiya (Sidebar - Desktop)

```
┌─────────────────────┐
│  🍽️ Milliy Catering │
│     ADMIN PANEL     │
├─────────────────────┤
│                     │
│  📊 Dashboard       │
│  📦 Buyurtmalar     │
│  🍽️ Xizmatlar       │
│  👥 Xodimlar        │
│  📅 Kalendar        │
│  💰 Moliya          │
│  👤 Mijozlar        │
│  📈 Analitika       │
│  💬 Chat            │
│  ⚙️ Sozlamalar      │
│                     │
├─────────────────────┤
│  👤 Admin           │
│  🚪 Chiqish         │
└─────────────────────┘
```

## Navigatsiya (Mobile)

```
┌─────────────────────────────────────────────────────────────┐
│                                                             │
│     🏠          📦          📅          💬          ≡      │
│    Home       Orders     Calendar     Chat        Menu      │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

## Admin Roli

- Barcha buyurtmalarni boshqarish
- Xizmatlar va narxlarni sozlash
- Xodimlarni tayinlash
- Moliyaviy hisobotlarni ko'rish
- Mijozlar bilan muloqot
- Tashkilot sozlamalarini boshqarish
