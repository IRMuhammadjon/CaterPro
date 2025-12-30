# CaterPro - Provider (Xizmat ko'rsatuvchi) Sahifalari

> Oshpaz, Ofitsiant, Arenda va boshqa xizmat ko'rsatuvchilar uchun barcha sahifalar
> **MUHIM:** Providerlar TASHKILOT bilan ishlaydi, mijoz bilan to'g'ridan-to'g'ri EMAS!

---

## 🔄 Yangilangan Model

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                        PROVIDER ISHI MODELI                                 │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│   🧑‍🍳 PROVIDER (Xizmat ko'rsatuvchi)                                        │
│      │                                                                      │
│      ▼                                                                      │
│   🏢 TASHKILOT (Org Admin) ga qo'shiladi                                   │
│      │  • Tashkilot providerlarni ro'yxatga oladi                          │
│      │  • Buyurtmalar kelganda provider tayinlaydi                         │
│      │  • Provider ish haqi/komissiya oladi                                │
│      │                                                                      │
│      ▼                                                                      │
│   📦 BUYURTMA                                                               │
│      • Tashkilot providerni tayinlaydi                                     │
│      • Provider vazifani bajaradi                                          │
│      • To'lov tashkilot orqali                                             │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘

Provider MIJOZNI ko'rmaydi.
Provider TASHKILOT dan vazifa oladi va bajaradi.
```

---

## 1. Autentifikatsiya Sahifalari

### 1.1 Provider Welcome (Kirish sahifasi)
```
Route: /provider/welcome
```

| Element | Tavsif |
|---------|--------|
| Logo | CaterPro Provider logotipi |
| Slogan | "Professional xizmat - barqaror daromad" |
| Kirish | Login sahifasiga |
| Ro'yxatdan o'tish | Provider registration |
| Statistika | "1000+ provider bizga qo'shildi" |
| Afzalliklar | Nima uchun CaterPro? |

**Afzalliklar ro'yxati:**
- Barqaror buyurtmalar oqimi
- Tashkilot orqali kafolatlangan to'lov
- Professional jamoada ishlash
- Reyting va o'sish imkoniyati

---

### 1.2 Provider Login
```
Route: /provider/login
```

| Element | Tavsif |
|---------|--------|
| Telefon/Email | Login credential |
| Parol | Maxfiy parol |
| Eslab qolish | Remember me checkbox |
| Kirish | Login tugmasi |
| Parolni unutdim | Reset password link |
| SMS login | OTP orqali kirish |
| Ro'yxatdan o'tish | Register sahifasiga |

---

### 1.3 Provider Registration (Ro'yxatdan o'tish)
```
Route: /provider/register
```

**Step 1: Telefon tasdiqlash**
| Element | Tavsif |
|---------|--------|
| Telefon raqam | +998 XX XXX XX XX |
| SMS yuborish | OTP yuborish |
| OTP kiritish | 6 xonali kod |

**Step 2: Shaxsiy ma'lumotlar**
| Element | Tavsif |
|---------|--------|
| Ism | To'liq ism |
| Familiya | Familiya |
| Tug'ilgan sana | Date picker |
| Email | Bog'lanish uchun |
| Parol | Yangi parol |
| Manzil | Yashash manzili |
| Shahar | Asosiy faoliyat shahri |

**Step 3: Xizmat turi tanlash**
| Element | Tavsif |
|---------|--------|
| Kategoriya | Oshpaz, Ofitsiant, Arenda, Dekor... |
| Sub-kategoriya | Milliy oshpaz, Yevropa oshpazi... |
| Tajriba | Yillar soni |
| Malaka darajasi | Boshlang'ich, O'rta, Professional |

**Step 4: Hujjatlar yuklash**
| Element | Tavsif |
|---------|--------|
| Passport | Shaxsni tasdiqlovchi hujjat (old/orqa) |
| Rasm | Professional foto |
| Sertifikat | (Ixtiyoriy) Malaka guvohnomasi |
| San-kitob | (Oshpazlar uchun) Sanitariya kitobchasi |
| Portfolio | Kamida 3 ta ish namunasi |

**Step 5: Tashkilotga qo'shilish**
| Element | Tavsif |
|---------|--------|
| Tashkilot qidirish | Mavjud tashkilotlar ro'yxati |
| Ariza yuborish | Tanlangan tashkilotga ariza |
| Yoki | Yangi tashkilot kutish |

**MUHIM:** Provider bir yoki bir nechta tashkilotga qo'shilishi mumkin.

---

### 1.4 Pending Approval (Tasdiqlash kutilmoqda)
```
Route: /provider/pending
```

| Element | Tavsif |
|---------|--------|
| Status | "Arizangiz ko'rib chiqilmoqda" |
| Tashkilot nomi | Qaysi tashkilotga ariza yuborgan |
| Kutish vaqti | "1-3 ish kuni ichida" |
| Progress | Hujjatlar tekshiruvi |
| Aloqa | Tashkilot bilan bog'lanish |
| Boshqa tashkilot | Boshqa joyga ham ariza yuborish |

---

## 2. Dashboard (Bosh panel)

### 2.1 Provider Dashboard
```
Route: /provider/dashboard
```

| Section | Elementlar |
|---------|------------|
| Header | Logo, Bildirishnomalar, Profil |
| Salom | "Xush kelibsiz, [Ism]!" |
| Tashkilot | Qaysi tashkilotda ishlayapti |
| Tez statistika | 4 ta card |
| Bugungi vazifalar | Bugungi ishlar |
| Kelgusi vazifalar | Yaqin kunlardagi |
| Daromad | Haftalik daromad grafigi |

**Statistika cardlari:**
```
┌─────────────────────────────────────────────────────────────────────────────┐
│                         PROVIDER DASHBOARD                                  │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  🏢 Tashkilot: Milliy Catering                    [O'zgartirish]           │
│                                                                             │
│  ┌──────────┐ ┌──────────┐ ┌──────────┐ ┌──────────┐                      │
│  │ 📦 12    │ │ 💰 2.8M  │ │ ⭐ 4.9   │ │ 📅 3     │                      │
│  │ Vazifalar│ │ Bu oy    │ │ Reyting  │ │ Bugun   │                      │
│  │ bu oy    │ │ daromad  │ │          │ │ ishlar   │                      │
│  └──────────┘ └──────────┘ └──────────┘ └──────────┘                      │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

### 2.2 Today's Tasks (Bugungi vazifalar)
```
Dashboard ichida
```

| Element | Tavsif |
|---------|--------|
| Vazifa card | Tadbir, Vaqt, Manzil |
| Status | Tayyorgarlik / Jarayonda / Tugallangan |
| Batafsil | Vazifa tafsiloti |
| Navigatsiya | Xaritada yo'nalish |

**Vazifa card:**
```
┌─────────────────────────────────────────────────────────────┐
│  📦 Vazifa #234                               🟢 Bugun     │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  🍽️ To'y - 150 kishilik milliy taomlar                     │
│  📅 Bugun, 16:00 - 23:00                                   │
│  📍 Yunusobod, To'yxona "Shodlik"                          │
│                                                             │
│  Sizning vazifangiz:                                        │
│  • Palov tayyorlash (150 kishi)                            │
│  • Shorva (150 kishi)                                       │
│  • Manti (150 kishi)                                        │
│                                                             │
│  [📋 Batafsil]              [📍 Xaritada]                  │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

---

## 3. Vazifalar (Tasks/Orders)

### 3.1 Tasks List (Vazifalar ro'yxati)
```
Route: /provider/tasks
```

| Tab | Tavsif |
|-----|--------|
| Yangi | Qabul qilish kutayotgan |
| Faol | Qabul qilingan, bajarilmoqda |
| Yakunlangan | Tugallangan vazifalar |
| Bekor qilingan | Rad etilgan |

**Filter:**
| Filter | Variantlar |
|--------|------------|
| Sana | Bugun, Hafta, Oy |
| Status | Yangi, Faol, Tugallangan |
| Tashkilot | (agar bir nechtada ishlasa) |

**MUHIM:** Provider faqat tashkilot tayinlagan vazifalarni ko'radi.
Mijoz ma'lumotlari KO'RINMAYDI.

---

### 3.2 Task Detail (Vazifa tafsiloti)
```
Route: /provider/tasks/:id
```

| Section | Elementlar |
|---------|------------|
| Header | Vazifa ID, Status, Tashkilot |
| Tadbir info | Tur, Sana, Vaqt |
| Manzil | Xarita + Navigatsiya |
| Sizning vazifangiz | Aniq nima qilish kerak |
| Mahsulotlar | (Oshpaz uchun) Ingredientlar |
| Jamoa | Birga ishlaydigan providerlar |
| To'lov | Bu vazifa uchun summa |
| Izohlar | Tashkilotdan eslatmalar |

**Vazifa tafsiloti:**
```
┌─────────────────────────────────────────────────────────────────────────────┐
│  📦 VAZIFA #234                                          🟢 Qabul qilingan │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  🏢 Tashkilot: Milliy Catering                                             │
│                                                                             │
│  📅 TADBIR MA'LUMOTLARI                                                    │
│  ├── Tur: To'y                                                             │
│  ├── Sana: 15-Fevral 2025                                                  │
│  ├── Vaqt: 16:00 - 23:00                                                   │
│  ├── Mehmonlar: 150 kishi                                                  │
│  └── Manzil: Yunusobod, "Shodlik" to'yxonasi                              │
│                                                                             │
│  👨‍🍳 SIZNING VAZIFANGIZ                                                     │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │  1. Palov tayyorlash - 150 kishi                                   │   │
│  │  2. Shorva - 150 kishi                                              │   │
│  │  3. Manti - 150 kishi                                               │   │
│  │  4. Salat (2 xil) - 150 kishi                                       │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│                                                                             │
│  📦 MAHSULOTLAR (Sizga yetkaziladi)                                        │
│  ├── Guruch: 30 kg                                                         │
│  ├── Go'sht: 25 kg                                                         │
│  ├── Sabzi: 15 kg                                                          │
│  └── ... (to'liq ro'yxat)                                                  │
│                                                                             │
│  👥 JAMOA (Bu tadbirda)                                                    │
│  ├── Siz - Bosh oshpaz                                                     │
│  ├── Anvar - Yordamchi oshpaz                                              │
│  └── 5 ta ofitsiant                                                        │
│                                                                             │
│  💰 TO'LOV: 450,000 so'm                                                   │
│                                                                             │
│  [📍 Xaritada ko'rish]     [✅ Boshlash]     [💬 Tashkilotga yozish]       │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

**MUHIM:** Provider MIJOZ haqida hech narsa bilmaydi!
Faqat tadbir turi, manzil va vazifa ko'rinadi.

---

### 3.3 New Task Request (Yangi vazifa)
```
Route: /provider/tasks/:id (status=pending)
```

| Element | Tavsif |
|---------|--------|
| Notification | Push bildirishnoma |
| Vazifa tafsiloti | Nima qilish kerak |
| To'lov | Qancha to'lanadi |
| Qabul qilish | Accept tugmasi |
| Rad etish | Reject + Sabab |

**Rad etish sabablari:**
- Band (boshqa ish bor)
- Juda uzoq (manzil)
- Boshqa sabab

---

### 3.4 Task Progress (Vazifa jarayoni)
```
Route: /provider/tasks/:id/progress
```

| Status | Tavsif |
|--------|--------|
| ⚪ Qabul qilindi | Vazifani oldim |
| 🔵 Yo'lda | Manzilga ketyapman |
| 🟡 Boshlandi | Ish boshladim |
| 🟢 Tugallandi | Ish tugadi |

| Tugma | Tavsif |
|-------|--------|
| Yo'ldaman | Status yangilash |
| Boshladim | Ish boshlandi |
| Tugadim | Ish yakunlandi |
| Muammo | Tashkilotga xabar |

---

## 4. Kalendar va Jadval

### 4.1 Calendar (Kalendar)
```
Route: /provider/calendar
```

| View | Tavsif |
|------|--------|
| Oylik | Oy ko'rinishi |
| Haftalik | Hafta ko'rinishi |
| Kunlik | Kun bo'yicha |
| Ro'yxat | List view |

| Marker | Tavsif |
|--------|--------|
| 🟢 | Tasdiqlangan vazifa |
| 🟡 | Kutilayotgan |
| 🔴 | Band qilingan (dam olish) |
| ⚪ | Bo'sh |

---

### 4.2 Availability (Mavjudlik sozlamalari)
```
Route: /provider/calendar/availability
```

| Element | Tavsif |
|---------|--------|
| Doimiy jadval | Haftalik ish vaqti |
| Dam olish | Maxsus dam olish kunlari |
| Ta'til | Uzoq muddatli band |
| Bir kunlik | Alohida kun band qilish |

**Haftalik jadval:**
| Kun | Boshlanish | Tugash | Status |
|-----|------------|--------|--------|
| Dushanba | 08:00 | 22:00 | ✅ Ishchi |
| Seshanba | 08:00 | 22:00 | ✅ Ishchi |
| Chorshanba | 08:00 | 22:00 | ✅ Ishchi |
| Payshanba | 08:00 | 22:00 | ✅ Ishchi |
| Juma | 08:00 | 22:00 | ✅ Ishchi |
| Shanba | 08:00 | 22:00 | ✅ Ishchi |
| Yakshanba | - | - | ❌ Dam olish |

**Tashkilot providerni faqat "ishchi" vaqtlarda tayinlaydi.**

---

## 5. Daromad va Moliya

### 5.1 Earnings (Daromadlar)
```
Route: /provider/earnings
```

| Section | Elementlar |
|---------|------------|
| Balans | Joriy balans |
| Bu oy | Oylik daromad |
| Bu hafta | Haftalik daromad |
| Yechib olish | Withdraw tugmasi |

**Daromad statistikasi:**
```
┌─────────────────────────────────────────────────────────────────────────────┐
│                          DAROMAD - Yanvar 2025                              │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  💰 JORIY BALANS:                        1,250,000 so'm                    │
│                                          [💳 Yechib olish]                 │
│                                                                             │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │  Bu oy:          2,850,000 so'm    (12 ta vazifa)                  │   │
│  │  O'tgan oy:      2,450,000 so'm    (10 ta vazifa)                  │   │
│  │  O'sish:         +16%                                               │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│                                                                             │
│  📊 DAROMAD GRAFIGI                                                        │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │    ▃ ▅ ▇ █ ▆ ▃ ▇ █ ▄ ▅ ▇ ▃                                        │   │
│  │    1  5  10 15 20 25 30 (kun)                                       │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

### 5.2 Transactions (Tranzaksiyalar)
```
Route: /provider/earnings/transactions
```

| Ustun | Tavsif |
|-------|--------|
| Sana | Qachon |
| Tavsif | Vazifa yoki yechish |
| Tashkilot | Qaysi tashkilotdan |
| Summa | +/- qancha |
| Status | To'langan/Kutilmoqda |

**Tranzaksiya turlari:**
| Tur | Icon | Tavsif |
|-----|------|--------|
| Vazifa to'lovi | 💰 | Bajarilgan ish uchun |
| Yechib olish | 📤 | Kartaga o'tkazish |
| Bonus | 🎁 | Qo'shimcha mukofot |
| Jarima | ⚠️ | Salbiy baho uchun |

---

### 5.3 Withdraw (Pul yechish)
```
Route: /provider/earnings/withdraw
```

| Element | Tavsif |
|---------|--------|
| Mavjud balans | Yechish mumkin bo'lgan |
| Summa | Qancha yechmoqchi |
| Karta | Tanlash yoki qo'shish |
| Komissiya | (agar bo'lsa) |
| Tasdiqlash | SMS kod |

**Yechish shartlari:**
- Minimal summa: 100,000 so'm
- Maksimal: 10,000,000 so'm/kun
- Vaqt: 1-3 ish kuni

---

## 6. Reyting va Sharhlar

### 6.1 My Rating (Mening reytingim)
```
Route: /provider/rating
```

| Section | Elementlar |
|---------|------------|
| Umumiy reyting | 4.9 / 5.0 (123 baho) |
| Kategoriyalar | Sifat, Vaqt, Muomala |
| Trend | Oylik o'zgarish |
| Sharhlar | Tashkilotlardan fikrlar |

**MUHIM:** Providerni TASHKILOT baholaydi, mijoz emas!

**Reyting tafsiloti:**
```
┌─────────────────────────────────────────────────────────────────────────────┐
│                            MENING REYTINGIM                                 │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│                    ⭐⭐⭐⭐⭐                                               │
│                      4.9                                                    │
│                   123 ta baho                                               │
│                                                                             │
│  ┌─────────────────────────────────────────────────────────────────────┐   │
│  │  Ish sifati:      ████████████████████ 4.9                         │   │
│  │  Vaqtga rioya:    ███████████████████░ 4.8                         │   │
│  │  Muomala:         ████████████████████ 5.0                         │   │
│  │  Tozalik:         ███████████████████░ 4.8                         │   │
│  └─────────────────────────────────────────────────────────────────────┘   │
│                                                                             │
│  📈 Reyting trendi: Bu oy +0.1                                             │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

### 6.2 Reviews from Organizations
```
Route: /provider/rating/reviews
```

**Sharh card:**
```
┌─────────────────────────────────────────────────────────────────────────────┐
│  🏢 Milliy Catering                              ⭐⭐⭐⭐⭐  │  15-Yanvar  │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  "Juda yaxshi ishladi. Palov mazasi zo'r bo'ldi, mehmonlar                 │
│   mamnun bo'ldi. Vaqtida keldi, ish joyini toza qoldirdi.                  │
│   Tavsiya qilamiz!"                                                        │
│                                                                             │
│  Vazifa: To'y #234, 150 kishi                                              │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## 7. Profil va Portfolio

### 7.1 My Profile
```
Route: /provider/profile
```

| Section | Elementlar |
|---------|------------|
| Avatar | Professional rasm |
| Asosiy info | Ism, Kategoriya, Tajriba |
| Reyting | Umumiy baho |
| Tashkilotlar | Qayerda ishlaydi |
| Portfolio | Ish namunalari |
| Hujjatlar | Status (tasdiqlangan/yo'q) |

---

### 7.2 Edit Profile
```
Route: /provider/profile/edit
```

| Tab | Elementlar |
|-----|------------|
| Shaxsiy | Ism, Telefon, Email, Manzil |
| Professional | Kategoriya, Tajriba, Malaka |
| Hujjatlar | Yangilash/Qo'shish |
| Portfolio | Rasmlar, Video |

---

### 7.3 Portfolio
```
Route: /provider/portfolio
```

| Element | Tavsif |
|---------|--------|
| Rasmlar | Ish namunalari |
| Video | (Ixtiyoriy) |
| Yangi qo'shish | Media yuklash |
| Tartib | Drag & drop |

**Portfolio tavsiyalari:**
- Kamida 5 ta sifatli rasm
- Turli xil ishlar
- Professional ko'rinish

---

## 8. Tashkilotlar Boshqaruvi

### 8.1 My Organizations (Mening tashkilotlarim)
```
Route: /provider/organizations
```

**Provider bir nechta tashkilotda ishlashi mumkin!**

| Element | Tavsif |
|---------|--------|
| Tashkilotlar ro'yxati | Qayerlarda ishlaydi |
| Asosiy | Default tashkilot |
| Status | Faol/Kutilmoqda |
| Qo'shilish | Yangi tashkilotga ariza |

**Tashkilot card:**
```
┌─────────────────────────────────────────────────────────────────────────────┐
│  🏢 Milliy Catering                              ⭐ Asosiy  │  🟢 Faol    │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  📍 Toshkent                                                               │
│  📅 Qo'shilgan: 15-Mart 2024                                               │
│  📦 Vazifalar: 45 ta                                                       │
│  💰 Daromad: 8,500,000 so'm                                                │
│  ⭐ Reyting: 4.9                                                            │
│                                                                             │
│  [📋 Batafsil]              [❌ Chiqish]                                   │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

### 8.2 Join Organization (Tashkilotga qo'shilish)
```
Route: /provider/organizations/join
```

| Element | Tavsif |
|---------|--------|
| Qidiruv | Tashkilot nomi bo'yicha |
| Ro'yxat | Mavjud tashkilotlar |
| Filter | Shahar, Kategoriya |
| Ariza | Qo'shilish so'rovi |

---

## 9. Xabarlar va Bildirishnomalar

### 9.1 Messages (Xabarlar)
```
Route: /provider/messages
```

**Provider faqat TASHKILOT bilan yozishadi!**

| Element | Tavsif |
|---------|--------|
| Chat ro'yxati | Tashkilotlar bilan |
| Vazifa konteksti | Qaysi vazifa haqida |
| Xabar yozish | Text + Attachment |

---

### 9.2 Notifications (Bildirishnomalar)
```
Route: /provider/notifications
```

| Tur | Tavsif |
|-----|--------|
| Yangi vazifa | Tashkilot tayinladi |
| To'lov | Balansga tushdi |
| Eslatma | Ertangi vazifa |
| Baho | Yangi reyting |
| Tizim | Muhim xabarlar |

---

## 10. Sozlamalar

### 10.1 Settings
```
Route: /provider/settings
```

| Section | Elementlar |
|---------|------------|
| Bildirishnomalar | Push, SMS, Email |
| Til | UZ/RU/EN |
| Xavfsizlik | Parol, 2FA |
| To'lov | Karta ma'lumotlari |
| Hisobni o'chirish | Account delete |

---

### 10.2 Notification Settings
```
Route: /provider/settings/notifications
```

| Bildirishnoma | Push | SMS |
|---------------|------|-----|
| Yangi vazifa | ✅ | ✅ |
| Eslatma (1 kun oldin) | ✅ | ✅ |
| Eslatma (1 soat oldin) | ✅ | ❌ |
| To'lov | ✅ | ✅ |
| Yangi baho | ✅ | ❌ |

---

## 11. Yordam

### 11.1 Help Center
```
Route: /provider/help
```

| Section | Elementlar |
|---------|------------|
| FAQ | Ko'p so'raladigan savollar |
| Qo'llanma | Video darsliklar |
| Maslahatlar | Professional tips |
| Aloqa | Support |

---

### 11.2 Report Problem
```
Route: /provider/help/report
```

| Element | Tavsif |
|---------|--------|
| Vazifa tanlash | Qaysi vazifa haqida |
| Muammo turi | Tanlash |
| Tavsif | Batafsil |
| Rasm | Dalil |
| Yuborish | Tashkilotga xabar |

---

## 12. Sahifalar Xaritasi

```
/provider
├── /provider/welcome
├── /provider/login
├── /provider/register
├── /provider/pending
├── /provider/dashboard
├── /provider/tasks
│   ├── /provider/tasks/:id
│   └── /provider/tasks/:id/progress
├── /provider/calendar
│   └── /provider/calendar/availability
├── /provider/earnings
│   ├── /provider/earnings/transactions
│   └── /provider/earnings/withdraw
├── /provider/rating
│   └── /provider/rating/reviews
├── /provider/profile
│   ├── /provider/profile/edit
│   └── /provider/portfolio
├── /provider/organizations
│   └── /provider/organizations/join
├── /provider/messages
├── /provider/notifications
├── /provider/settings
│   └── /provider/settings/notifications
└── /provider/help
    └── /provider/help/report
```

---

## 13. Navigatsiya

### Bottom Navigation (Mobile)
| Icon | Nom | Route |
|------|-----|-------|
| 🏠 | Bosh sahifa | /provider/dashboard |
| 📦 | Vazifalar | /provider/tasks |
| 📅 | Kalendar | /provider/calendar |
| 💰 | Daromad | /provider/earnings |
| 👤 | Profil | /provider/profile |

---

## 14. Muhim Farqlar

| Eski Model ❌ | Yangi Model ✅ |
|--------------|---------------|
| Provider mijozni ko'radi | Provider faqat VAZIFA ko'radi |
| Mijoz bilan chat | TASHKILOT bilan chat |
| Mijoz provider tanlaydi | TASHKILOT provider tayinlaydi |
| Provider narx belgilaydi | TASHKILOT narx belgilaydi |
| To'lov mijozdan | To'lov TASHKILOT orqali |

**Afzalliklari:**
1. Provider faqat ishiga e'tibor beradi
2. Tashkilot sifatni nazorat qiladi
3. Kafolatlangan to'lov
4. Professional muhit
