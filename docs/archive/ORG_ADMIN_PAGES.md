# CaterPro - Tashkilot Admin (Organization Admin) Sahifalari

> CaterPro dasturini o'rnatib olgan tashkilot egalari va adminlari uchun barcha sahifalar
> Misol: "Milliy Catering", "Lux Event" kabi kompaniyalar

---

## 1. Autentifikatsiya Sahifalari

### 1.1 Organization Login
```
Route: /org/login
yoki
Route: https://milliy-catering.caterpro.uz/login (subdomain)
```

| Element | Tavsif |
|---------|--------|
| Tashkilot logo | Kompaniya logotipi |
| Email/Telefon | Admin login |
| Parol | Maxfiy parol |
| Eslab qolish | Remember session |
| Kirish | Login tugmasi |
| Parolni unutdim | Reset password |
| 2FA | Ikki bosqichli tasdiqlash |

---

### 1.2 First Time Setup (Birinchi sozlash)
```
Route: /org/setup
```

**Tashkilot yangi ro'yxatdan o'tganda:**

**Step 1: Tashkilot ma'lumotlari**
| Element | Tavsif |
|---------|--------|
| Tashkilot nomi | "Milliy Catering" |
| Logo yuklash | Kompaniya logotipi |
| Tavsif | Qisqacha tavsif |
| Manzil | Ofis manzili |
| Telefon | Asosiy telefon |
| Email | Kompaniya emaili |

**Step 2: Subdomain sozlash**
| Element | Tavsif |
|---------|--------|
| Subdomain | milliy-catering.caterpro.uz |
| Custom domain | (Premium) catering.milliy.uz |
| SSL | Avtomatik HTTPS |

**Step 3: Branding**
| Element | Tavsif |
|---------|--------|
| Primary color | Asosiy rang |
| Secondary color | Ikkinchi rang |
| Favicon | Brauzer icon |
| Email template | Email dizayni |

**Step 4: Asosiy sozlamalar**
| Element | Tavsif |
|---------|--------|
| Valyuta | UZS / USD |
| Til | UZ / RU / EN |
| Vaqt zonasi | Asia/Tashkent |
| Ish vaqti | 09:00 - 18:00 |

---

## 2. Dashboard (Bosh panel)

### 2.1 Main Dashboard
```
Route: /org/dashboard
```

| Section | Elementlar |
|---------|------------|
| Header | Logo, Search, Notifications, Admin profil |
| Welcome | "Xush kelibsiz, [Tashkilot nomi]!" |
| Quick stats | 6 ta statistika card |
| Revenue chart | Daromad grafigi |
| Recent orders | Oxirgi buyurtmalar |
| Top providers | Eng yaxshi providerlar |
| Pending tasks | Kutilayotgan vazifalar |

**Statistika cardlari:**
| Card | Tavsif |
|------|--------|
| 📦 Buyurtmalar | Bu oydagi buyurtmalar (234) |
| 💰 Aylanma | Umumiy aylanma (45.2M) |
| 💵 Foyda | Toza foyda (12.4M) |
| 👥 Mijozlar | Umumiy mijozlar (156) |
| 🧑‍🍳 Providerlar | Faol providerlar (23) |
| ⭐ Reyting | O'rtacha baho (4.7) |

---

### 2.2 Quick Actions
```
Dashboard ichida
```

| Tugma | Tavsif |
|-------|--------|
| ➕ Yangi buyurtma | Qo'lda buyurtma yaratish |
| 👤 Yangi mijoz | Mijoz qo'shish |
| 🧑‍🍳 Yangi provider | Provider qo'shish |
| 📊 Hisobot | Tez hisobot |

---

## 3. Buyurtmalar Boshqaruvi

### 3.1 Orders List (Buyurtmalar ro'yxati)
```
Route: /org/orders
```

| Tab | Tavsif |
|-----|--------|
| Barchasi | Barcha buyurtmalar |
| Yangi | Tasdiqlash kutayotgan |
| Faol | Qabul qilingan |
| Yakunlangan | Tugallangan |
| Bekor qilingan | Rad etilgan |

**Filtrlar:**
| Filter | Variantlar |
|--------|------------|
| Sana oralig'i | Custom date range |
| Status | Multi-select |
| Mijoz | Qidiruv |
| Provider | Tanlash |
| Xizmat turi | Kategoriya |
| Summa | Min - Max |
| Xizmat darajasi | Start/Comfort/Premium/Business |

**Jadval ustunlari:**
| Ustun | Tavsif |
|-------|--------|
| ID | Buyurtma raqami |
| Sana | Tadbir sanasi |
| Mijoz | Ism + Telefon |
| Xizmat | Turi + Daraja |
| Mehmonlar | Kishilar soni |
| Provider | Kim bajaradi |
| Summa | Umumiy narx |
| Foyda | Toza foyda |
| Status | Holat badge |
| Actions | Ko'rish, Tahrirlash, Bekor |

**Export:**
| Format | Tavsif |
|--------|--------|
| Excel | .xlsx format |
| PDF | Hisobot ko'rinishida |
| CSV | Ma'lumotlar bazasi uchun |

---

### 3.2 Order Detail (Buyurtma tafsiloti)
```
Route: /org/orders/:id
```

| Section | Elementlar |
|---------|------------|
| Header | Order ID, Status, Actions |
| Timeline | Status tarixi |
| Mijoz info | To'liq ma'lumot + Aloqa |
| Tadbir | Tur, Sana, Vaqt, Manzil, Mehmonlar |
| Xizmatlar | Tanlangan xizmatlar ro'yxati |
| Provider | Kim bajaradi + Aloqa |
| Moliya | To'liq hisob-kitob |
| Izohlar | Ichki izohlar |
| Tarix | O'zgarishlar logi |

**Moliyaviy tafsilot:**
```
┌─────────────────────────────────────────────────┐
│  MOLIYAVIY HISOB - Buyurtma #234                │
├─────────────────────────────────────────────────┤
│                                                 │
│  KIRIM                                          │
│  ├── Xizmat narxi:         4,500,000 so'm      │
│  ├── Qo'shimcha xizmatlar:   300,000 so'm      │
│  └── Transport:              150,000 so'm      │
│  JAMI KIRIM:               4,950,000 so'm      │
│                                                 │
│  CHIQIM                                         │
│  ├── Mahsulotlar (bozorlik):1,800,000 so'm     │
│  ├── Oshpaz ish haqi:        450,000 so'm      │
│  ├── Ofitsiantlar (5):       500,000 so'm      │
│  ├── Idish arenda:           200,000 so'm      │
│  ├── Transport:              150,000 so'm      │
│  └── Boshqa:                 200,000 so'm      │
│  JAMI CHIQIM:              3,300,000 so'm      │
│                                                 │
│  ════════════════════════════════════════════  │
│  💵 TOZA FOYDA:            1,650,000 so'm      │
│  📊 RENTABELLIK:                33.3%          │
│                                                 │
└─────────────────────────────────────────────────┘
```

---

### 3.3 Create Order (Buyurtma yaratish)
```
Route: /org/orders/create
```

**Step 1: Mijoz tanlash/yaratish**
| Element | Tavsif |
|---------|--------|
| Mavjud mijoz | Qidiruv va tanlash |
| Yangi mijoz | Tez ro'yxatdan o'tkazish |

**Step 2: Tadbir ma'lumotlari**
| Element | Tavsif |
|---------|--------|
| Tadbir turi | To'y, Tug'ilgan kun, Korporativ... |
| Sana | Kalendar |
| Boshlanish vaqti | Time picker |
| Tugash vaqti | Time picker |
| Mehmonlar soni | Raqam |
| Manzil | Xarita yoki qo'lda |
| Xizmat darajasi | Start/Comfort/Premium/Business |

**Step 3: Xizmatlar tanlash**
| Element | Tavsif |
|---------|--------|
| Xizmat kategoriyasi | Oshpaz, Ofitsiant, Arenda... |
| Provider tanlash | Mavjud providerlardan |
| Xizmatlar | Checkbox list |
| Qo'shimchalar | Qo'shimcha xizmatlar |
| Menyu | (Oshpaz uchun) Taomlar |

**Step 4: Bozorlik/Xarajatlar**
| Element | Tavsif |
|---------|--------|
| Mahsulotlar | Avtomatik yoki qo'lda |
| Narxlar | Har bir mahsulot narxi |
| Boshqa xarajatlar | Transport, arenda... |

**Step 5: Narxlash**
| Element | Tavsif |
|---------|--------|
| Xizmat narxi | Avtomatik hisoblash |
| Chegirma | Foiz yoki summa |
| Yakuniy narx | Jami summa |
| Avans | Oldindan to'lov % |

**Step 6: Tasdiqlash**
| Element | Tavsif |
|---------|--------|
| Xulosa | Barcha ma'lumotlar |
| Shartnoma | Shartnoma generatsiya |
| Saqlash | Buyurtmani yaratish |

---

### 3.4 Order Calendar (Buyurtmalar kalendari)
```
Route: /org/orders/calendar
```

| View | Tavsif |
|------|--------|
| Oylik | Oy ko'rinishi |
| Haftalik | Hafta ko'rinishi |
| Kunlik | Kun bo'yicha |
| Timeline | Gantt chart ko'rinishi |

| Element | Tavsif |
|---------|--------|
| Buyurtma | Rangli marker |
| Drag & drop | Sanani o'zgartirish |
| Provider filter | Provider bo'yicha |
| Click | Quick view modal |

---

## 4. Mijozlar Boshqaruvi

### 4.1 Customers List (Mijozlar ro'yxati)
```
Route: /org/customers
```

**Filtrlar:**
| Filter | Variantlar |
|--------|------------|
| Status | Faol, Nofaol, VIP |
| Buyurtmalar soni | 1, 2-4, 5+ |
| Jami xarajat | Summa oralig'i |
| Ro'yxatdan o'tgan | Sana oralig'i |
| Manbai | Qayerdan kelgan |

**Jadval:**
| Ustun | Tavsif |
|-------|--------|
| ID | Mijoz ID |
| Ism | To'liq ism |
| Telefon | Aloqa |
| Buyurtmalar | Soni |
| Jami xarajat | Umumiy sarflagan |
| Oxirgi buyurtma | Qachon |
| VIP | Badge |
| Actions | Ko'rish, Tahrirlash |

---

### 4.2 Customer Detail (Mijoz profili)
```
Route: /org/customers/:id
```

| Section | Elementlar |
|---------|------------|
| Header | Ism, Avatar, VIP badge, Actions |
| Aloqa | Telefon, Email, Manzil |
| Statistika | Buyurtmalar, Xarajat, O'rtacha check |
| Buyurtmalar | Barcha buyurtmalar tarixi |
| Izohlar | Ichki notes |
| Segmentlar | Teglar (VIP, Korporativ...) |

**Mijoz statistikasi:**
```
┌─────────────────────────────────────────────────┐
│  👤 KARIMOV ALISHER                    [VIP 🌟] │
├─────────────────────────────────────────────────┤
│                                                 │
│  📦 Buyurtmalar:          12 ta                │
│  💰 Jami xarajat:         8,500,000 so'm       │
│  📊 O'rtacha check:       708,333 so'm         │
│  ⭐ Bergan baho:          4.9 / 5              │
│  📅 Oxirgi buyurtma:      3 kun oldin          │
│  🎂 Tug'ilgan kun:        15-Mart              │
│                                                 │
│  BUYURTMA TARIXI                               │
│  ├── #234 | 25-Yan | To'y | 4,500,000 | ✅     │
│  ├── #201 | 10-Yan | Tug'ilgan kun | 850,000   │
│  ├── #189 | 25-Dek | Yangi yil | 1,200,000     │
│  └── ... (yana 9 ta)                           │
│                                                 │
└─────────────────────────────────────────────────┘
```

---

### 4.3 Add/Edit Customer
```
Route: /org/customers/create
Route: /org/customers/:id/edit
```

| Field | Tavsif |
|-------|--------|
| Ism | To'liq ism |
| Telefon | +998 XX XXX XX XX |
| Email | Ixtiyoriy |
| Tug'ilgan sana | Eslatma uchun |
| Manzil | Asosiy manzil |
| Kompaniya | (Korporativ uchun) |
| Izoh | Ichki note |
| Teglar | VIP, Korporativ, Doimiy... |
| Manbai | Qayerdan kelgan |

---

### 4.4 Customer Segments (Segmentlar)
```
Route: /org/customers/segments
```

| Segment | Tavsif | Mijozlar |
|---------|--------|----------|
| 🌟 VIP | 5+ buyurtma yoki 5M+ xarajat | 23 |
| 🔵 Doimiy | 2-4 buyurtma | 45 |
| ⚪ Yangi | 1 buyurtma | 88 |
| 🏢 Korporativ | B2B mijozlar | 12 |
| 😴 Nofaol | 3+ oy buyurtmasiz | 34 |

---

## 5. Providerlar Boshqaruvi

### 5.1 Providers List (Providerlar ro'yxati)
```
Route: /org/providers
```

**Filtrlar:**
| Filter | Variantlar |
|--------|------------|
| Kategoriya | Oshpaz, Ofitsiant, Arenda... |
| Status | Faol, Nofaol, Kutilmoqda |
| Reyting | 3+, 4+, 4.5+ |
| Verified | Tasdiqlangan/Tasdiqlanmagan |

**Jadval:**
| Ustun | Tavsif |
|-------|--------|
| ID | Provider ID |
| Ism/Nomi | Provider nomi |
| Kategoriya | Xizmat turi |
| Reyting | Yulduzlar |
| Buyurtmalar | Bu oydagi |
| Daromad | Bu oydagi |
| Status | Faol/Nofaol |
| Verified | Badge |
| Actions | Ko'rish, Tahrirlash |

---

### 5.2 Provider Detail
```
Route: /org/providers/:id
```

| Section | Elementlar |
|---------|------------|
| Profil | Ism, Rasm, Kategoriya, Reyting |
| Aloqa | Telefon, Email |
| Hujjatlar | Passport, Sertifikatlar |
| Xizmatlar | Ko'rsatadigan xizmatlar |
| Statistika | Buyurtmalar, Daromad, Reyting |
| Sharhlar | Mijoz fikrlari |
| Kalendar | Band/bo'sh kunlar |
| Hisob-kitob | To'lovlar tarixi |

---

### 5.3 Add Provider (Provider qo'shish)
```
Route: /org/providers/create
```

| Tab | Elementlar |
|-----|------------|
| Asosiy | Ism, Telefon, Email, Kategoriya |
| Hujjatlar | Passport, Sertifikat yuklash |
| Xizmatlar | Xizmatlar va narxlar |
| Jadval | Ish vaqtlari |
| To'lov | Bank ma'lumotlari |

---

### 5.4 Provider Verification (Tasdiqlash)
```
Route: /org/providers/pending
```

| Element | Tavsif |
|---------|--------|
| Kutilayotganlar | Yangi arizalar |
| Hujjatlar | Ko'rish va tekshirish |
| Tasdiqlash | Approve tugmasi |
| Rad etish | Reject + Sabab |
| So'rov | Qo'shimcha hujjat so'rash |

---

### 5.5 Provider Payouts (Provider to'lovlari)
```
Route: /org/providers/payouts
```

| Filter | Variantlar |
|--------|------------|
| Provider | Tanlash |
| Davr | Sana oralig'i |
| Status | To'langan/Kutilmoqda |

**To'lov hisoblash:**
```
Provider: Sardor Oshpaz
Davr: 01-31 Yanvar 2025

Buyurtmalar:
├── #234: 450,000 so'm (10% komissiya: 45,000)
├── #228: 380,000 so'm (10% komissiya: 38,000)
├── #215: 520,000 so'm (10% komissiya: 52,000)
└── Jami: 1,350,000 so'm

Komissiya: -135,000 so'm
════════════════════════════
To'lanadigan: 1,215,000 so'm
```

---

## 6. Xizmatlar Katalogi

### 6.1 Services Catalog (Xizmatlar ro'yxati)
```
Route: /org/services
```

| Element | Tavsif |
|---------|--------|
| Kategoriyalar | Xizmat turlari |
| Xizmatlar | Har bir kategoriya ichida |
| Narxlar | Daraja bo'yicha |
| Status | Faol/Nofaol |

---

### 6.2 Service Categories (Kategoriyalar)
```
Route: /org/services/categories
```

| Kategoriya | Sub-kategoriyalar |
|------------|-------------------|
| 👨‍🍳 Oshpaz | Milliy, Yevropa, Osiyo |
| 🤵 Ofitsiant | Oddiy, Bosh ofitsiant |
| 🍽️ Arenda | Idish, Mebel, Chodir |
| 💐 Dekor | Gul, Shar, To'liq bezak |
| 📸 Foto/Video | Fotograf, Videograf |
| 🎵 Musiqa | DJ, Jonli musiqa |
| 🚗 Transport | Mehmon tashish |

---

### 6.3 Pricing Templates (Narx shablonlari)
```
Route: /org/services/pricing
```

| Daraja | Koeffitsient | Tavsif |
|--------|--------------|--------|
| Start | 1.0x | Bazaviy narx |
| Comfort | 1.5x | +50% qo'shimcha |
| Premium | 2.2x | +120% qo'shimcha |
| Business | 3.0x | +200% qo'shimcha |

---

## 7. Moliya va Hisobotlar

### 7.1 Finance Dashboard
```
Route: /org/finance
```

| Section | Elementlar |
|---------|------------|
| Overview | Umumiy ko'rsatkichlar |
| Revenue chart | Daromad grafigi |
| Expense chart | Xarajat grafigi |
| Profit chart | Foyda grafigi |
| Cash flow | Pul oqimi |

**Umumiy ko'rsatkichlar:**
```
┌─────────────────────────────────────────────────────────────┐
│               MOLIYAVIY DASHBOARD - Yanvar 2025             │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  ┌─────────────┐ ┌─────────────┐ ┌─────────────┐          │
│  │ 💰 45.2M    │ │ 💸 32.8M    │ │ 💵 12.4M    │          │
│  │ Aylanma    │ │ Xarajatlar  │ │ Toza foyda  │          │
│  │ ↑ 12%      │ │ ↑ 8%        │ │ ↑ 18%       │          │
│  └─────────────┘ └─────────────┘ └─────────────┘          │
│                                                             │
│  📊 RENTABELLIK: 27.4%                                     │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

---

### 7.2 Revenue Report (Daromad hisoboti)
```
Route: /org/finance/revenue
```

| Filter | Variantlar |
|--------|------------|
| Davr | Kun, Hafta, Oy, Yil, Custom |
| Kategoriya | Xizmat turi |
| Provider | Tanlash |
| Mijoz | Tanlash |

**Daromad bo'linishi:**
| Manba | Summa | % |
|-------|-------|---|
| Catering (to'liq) | 18,500,000 | 41% |
| Faqat oshpaz | 10,200,000 | 23% |
| Ofitsiant | 6,100,000 | 13% |
| Arenda | 4,100,000 | 9% |
| Dekor | 3,500,000 | 8% |
| Boshqa | 2,800,000 | 6% |
| **JAMI** | **45,200,000** | **100%** |

---

### 7.3 Expense Report (Xarajatlar hisoboti)
```
Route: /org/finance/expenses
```

| Kategoriya | Summa | % |
|------------|-------|---|
| Mahsulotlar (bozorlik) | 18,200,000 | 55% |
| Ish haqi (providerlar) | 9,800,000 | 30% |
| Transport | 2,100,000 | 6% |
| Arenda (xarajat) | 1,500,000 | 5% |
| Boshqa | 1,200,000 | 4% |
| **JAMI** | **32,800,000** | **100%** |

---

### 7.4 Profit Analysis (Foyda tahlili)
```
Route: /org/finance/profit
```

**Buyurtma bo'yicha foyda:**
| Order | Kirim | Chiqim | Foyda | Margin |
|-------|-------|--------|-------|--------|
| #234 | 4,950,000 | 3,300,000 | 1,650,000 | 33.3% |
| #233 | 2,800,000 | 2,050,000 | 750,000 | 26.8% |
| #232 | 850,000 | 630,000 | 220,000 | 25.9% |

**Oylik foyda trend:**
```
Yanvar:  ████████████████ 12.4M (27.4%)
Dekabr:  ██████████████ 10.5M (25.1%)
Noyabr:  █████████████ 9.8M (24.3%)
Oktabr:  ████████████ 8.9M (23.8%)
```

---

### 7.5 Transactions (Tranzaksiyalar)
```
Route: /org/finance/transactions
```

| Filter | Variantlar |
|--------|------------|
| Tur | Kirim, Chiqim, Barchasi |
| Kategoriya | Buyurtma, Xarajat, To'lov |
| Sana | Date range |

**Tranzaksiya turlari:**
| Tur | Icon | Tavsif |
|-----|------|--------|
| Buyurtma to'lovi | 💰 | Mijozdan kirim |
| Bozorlik | 🛒 | Mahsulot xaridi |
| Ish haqi | 👷 | Provider to'lovi |
| Arenda | 📦 | Idish/mebel arenda |
| Transport | 🚗 | Yetkazib berish |
| Boshqa | 📝 | Turli xarajatlar |

---

### 7.6 Invoices (Hisob-fakturalar)
```
Route: /org/finance/invoices
```

| Element | Tavsif |
|---------|--------|
| Invoice ro'yxati | Barcha fakturalar |
| Yaratish | Yangi faktura |
| Yuborish | Email orqali |
| Download | PDF yuklab olish |
| Status | To'langan/Kutilmoqda |

---

## 8. Hisobotlar va Analitika

### 8.1 Reports Dashboard
```
Route: /org/reports
```

| Report | Tavsif |
|--------|--------|
| Sales Report | Sotuvlar hisoboti |
| Customer Report | Mijozlar hisoboti |
| Provider Report | Providerlar hisoboti |
| Service Report | Xizmatlar hisoboti |
| Financial Report | Moliyaviy hisobot |
| Custom Report | Maxsus hisobot |

---

### 8.2 Sales Report (Sotuvlar hisoboti)
```
Route: /org/reports/sales
```

| Metrika | Qiymat | O'zgarish |
|---------|--------|-----------|
| Buyurtmalar soni | 234 | ↑ 12% |
| Umumiy aylanma | 45.2M | ↑ 15% |
| O'rtacha check | 193K | ↑ 3% |
| Konversiya | 68% | ↑ 5% |
| Qayta buyurtma | 42% | ↑ 8% |

**Grafiklar:**
- Kunlik/Haftalik/Oylik sotuvlar (line)
- Xizmat turlari bo'yicha (pie)
- Eng yaxshi kunlar (bar)
- Konversiya funnel

---

### 8.3 Customer Report
```
Route: /org/reports/customers
```

| Metrika | Qiymat |
|---------|--------|
| Jami mijozlar | 156 |
| Yangi mijozlar (bu oy) | 23 |
| Qaytgan mijozlar | 65% |
| Churn rate | 8% |
| Customer LTV | 2.1M |

**Segmentatsiya:**
```
VIP (5+):     ████████████████ 23 (15%) → 68% daromad
Doimiy (2-4): ██████████████████████ 45 (29%) → 24% daromad
Yangi (1):    ███████████████████████████████████ 88 (56%) → 8% daromad
```

---

### 8.4 Provider Report
```
Route: /org/reports/providers
```

| Provider | Buyurtmalar | Daromad | Reyting |
|----------|-------------|---------|---------|
| Sardor Oshpaz | 45 | 8.5M | 4.9 |
| Jahongir Oshpaz | 38 | 6.2M | 4.7 |
| Bobur Ofitsiant | 52 | 3.8M | 4.8 |
| Idish Arenda | 34 | 2.1M | 4.6 |

---

### 8.5 Custom Report Builder
```
Route: /org/reports/builder
```

| Element | Tavsif |
|---------|--------|
| Metrikalar | Tanlash (drag & drop) |
| Filtrlar | Shartlar qo'yish |
| Visualizatsiya | Chart turi |
| Davr | Time range |
| Saqlash | Shablon sifatida |
| Export | PDF, Excel, CSV |

---

## 9. Bozorlik va Inventory

### 9.1 Grocery Calculator (Bozorlik kalkulyatori)
```
Route: /org/grocery
```

| Element | Tavsif |
|---------|--------|
| Buyurtma tanlash | Qaysi buyurtma uchun |
| Menyu | Taomlar ro'yxati |
| Mehmonlar | Kishilar soni |
| Hisoblash | Avtomatik kalkulyatsiya |

**Hisoblash formulasi:**
```
Mahsulot = (Mehmonlar × Porsiya × 1.1) / 1000

Misol: Palov (150 kishi)
├── Guruch: 150 × 200g × 1.1 = 33 kg
├── Go'sht: 150 × 150g × 1.1 = 25 kg
├── Sabzi: 150 × 100g × 1.1 = 16.5 kg
├── Piyoz: 150 × 50g × 1.1 = 8.25 kg
└── Yog': 150 × 30ml × 1.1 = 5 litr
```

---

### 9.2 Grocery List (Bozorlik ro'yxati)
```
Route: /org/grocery/list/:orderId
```

| Mahsulot | Miqdor | Narx | Jami |
|----------|--------|------|------|
| Guruch (kg) | 33 | 18,000 | 594,000 |
| Go'sht (kg) | 25 | 85,000 | 2,125,000 |
| Sabzi (kg) | 16.5 | 8,000 | 132,000 |
| Piyoz (kg) | 8.25 | 6,000 | 49,500 |
| Yog' (litr) | 5 | 25,000 | 125,000 |
| **JAMI** | | | **3,025,500** |

**Actions:**
- Print (chop etish)
- Send (provider ga yuborish)
- Mark purchased (sotib olingan)

---

### 9.3 Inventory (Ombor)
```
Route: /org/inventory
(Arenda xizmati uchun)
```

| Tovar | Mavjud | Band | Bo'sh |
|-------|--------|------|-------|
| Likopcha (katta) | 500 | 150 | 350 |
| Qoshiq to'plam | 300 | 100 | 200 |
| Stakan (kristal) | 400 | 80 | 320 |
| Stul (klassik) | 200 | 45 | 155 |

---

## 10. Sozlamalar

### 10.1 Organization Settings
```
Route: /org/settings
```

| Tab | Elementlar |
|-----|------------|
| General | Asosiy sozlamalar |
| Branding | Logo, ranglar |
| Team | Adminlar boshqaruvi |
| Billing | Obuna va to'lov |
| Integrations | API, webhook |
| Security | Xavfsizlik |

---

### 10.2 General Settings
```
Route: /org/settings/general
```

| Field | Tavsif |
|-------|--------|
| Tashkilot nomi | Kompaniya nomi |
| Tavsif | Qisqacha tavsif |
| Telefon | Asosiy telefon |
| Email | Kompaniya email |
| Manzil | Ofis manzili |
| Ish vaqti | Ochilish-yopilish |
| Valyuta | UZS / USD |
| Til | UZ / RU / EN |
| Vaqt zonasi | Asia/Tashkent |

---

### 10.3 Branding
```
Route: /org/settings/branding
```

| Element | Tavsif |
|---------|--------|
| Logo | Asosiy logo |
| Favicon | Brauzer icon |
| Primary color | Asosiy rang |
| Secondary color | Ikkinchi rang |
| Email header | Email dizayni |
| Invoice logo | Faktura uchun |

---

### 10.4 Team Management (Jamoa)
```
Route: /org/settings/team
```

**Rollar:**
| Rol | Ruxsatlar |
|-----|-----------|
| Owner | To'liq ruxsat |
| Admin | Buyurtma, Mijoz, Provider, Moliya |
| Manager | Buyurtma, Mijoz, Provider |
| Operator | Faqat buyurtmalar |

**Jamoa a'zolari:**
| Ism | Email | Rol | Status |
|-----|-------|-----|--------|
| Alisher | alisher@mail.uz | Owner | ✅ |
| Bobur | bobur@mail.uz | Admin | ✅ |
| Malika | malika@mail.uz | Manager | ✅ |

---

### 10.5 Billing (Obuna)
```
Route: /org/settings/billing
```

| Section | Elementlar |
|---------|------------|
| Joriy tarif | Hozirgi obuna |
| Xususiyatlar | Mavjud imkoniyatlar |
| To'lov tarixi | O'tgan to'lovlar |
| Karta | Saqlangan karta |
| Yangilash | Tarifni oshirish |
| Invoice | Fakturalar tarixi |

---

### 10.6 API & Integrations
```
Route: /org/settings/integrations
```

| Integration | Tavsif |
|-------------|--------|
| API Key | API kaliti generatsiya |
| Webhooks | Event notifications |
| Click/Payme | To'lov integratsiya |
| SMS (Eskiz) | SMS xabar |
| Google Calendar | Kalendar sync |
| Telegram Bot | Bildirishnomalar |

---

## 11. Sahifalar Xaritasi

```
/org
├── /org/login
├── /org/setup
├── /org/dashboard
├── /org/orders
│   ├── /org/orders/create
│   ├── /org/orders/:id
│   ├── /org/orders/:id/edit
│   └── /org/orders/calendar
├── /org/customers
│   ├── /org/customers/create
│   ├── /org/customers/:id
│   ├── /org/customers/:id/edit
│   └── /org/customers/segments
├── /org/providers
│   ├── /org/providers/create
│   ├── /org/providers/:id
│   ├── /org/providers/:id/edit
│   ├── /org/providers/pending
│   └── /org/providers/payouts
├── /org/services
│   ├── /org/services/categories
│   └── /org/services/pricing
├── /org/finance
│   ├── /org/finance/revenue
│   ├── /org/finance/expenses
│   ├── /org/finance/profit
│   ├── /org/finance/transactions
│   └── /org/finance/invoices
├── /org/reports
│   ├── /org/reports/sales
│   ├── /org/reports/customers
│   ├── /org/reports/providers
│   └── /org/reports/builder
├── /org/grocery
│   ├── /org/grocery/list/:orderId
│   └── /org/inventory
├── /org/settings
│   ├── /org/settings/general
│   ├── /org/settings/branding
│   ├── /org/settings/team
│   ├── /org/settings/billing
│   └── /org/settings/integrations
├── /org/notifications
└── /org/help
```

---

## 12. Navigatsiya

### Sidebar Menu
| Icon | Nom | Route |
|------|-----|-------|
| 📊 | Dashboard | /org/dashboard |
| 📦 | Buyurtmalar | /org/orders |
| 👥 | Mijozlar | /org/customers |
| 🧑‍🍳 | Providerlar | /org/providers |
| 🛠️ | Xizmatlar | /org/services |
| 💰 | Moliya | /org/finance |
| 📈 | Hisobotlar | /org/reports |
| 🛒 | Bozorlik | /org/grocery |
| ⚙️ | Sozlamalar | /org/settings |
| ❓ | Yordam | /org/help |
