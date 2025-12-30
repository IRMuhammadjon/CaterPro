# CaterPro - Super Admin (Platforma Egasi) Sahifalari

> CaterPro platformasi egasi (Siz) uchun barcha sahifalar
> Barcha tashkilotlarni boshqarish, monitoring va analitika

---

## 1. Autentifikatsiya

### 1.1 Super Admin Login
```
Route: /super-admin/login
yoki
Route: https://admin.caterpro.uz/login
```

| Element | Tavsif |
|---------|--------|
| Logo | CaterPro Admin logo |
| Email | Super admin email |
| Parol | Maxfiy parol |
| 2FA | Ikki bosqichli tasdiqlash (majburiy) |
| Kirish | Login tugmasi |
| Security log | Kirish tarixini ko'rish |

**Xavfsizlik:**
- IP whitelist
- 2FA majburiy
- Session timeout: 30 min
- Failed login alert

---

## 2. Main Dashboard

### 2.1 Super Admin Dashboard
```
Route: /super-admin/dashboard
```

| Section | Elementlar |
|---------|------------|
| Header | Logo, Global search, Notifications, Admin profil |
| Welcome | "Super Admin Dashboard" |
| Platform stats | 8 ta asosiy metrika |
| Revenue chart | Platform daromadi |
| Organizations map | Geografik joylashuv |
| Recent activity | So'nggi harakatlar |
| Alerts | Muhim ogohlantirishlar |

**Asosiy metrikalar:**
```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    CATERPRO PLATFORM DASHBOARD                              │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  ┌──────────┐ ┌──────────┐ ┌──────────┐ ┌──────────┐                      │
│  │ 🏢 47    │ │ 📦 1,234 │ │ 💰 156M  │ │ 👥 4,521 │                      │
│  │Tashkilot │ │Buyurtma  │ │Aylanma   │ │Mijozlar  │                      │
│  │ ↑ 5      │ │ ↑ 12%    │ │ ↑ 18%    │ │ ↑ 234    │                      │
│  └──────────┘ └──────────┘ └──────────┘ └──────────┘                      │
│                                                                             │
│  ┌──────────┐ ┌──────────┐ ┌──────────┐ ┌──────────┐                      │
│  │ 🧑‍🍳 892  │ │ 💵 112M  │ │ 📈 95.9M │ │ ⭐ 4.7   │                      │
│  │Provider  │ │Obuna     │ │Sof foyda │ │O'rtacha  │                      │
│  │ ↑ 45     │ │daromad   │ │(sizning) │ │reyting   │                      │
│  └──────────┘ └──────────┘ └──────────┘ └──────────┘                      │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

### 2.2 Real-time Activity
```
Dashboard ichida
```

| Event | Tavsif |
|-------|--------|
| 🆕 Yangi tashkilot | "Farg'ona Food" ro'yxatdan o'tdi |
| 📦 Buyurtma | "Milliy Catering" #234 buyurtma oldi |
| 💰 To'lov | "Lux Event" oylik obuna to'ladi |
| ⚠️ Alert | "Andijon Catering" obunasi tugaydi |

---

## 3. Tashkilotlar Boshqaruvi

### 3.1 Organizations List (Tashkilotlar ro'yxati)
```
Route: /super-admin/organizations
```

**Filtrlar:**
| Filter | Variantlar |
|--------|------------|
| Status | Faol, Nofaol, Trial, Suspended |
| Obuna | Enterprise, Premium, Basic, Starter, Trial |
| Shahar | Lokatsiya bo'yicha |
| Ro'yxatdan | Sana oralig'i |
| Aylanma | Summa oralig'i |

**Jadval:**
| Ustun | Tavsif |
|-------|--------|
| ID | Tashkilot ID |
| Nomi | Tashkilot nomi |
| Subdomain | xxx.caterpro.uz |
| Obuna | Tarif turi |
| Buyurtmalar | Bu oydagi |
| Aylanma | Umumiy aylanma |
| Foyda | Tashkilot foydasi |
| Obuna tugashi | Qachon |
| Status | Faol/Nofaol |
| Actions | Ko'rish, Tahrirlash, Login as |

**Quick Actions:**
| Tugma | Tavsif |
|-------|--------|
| ➕ Yangi tashkilot | Tashkilot yaratish |
| 📧 Bulk email | Hammaga xabar |
| 📊 Export | Ma'lumotlarni yuklab olish |

---

### 3.2 Organization Detail (Tashkilot tafsiloti)
```
Route: /super-admin/organizations/:id
```

| Tab | Elementlar |
|-----|------------|
| Overview | Umumiy ko'rinish |
| Statistics | Statistika |
| Subscription | Obuna ma'lumotlari |
| Team | Adminlar |
| Settings | Sozlamalar |
| Logs | Faoliyat tarixi |

**Overview:**
```
┌─────────────────────────────────────────────────────────────────────────────┐
│  🏢 MILLIY CATERING                                        [Faol] [Premium]│
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  📍 Toshkent, O'zbekiston                                                  │
│  📞 +998 71 123 45 67                                                      │
│  ✉️  info@milliy-catering.uz                                               │
│  🌐 milliy-catering.caterpro.uz                                            │
│                                                                             │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │                      BU OYDAGI KO'RSATKICHLAR                       │   │
│  ├─────────────────────────────────────────────────────────────────────┤   │
│  │  📦 Buyurtmalar:     234 ta      │  💰 Aylanma:    45,200,000      │   │
│  │  👥 Mijozlar:        156 ta      │  💵 Foyda:      12,400,000      │   │
│  │  🧑‍🍳 Providerlar:     23 ta      │  📊 Margin:     27.4%           │   │
│  │  ⭐ Reyting:         4.7/5       │  📈 O'sish:     +18%            │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│                                                                             │
│  📅 Ro'yxatdan o'tgan: 15-Mart 2024                                        │
│  📅 Obuna tugaydi: 15-Fevral 2025 (18 kun qoldi)                           │
│                                                                             │
│  [🔑 Login as Admin]  [✏️ Tahrirlash]  [⏸️ To'xtatish]  [🗑️ O'chirish]     │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

### 3.3 Create Organization (Tashkilot yaratish)
```
Route: /super-admin/organizations/create
```

**Step 1: Asosiy ma'lumotlar**
| Field | Tavsif |
|-------|--------|
| Tashkilot nomi | Kompaniya nomi |
| Subdomain | xxx.caterpro.uz |
| Email | Admin email |
| Telefon | Aloqa |
| Shahar | Lokatsiya |
| Manzil | To'liq manzil |

**Step 2: Admin yaratish**
| Field | Tavsif |
|-------|--------|
| Admin ismi | To'liq ism |
| Email | Login email |
| Telefon | +998 XX XXX XX XX |
| Parol | Vaqtinchalik parol |

**Step 3: Obuna tanlash**
| Field | Tavsif |
|-------|--------|
| Tarif | Starter/Basic/Premium/Enterprise |
| Davr | Oylik/Yillik |
| Trial | Bepul sinov davri |
| Chegirma | Maxsus chegirma % |

**Step 4: Sozlamalar**
| Field | Tavsif |
|-------|--------|
| Custom domain | (Premium+) Maxsus domen |
| White label | (Enterprise) Branding |
| API access | API ruxsati |
| Features | Maxsus xususiyatlar |

---

### 3.4 Login as Organization
```
Route: /super-admin/organizations/:id/impersonate
```

| Element | Tavsif |
|---------|--------|
| Ogohlantirish | "Tashkilot panelida ishlayapsiz" |
| Tashkilot panel | To'liq admin panel |
| Chiqish | Super admin ga qaytish |
| Log | Barcha harakatlar loglanadi |

---

### 3.5 Organization Subscription Management
```
Route: /super-admin/organizations/:id/subscription
```

| Element | Tavsif |
|---------|--------|
| Joriy tarif | Hozirgi obuna |
| Tarif o'zgartirish | Upgrade/Downgrade |
| Muddat uzaytirish | Extend subscription |
| Chegirma berish | Maxsus chegirma |
| Bepul oy | Bonus period |
| To'lov tarixi | Payment history |

---

## 4. Obunalar va To'lovlar

### 4.1 Subscriptions Overview
```
Route: /super-admin/subscriptions
```

**Obuna statistikasi:**
```
┌─────────────────────────────────────────────────────────────────────────────┐
│                        OBUNA STATISTIKASI                                   │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  TARIF BO'YICHA TAQSIMOT                                                   │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │  💎 Enterprise:  3 ta  (6%)   │  ████                              │   │
│  │  🥇 Premium:    12 ta (26%)   │  ████████████                      │   │
│  │  🥈 Basic:      18 ta (38%)   │  ██████████████████                │   │
│  │  🥉 Starter:    14 ta (30%)   │  ███████████████                   │   │
│  │  🆓 Trial:       8 ta         │  (hisoblanmaydi)                   │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│                                                                             │
│  OYLIK DAROMAD (MRR)                                                       │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │  Enterprise (3):   3 × 10,000,000  =   30,000,000 so'm             │   │
│  │  Premium (12):    12 ×  3,999,000  =   47,988,000 so'm             │   │
│  │  Basic (18):      18 ×  1,499,000  =   26,982,000 so'm             │   │
│  │  Starter (14):    14 ×    499,000  =    6,986,000 so'm             │   │
│  │  ─────────────────────────────────────────────────────────         │   │
│  │  JAMI MRR:                            111,956,000 so'm             │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

### 4.2 Subscription List
```
Route: /super-admin/subscriptions/list
```

| Filter | Variantlar |
|--------|------------|
| Tarif | Enterprise, Premium, Basic, Starter |
| Status | Faol, Tugayapti, Muddati o'tgan |
| Auto-renew | Ha/Yo'q |

**Jadval:**
| Tashkilot | Tarif | Boshlanish | Tugash | Summa | Auto | Status |
|-----------|-------|------------|--------|-------|------|--------|
| Milliy Catering | Premium | 15-Yan | 15-Fev | 3.99M | ✅ | 🟢 |
| Lux Event | Business | 01-Yan | 01-Fev | 10M | ✅ | 🟢 |
| Toshkent Food | Basic | 20-Dek | 20-Yan | 1.49M | ❌ | 🟡 |

---

### 4.3 Payments (To'lovlar)
```
Route: /super-admin/payments
```

| Filter | Variantlar |
|--------|------------|
| Status | Muvaffaqiyatli, Kutilmoqda, Rad |
| Tur | Obuna, Bir martalik, Refund |
| Usul | Click, Payme, Bank |
| Sana | Date range |

**Jadval:**
| ID | Sana | Tashkilot | Tur | Summa | Usul | Status |
|----|------|-----------|-----|-------|------|--------|
| #1234 | 25-Yan | Milliy Catering | Obuna | 3,999,000 | Click | ✅ |
| #1233 | 24-Yan | Lux Event | Obuna | 10,000,000 | Bank | ✅ |
| #1232 | 23-Yan | Andijon Catering | Obuna | 499,000 | Payme | ❌ |

---

### 4.4 Revenue Analytics
```
Route: /super-admin/payments/analytics
```

| Metrika | Qiymat | O'zgarish |
|---------|--------|-----------|
| MRR | 111.9M | ↑ 8% |
| ARR | 1.34B | ↑ 12% |
| ARPU | 2.38M | ↑ 3% |
| Churn | 4.2% | ↓ 1% |
| LTV | 28.5M | ↑ 5% |

**Grafiklar:**
- MRR trend (line chart)
- Revenue by plan (pie chart)
- Churn analysis (bar chart)
- Cohort retention (heatmap)

---

### 4.5 Expiring Subscriptions
```
Route: /super-admin/subscriptions/expiring
```

| Element | Tavsif |
|---------|--------|
| 7 kun ichida | Tez tugayadiganlar |
| 30 kun ichida | Yaqin orada |
| Eslatma yuborish | Bulk notification |
| Chegirma taklifi | Retention offer |

---

## 5. Foydalanuvchilar Boshqaruvi

### 5.1 All Users
```
Route: /super-admin/users
```

| Tab | Tavsif |
|-----|--------|
| Org Admins | Tashkilot adminlari |
| Providers | Xizmat ko'rsatuvchilar |
| Customers | Oxirgi foydalanuvchilar |

**Filtrlar:**
| Filter | Variantlar |
|--------|------------|
| Tashkilot | Qaysi tashkilotda |
| Rol | Admin, Provider, Customer |
| Status | Faol, Nofaol, Banned |
| Sana | Ro'yxatdan o'tgan |

---

### 5.2 User Detail
```
Route: /super-admin/users/:id
```

| Section | Elementlar |
|---------|------------|
| Profil | Shaxsiy ma'lumotlar |
| Faoliyat | Harakat tarixi |
| Tashkilot | Qayerda ishlaydi |
| Ruxsatlar | Permissions |
| Sessions | Faol sessiyalar |

**Actions:**
| Tugma | Tavsif |
|-------|--------|
| Ban | Foydalanuvchini bloklash |
| Reset password | Parol tiklash |
| Force logout | Sessiyalarni tugatish |
| Delete | O'chirish |

---

## 6. Platform Analitika

### 6.1 Analytics Dashboard
```
Route: /super-admin/analytics
```

| Section | Elementlar |
|---------|------------|
| Overview | Umumiy metrikalar |
| Growth | O'sish ko'rsatkichlari |
| Engagement | Foydalanish statistikasi |
| Geographic | Geografik taqsimot |
| Performance | Tizim ishlashi |

---

### 6.2 Platform Metrics
```
Route: /super-admin/analytics/metrics
```

**O'sish ko'rsatkichlari:**
| Metrika | Bu oy | O'tgan oy | O'zgarish |
|---------|-------|-----------|-----------|
| Yangi tashkilotlar | 5 | 3 | ↑ 67% |
| Yangi providerlar | 89 | 67 | ↑ 33% |
| Yangi mijozlar | 456 | 389 | ↑ 17% |
| Buyurtmalar | 1,234 | 1,089 | ↑ 13% |
| GMV | 156M | 134M | ↑ 16% |

---

### 6.3 Geographic Analytics
```
Route: /super-admin/analytics/geo
```

| Shahar | Tashkilotlar | Buyurtmalar | Aylanma |
|--------|--------------|-------------|---------|
| Toshkent | 28 | 678 | 89M |
| Samarqand | 8 | 234 | 28M |
| Buxoro | 5 | 156 | 18M |
| Farg'ona | 3 | 89 | 12M |
| Boshqa | 3 | 77 | 9M |

**Xarita vizualizatsiya:**
- Interactive map
- Marker size = Aylanma
- Color = Tashkilotlar soni

---

### 6.4 Performance Metrics
```
Route: /super-admin/analytics/performance
```

| Metrika | Qiymat | Target |
|---------|--------|--------|
| Uptime | 99.9% | 99.5% |
| Avg response | 145ms | 200ms |
| Error rate | 0.02% | 0.1% |
| Active users | 2,341 | - |
| Peak load | 567 req/s | - |

---

## 7. Hisobotlar

### 7.1 Reports Center
```
Route: /super-admin/reports
```

| Report | Tavsif |
|--------|--------|
| Revenue Report | Daromad hisoboti |
| Organization Report | Tashkilotlar hisoboti |
| User Growth | Foydalanuvchi o'sishi |
| Subscription Report | Obuna hisoboti |
| Churn Analysis | Ketish tahlili |
| Custom Report | Maxsus hisobot |

---

### 7.2 Revenue Report
```
Route: /super-admin/reports/revenue
```

| Manba | Bu oy | O'tgan oy | O'zgarish |
|-------|-------|-----------|-----------|
| Obuna to'lovlari | 111.9M | 103.4M | ↑ 8% |
| Server xarajatlari | -5M | -4.8M | ↑ 4% |
| Marketing | -8M | -7M | ↑ 14% |
| Support | -3M | -2.8M | ↑ 7% |
| **Sof foyda** | **95.9M** | **88.8M** | **↑ 8%** |

---

### 7.3 Organization Performance Report
```
Route: /super-admin/reports/organizations
```

**Top 10 tashkilotlar:**
| # | Tashkilot | Buyurtmalar | Aylanma | Foyda |
|---|-----------|-------------|---------|-------|
| 1 | Milliy Catering | 234 | 45.2M | 12.4M |
| 2 | Lux Event | 189 | 38.7M | 10.1M |
| 3 | Samarqand Osh | 145 | 28.9M | 7.8M |
| 4 | Premium Food | 112 | 22.1M | 5.9M |
| 5 | Namangan Catering | 98 | 18.5M | 4.8M |

---

### 7.4 Scheduled Reports
```
Route: /super-admin/reports/scheduled
```

| Report | Chastotasi | Qabul qiluvchilar | Format |
|--------|------------|-------------------|--------|
| Daily Summary | Kunlik | admin@caterpro.uz | Email |
| Weekly Revenue | Haftalik | finance@caterpro.uz | PDF |
| Monthly Full | Oylik | ceo@caterpro.uz | Excel |

---

## 8. Tizim Sozlamalari

### 8.1 Platform Settings
```
Route: /super-admin/settings
```

| Tab | Elementlar |
|-----|------------|
| General | Umumiy sozlamalar |
| Pricing | Tarif narxlari |
| Features | Xususiyatlar |
| Email | Email sozlamalari |
| Notifications | Bildirishnomalar |
| Security | Xavfsizlik |
| API | API sozlamalari |

---

### 8.2 Pricing Configuration
```
Route: /super-admin/settings/pricing
```

| Tarif | Oylik | Yillik | Xususiyatlar |
|-------|-------|--------|--------------|
| Starter | 499,000 | 4,990,000 | [Edit] |
| Basic | 1,499,000 | 14,990,000 | [Edit] |
| Premium | 3,999,000 | 39,990,000 | [Edit] |
| Enterprise | Kelishuv | Kelishuv | [Edit] |

**Har bir tarif uchun:**
| Limit | Starter | Basic | Premium | Enterprise |
|-------|---------|-------|---------|------------|
| Buyurtmalar/oy | 50 | 200 | ∞ | ∞ |
| Providerlar | 20 | 100 | ∞ | ∞ |
| Adminlar | 3 | 10 | ∞ | ∞ |
| Analitika | ❌ | Oddiy | To'liq | Custom |
| API | ❌ | ❌ | ✅ | ✅ |
| White label | ❌ | ❌ | ❌ | ✅ |

---

### 8.3 Feature Flags
```
Route: /super-admin/settings/features
```

| Feature | Status | Tavsif |
|---------|--------|--------|
| new_dashboard | 🟢 On | Yangi dashboard |
| ai_reports | 🟡 Beta | AI hisobotlar |
| mobile_app | 🔴 Off | Mobil ilova |
| telegram_bot | 🟢 On | Telegram bot |
| advanced_analytics | 🟢 On | Kengaytirilgan analitika |

---

### 8.4 Email Templates
```
Route: /super-admin/settings/emails
```

| Template | Tavsif |
|----------|--------|
| Welcome | Ro'yxatdan o'tganda |
| Subscription | Obuna to'langan |
| Expiring | Obuna tugayapti |
| Expired | Obuna tugadi |
| Password reset | Parol tiklash |
| Invoice | Hisob-faktura |

**Template Editor:**
| Element | Tavsif |
|---------|--------|
| Subject | Email mavzusi |
| Body | HTML editor |
| Variables | Dinamik o'zgaruvchilar |
| Preview | Ko'rib chiqish |
| Test send | Test yuborish |

---

### 8.5 Security Settings
```
Route: /super-admin/settings/security
```

| Setting | Qiymat |
|---------|--------|
| 2FA | Majburiy (Super Admin) |
| Session timeout | 30 min |
| Password policy | Strong |
| IP whitelist | [Manage] |
| Login attempts | 5 marta |
| Audit logging | ✅ Yoqilgan |

---

### 8.6 API Configuration
```
Route: /super-admin/settings/api
```

| Element | Tavsif |
|---------|--------|
| API versiyasi | v1, v2 |
| Rate limiting | 1000 req/min |
| Webhooks | Event callbacks |
| API keys | Master keys |
| Documentation | API docs link |

---

## 9. Monitoring va Logs

### 9.1 System Health
```
Route: /super-admin/monitoring
```

| Service | Status | Uptime | Response |
|---------|--------|--------|----------|
| API Server | 🟢 | 99.99% | 45ms |
| Database | 🟢 | 99.98% | 12ms |
| Redis | 🟢 | 99.99% | 2ms |
| File Storage | 🟢 | 99.95% | 89ms |
| Payment Gateway | 🟢 | 99.90% | 234ms |
| SMS Service | 🟡 | 98.50% | 567ms |

---

### 9.2 Activity Logs
```
Route: /super-admin/logs/activity
```

| Filter | Variantlar |
|--------|------------|
| User | Tanlash |
| Action | Login, Create, Update, Delete |
| Resource | Org, User, Order, Payment |
| Date | Time range |

**Log entry:**
```
2025-01-25 14:32:15 | admin@caterpro.uz | UPDATE | Organization
IP: 192.168.1.1 | Browser: Chrome 120 | Location: Tashkent
Details: Updated subscription for "Milliy Catering" from Basic to Premium
```

---

### 9.3 Error Logs
```
Route: /super-admin/logs/errors
```

| Severity | Count (24h) |
|----------|-------------|
| 🔴 Critical | 0 |
| 🟠 Error | 3 |
| 🟡 Warning | 45 |
| 🔵 Info | 1,234 |

**Error entry:**
```
2025-01-25 14:30:22 | ERROR | Payment Service
Message: Click payment timeout
Stack trace: [View]
Affected: Order #1234, Org: Milliy Catering
Status: Resolved (auto-retry successful)
```

---

### 9.4 Audit Trail
```
Route: /super-admin/logs/audit
```

| Element | Tavsif |
|---------|--------|
| Kimlarga | Super adminlar harakatlari |
| Nima qildi | Barcha o'zgarishlar |
| Qachon | Timestamp |
| IP | IP manzil |
| Natija | Muvaffaqiyatli/Xato |

---

## 10. Support va Tickets

### 10.1 Support Dashboard
```
Route: /super-admin/support
```

| Metrika | Qiymat |
|---------|--------|
| Ochiq ticketlar | 12 |
| Bugun yopilgan | 8 |
| O'rtacha javob vaqti | 2.3 soat |
| Qoniqish | 94% |

---

### 10.2 Support Tickets
```
Route: /super-admin/support/tickets
```

| Filter | Variantlar |
|--------|------------|
| Status | Yangi, Jarayonda, Yopilgan |
| Priority | Yuqori, O'rta, Past |
| Tashkilot | Tanlash |
| Kategoriya | Technical, Billing, Feature |

**Ticket:**
| ID | Tashkilot | Mavzu | Priority | Status | Vaqt |
|----|-----------|-------|----------|--------|------|
| #456 | Milliy Catering | Payment issue | 🔴 High | 🟡 Open | 2h |
| #455 | Lux Event | Feature request | 🟢 Low | 🔵 Closed | 1d |

---

### 10.3 Ticket Detail
```
Route: /super-admin/support/tickets/:id
```

| Element | Tavsif |
|---------|--------|
| Ticket info | ID, Status, Priority |
| Tashkilot | Qaysi tashkilotdan |
| Conversation | Yozishmalar |
| Internal notes | Ichki izohlar |
| Actions | Assign, Close, Escalate |
| Related | Bog'liq buyurtmalar/to'lovlar |

---

## 11. Marketing va Communications

### 11.1 Announcements
```
Route: /super-admin/communications/announcements
```

| Element | Tavsif |
|---------|--------|
| Yangi e'lon | Barcha tashkilotlarga |
| Scheduled | Rejalashtirilgan |
| Tarix | O'tgan e'lonlar |
| Target | Kimga (All/Tarif bo'yicha) |

---

### 11.2 Email Campaigns
```
Route: /super-admin/communications/campaigns
```

| Campaign | Target | Sent | Opened | Clicked |
|----------|--------|------|--------|---------|
| New feature | All | 47 | 89% | 34% |
| Promo offer | Trial | 8 | 75% | 45% |
| Tips & tricks | Basic | 18 | 67% | 23% |

---

## 12. Sahifalar Xaritasi

```
/super-admin
├── /super-admin/login
├── /super-admin/dashboard
├── /super-admin/organizations
│   ├── /super-admin/organizations/create
│   ├── /super-admin/organizations/:id
│   ├── /super-admin/organizations/:id/edit
│   ├── /super-admin/organizations/:id/subscription
│   └── /super-admin/organizations/:id/impersonate
├── /super-admin/subscriptions
│   ├── /super-admin/subscriptions/list
│   └── /super-admin/subscriptions/expiring
├── /super-admin/payments
│   └── /super-admin/payments/analytics
├── /super-admin/users
│   └── /super-admin/users/:id
├── /super-admin/analytics
│   ├── /super-admin/analytics/metrics
│   ├── /super-admin/analytics/geo
│   └── /super-admin/analytics/performance
├── /super-admin/reports
│   ├── /super-admin/reports/revenue
│   ├── /super-admin/reports/organizations
│   └── /super-admin/reports/scheduled
├── /super-admin/settings
│   ├── /super-admin/settings/pricing
│   ├── /super-admin/settings/features
│   ├── /super-admin/settings/emails
│   ├── /super-admin/settings/security
│   └── /super-admin/settings/api
├── /super-admin/monitoring
├── /super-admin/logs
│   ├── /super-admin/logs/activity
│   ├── /super-admin/logs/errors
│   └── /super-admin/logs/audit
├── /super-admin/support
│   └── /super-admin/support/tickets/:id
└── /super-admin/communications
    ├── /super-admin/communications/announcements
    └── /super-admin/communications/campaigns
```

---

## 13. Navigatsiya

### Sidebar Menu
| Icon | Nom | Route |
|------|-----|-------|
| 📊 | Dashboard | /super-admin/dashboard |
| 🏢 | Tashkilotlar | /super-admin/organizations |
| 💳 | Obunalar | /super-admin/subscriptions |
| 💰 | To'lovlar | /super-admin/payments |
| 👥 | Foydalanuvchilar | /super-admin/users |
| 📈 | Analitika | /super-admin/analytics |
| 📋 | Hisobotlar | /super-admin/reports |
| ⚙️ | Sozlamalar | /super-admin/settings |
| 🖥️ | Monitoring | /super-admin/monitoring |
| 📝 | Loglar | /super-admin/logs |
| 🎧 | Support | /super-admin/support |
| 📢 | Communications | /super-admin/communications |
