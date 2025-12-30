# CaterPro - Mijoz (User) Sahifalari

> Xizmatdan foydalanuvchi oddiy foydalanuvchilar uchun barcha sahifalar
> **MUHIM:** Mijozlar to'g'ridan-to'g'ri providerlarni emas, XIZMAT PAKETLARINI tanlaydi!

---

## 🔄 Yangilangan Model

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                           YANGI BUYURTMA MODELI                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│   👤 MIJOZ                                                                  │
│      │                                                                      │
│      ▼                                                                      │
│   📦 XIZMAT (Service) tanlaydi                                             │
│      │  • "To'y uchun Premium paket"                                       │
│      │  • "Tug'ilgan kun Comfort paketi"                                   │
│      │  • "Korporativ tadbir Business"                                     │
│      │                                                                      │
│      ▼                                                                      │
│   🏢 TASHKILOT (Org Admin)                                                 │
│      │  • Buyurtmani ko'radi                                               │
│      │  • Providerlarni tayinlaydi                                         │
│      │  • Oshpaz, Ofitsiant, Arenda...                                     │
│      │                                                                      │
│      ▼                                                                      │
│   🧑‍🍳 PROVIDERLAR                                                          │
│      • Ishni bajaradi                                                       │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘

Mijoz BILMAYDI qaysi oshpaz yoki ofitsiant kelishini.
Mijoz faqat XIZMAT SIFATI va PAKET turini tanlaydi.
```

---

## 1. Autentifikatsiya Sahifalari

### 1.1 Welcome Screen (Kirish sahifasi)
```
Route: /
```

| Element | Tavsif |
|---------|--------|
| Logo | CaterPro logotipi |
| Slogan | "Tadbiringizni mukammal qiling" |
| Kirish tugmasi | Login sahifasiga o'tish |
| Ro'yxatdan o'tish | Register sahifasiga o'tish |
| Til tanlash | UZ / RU / EN |

---

### 1.2 Login (Kirish)
```
Route: /login
```

| Element | Tavsif |
|---------|--------|
| Telefon raqam | +998 XX XXX XX XX formati |
| Parol | Maxfiy parol kiritish |
| Eslab qolish | Checkbox - sessiyani saqlash |
| Kirish tugmasi | Validatsiya va login |
| Parolni unutdim | Parol tiklash sahifasiga |
| SMS orqali kirish | OTP kod bilan kirish |
| Google login | OAuth orqali |
| Ro'yxatdan o'tish | Register sahifasiga link |

**Validatsiya:**
- Telefon: O'zbek formati tekshiruvi
- Parol: Minimum 6 belgi
- 3 marta noto'g'ri kirishda CAPTCHA

---

### 1.3 Register (Ro'yxatdan o'tish)
```
Route: /register
```

**Step 1: Telefon tasdiqlash**
| Element | Tavsif |
|---------|--------|
| Telefon raqam | +998 XX XXX XX XX |
| SMS yuborish | OTP kod yuborish |
| OTP kiritish | 6 xonali kod |
| Qayta yuborish | 60 soniyadan keyin |

**Step 2: Shaxsiy ma'lumotlar**
| Element | Tavsif |
|---------|--------|
| Ism | Foydalanuvchi ismi |
| Familiya | Foydalanuvchi familiyasi |
| Email | Ixtiyoriy email manzil |
| Parol | Yangi parol yaratish |
| Parol tasdiqlash | Parolni takrorlash |

**Step 3: Qo'shimcha (Ixtiyoriy)**
| Element | Tavsif |
|---------|--------|
| Tug'ilgan sana | Sana tanlash |
| Shahar | Dropdown ro'yxat |
| Profil rasmi | Rasm yuklash |

**Validatsiya:**
- Telefon: Unikal bo'lishi shart
- Parol: Min 6 belgi, 1 raqam
- Email: Format tekshiruvi

---

### 1.4 Forgot Password (Parolni tiklash)
```
Route: /forgot-password
```

**Step 1:**
| Element | Tavsif |
|---------|--------|
| Telefon raqam | Ro'yxatdan o'tgan raqam |
| SMS yuborish | OTP yuborish |

**Step 2:**
| Element | Tavsif |
|---------|--------|
| OTP kod | 6 xonali tasdiqlash kodi |
| Yangi parol | Yangi parol kiritish |
| Tasdiqlash | Parolni takrorlash |
| Saqlash | Parolni yangilash |

---

## 2. Asosiy Sahifalar

### 2.1 Home (Bosh sahifa)
```
Route: /home
```

| Section | Elementlar |
|---------|------------|
| Header | Logo, Qidiruv, Bildirishnomalar, Profil |
| Banner | Reklama slideri (aksiyalar, chegirmalar) |
| Tadbir turlari | To'y, Tug'ilgan kun, Korporativ, Boshqa |
| Xizmat paketlari | Mashhur paketlar (Start, Comfort, Premium, Business) |
| Qanday ishlaydi | 3 qadam tushuntirish |
| Sharhlar | Mijozlar fikrlari |
| Footer | Navigatsiya, Yordam, Ijtimoiy tarmoqlar |

---

### 2.2 Services Catalog (Xizmatlar katalogi)
```
Route: /services
```

**Bu sahifada mijoz XIZMAT PAKETLARINI ko'radi, PROVIDERLARNI EMAS!**

| Filter | Variantlar |
|--------|------------|
| Tadbir turi | To'y, Tug'ilgan kun, Korporativ, Boshqa |
| Xizmat darajasi | Start, Comfort, Premium, Business |
| Mehmonlar soni | 10-50, 50-100, 100-200, 200+ |
| Narx oralig'i | Min - Max slider |
| Xizmat turlari | Faqat ovqat, To'liq xizmat, Arenda... |

**Xizmat paket card:**
```
┌─────────────────────────────────────────────────────────────┐
│  🍽️ TO'Y PREMIUM PAKET                           ⭐ 4.8    │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  📝 Paket tarkibi:                                         │
│  ├── ✅ Milliy taomlar (5 xil)                             │
│  ├── ✅ Ofitsiantlar xizmati                               │
│  ├── ✅ Idish-tovoq to'plami                               │
│  ├── ✅ Stol bezatish                                      │
│  └── ✅ Transport                                          │
│                                                             │
│  👥 50-150 kishi uchun                                     │
│  💰 Kishi boshiga: 85,000 so'm dan                         │
│                                                             │
│  [📖 Batafsil]              [🛒 Buyurtma berish]           │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

---

### 2.3 Service Detail (Xizmat tafsiloti)
```
Route: /services/:id
```

| Section | Elementlar |
|---------|------------|
| Gallery | Paket rasmlari (oldingi ishlar) |
| Sarlavha | Paket nomi + Reyting |
| Tavsif | Batafsil tavsif |
| Paket tarkibi | Nimalar kiradi |
| Darajalar | Start/Comfort/Premium/Business narxlari |
| Menyu variantlari | (Ovqat uchun) Taomlar ro'yxati |
| Qo'shimcha xizmatlar | Tanlab qo'shish mumkin |
| Sharhlar | Mijozlar fikrlari |
| FAQ | Ko'p so'raladigan savollar |
| Buyurtma tugmasi | "Buyurtma berish" |

**Xizmat darajalari:**
```
┌─────────────────────────────────────────────────────────────────────────────┐
│                         XIZMAT DARAJALARINI TANLANG                         │
├─────────────────┬─────────────────┬─────────────────┬───────────────────────┤
│     ⭐          │     ⭐⭐         │     ⭐⭐⭐       │     ⭐⭐⭐⭐           │
│    START        │    COMFORT      │    PREMIUM      │    BUSINESS           │
├─────────────────┼─────────────────┼─────────────────┼───────────────────────┤
│ 45,000 so'm     │ 65,000 so'm     │ 85,000 so'm     │ 120,000 so'm         │
│ /kishi          │ /kishi          │ /kishi          │ /kishi                │
├─────────────────┼─────────────────┼─────────────────┼───────────────────────┤
│ • 3 xil taom    │ • 5 xil taom    │ • 7 xil taom    │ • 10+ xil taom       │
│ • Oddiy idish   │ • Sifatli idish │ • Premium idish │ • VIP idish          │
│ • 1 ofitsiant/  │ • 1 ofitsiant/  │ • 1 ofitsiant/  │ • 1 ofitsiant/       │
│   25 kishi      │   20 kishi      │   15 kishi      │   10 kishi           │
│                 │ • Stol bezak    │ • To'liq bezak  │ • Ekskluziv bezak    │
│                 │                 │ • Fotograf      │ • Foto + Video       │
├─────────────────┼─────────────────┼─────────────────┼───────────────────────┤
│   [Tanlash]     │   [Tanlash]     │  [Tavsiyali ✓]  │   [Tanlash]          │
└─────────────────┴─────────────────┴─────────────────┴───────────────────────┘
```

---

### 2.4 Booking (Buyurtma berish)
```
Route: /booking/:serviceId
```

**Step 1: Tadbir ma'lumotlari**
| Element | Tavsif |
|---------|--------|
| Tadbir turi | To'y, Tug'ilgan kun, Korporativ, Boshqa |
| Tadbir nomi | "Alisher va Malika to'yi" (ixtiyoriy) |
| Sana | Kalendar orqali tanlash |
| Boshlanish vaqti | Time picker |
| Tugash vaqti | Time picker (taxminiy) |
| Mehmonlar soni | Raqam kiritish |

**Step 2: Manzil**
| Element | Tavsif |
|---------|--------|
| Manzil turi | Uy, To'yxona, Restoran, Boshqa |
| Shahar | Dropdown |
| Tuman | Dropdown |
| To'liq manzil | Text input |
| Mo'ljal | Qo'shimcha izoh |
| Xarita | Xaritadan belgilash |

**Step 3: Xizmat darajasi tanlash**
| Element | Tavsif |
|---------|--------|
| Daraja | Start / Comfort / Premium / Business |
| Paket tarkibi | Tanlangan darajadagi xizmatlar |
| Qo'shimcha xizmatlar | Checkbox list (qo'shish mumkin) |

**Step 4: Menyu tanlash (agar ovqat xizmati bo'lsa)**
| Element | Tavsif |
|---------|--------|
| Menyu varianti | Tayyor menyu variantlari |
| Taomlar | Tanlangan menyudagi taomlar |
| Maxsus talablar | Allergiya, Halol, Vegetarian... |
| Qo'shimcha taom | Qo'shish mumkin (+narx) |

**Step 5: Maxsus talablar**
| Element | Tavsif |
|---------|--------|
| Izoh | Textarea - maxsus istaklar |
| Allergiya | Mahsulot cheklovlari |
| Rasm yuklash | Misol rasmlar (ixtiyoriy) |

**Step 6: Narx va Tasdiqlash**
| Element | Tavsif |
|---------|--------|
| Narx kalkulyatsiyasi | Avtomatik hisob |
| Chegirma kodi | Promo code kiritish |
| Yakuniy narx | Jami summa |
| To'lov usuli | Naqd, Karta, Click, Payme |
| Oldindan to'lov | 30-50% avans |
| Shartnoma | Foydalanish shartlari checkbox |
| Tasdiqlash | Buyurtmani yuborish |

**Narx kalkulyatsiyasi:**
```
┌─────────────────────────────────────────────────────────────┐
│                    BUYURTMA XULOSASI                        │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  📦 Xizmat: To'y Premium Paket                             │
│  ⭐ Daraja: PREMIUM                                         │
│  👥 Mehmonlar: 100 kishi                                   │
│  📅 Sana: 15-Fevral 2025, 16:00                            │
│                                                             │
│  ─────────────────────────────────────────────────────────  │
│                                                             │
│  Asosiy xizmat (100 × 85,000):        8,500,000 so'm       │
│  Qo'shimcha: Fotograf:                  500,000 so'm       │
│  Qo'shimcha: Tort (5 kg):               350,000 so'm       │
│  ─────────────────────────────────────────────────────────  │
│  Jami:                                9,350,000 so'm       │
│  Chegirma (HAPPY10):                   -935,000 so'm       │
│  ─────────────────────────────────────────────────────────  │
│  💰 YAKUNIY NARX:                     8,415,000 so'm       │
│                                                             │
│  📌 Oldindan to'lov (30%):            2,524,500 so'm       │
│  📌 Tadbir kunida:                    5,890,500 so'm       │
│                                                             │
│                    [✅ Buyurtma berish]                     │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

---

### 2.5 Order Confirmation (Buyurtma tasdiqlandi)
```
Route: /booking/success/:orderId
```

| Element | Tavsif |
|---------|--------|
| Success icon | Yashil checkmark |
| Xabar | "Buyurtmangiz qabul qilindi!" |
| Buyurtma ID | #12345 |
| Keyingi qadam | "Tez orada siz bilan bog'lanamiz" |
| Eslatma | "30 daqiqa ichida tasdiqlash xabari keladi" |
| Tugmalar | "Buyurtmani ko'rish", "Bosh sahifa" |

---

### 2.6 Orders List (Buyurtmalar ro'yxati)
```
Route: /orders
```

| Tab | Tavsif |
|-----|--------|
| Faol | Hozirgi/kelgusi buyurtmalar |
| Tarix | O'tgan buyurtmalar |
| Bekor qilingan | Rad etilgan buyurtmalar |

**Order Card:**
```
┌─────────────────────────────────────────────────────────────┐
│  📦 Buyurtma #12345                              🟢 Faol   │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  🍽️ To'y Premium Paket                                     │
│  📅 15-Fevral 2025, 16:00                                  │
│  👥 100 kishi                                              │
│  📍 Toshkent, Yunusobod tumani                             │
│  💰 8,415,000 so'm                                         │
│                                                             │
│  Status: ✅ Tasdiqlandi - Tayyorgarlik boshlandi           │
│                                                             │
│  [📋 Batafsil]                          [💬 Chat]          │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

---

### 2.7 Order Detail (Buyurtma tafsiloti)
```
Route: /orders/:orderId
```

| Section | Elementlar |
|---------|------------|
| Status | Joriy holat + Timeline |
| Tadbir info | Tur, Sana, Vaqt, Manzil, Mehmonlar |
| Xizmat | Paket nomi, Daraja, Tarkibi |
| Narx | To'liq hisob-kitob |
| To'lov holati | To'langan/Qolgan |
| Aloqa | Tashkilot bilan chat |
| Bekor qilish | (agar imkon bo'lsa) |

**Status Timeline:**
```
┌─────────────────────────────────────────────────────────────┐
│                    BUYURTMA HOLATI                          │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  ✅ Buyurtma qabul qilindi          25-Yan, 14:32          │
│     │                                                       │
│  ✅ Tasdiqlandi                     25-Yan, 15:10          │
│     │                                                       │
│  ✅ Avans to'landi (30%)            25-Yan, 16:45          │
│     │                                                       │
│  🔵 Tayyorgarlik boshlandi          10-Fev, 09:00          │
│     │  └── Mahsulotlar xarid qilindi                       │
│     │  └── Jamoa tayinlandi                                │
│     │                                                       │
│  ⚪ Xizmat ko'rsatilmoqda           15-Fev, 16:00          │
│     │                                                       │
│  ⚪ Yakunlandi                      15-Fev, 23:00          │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

**MUHIM:** Mijoz qaysi oshpaz yoki ofitsiant kelishini BILMAYDI.
Faqat "Jamoa tayinlandi" xabarini ko'radi.

---

### 2.8 Rate & Review (Baholash)
```
Route: /review/:orderId
```

**Xizmat tugagandan keyin:**

| Element | Tavsif |
|---------|--------|
| Umumiy baho | 1-5 yulduz |
| Ovqat sifati | 1-5 yulduz |
| Xizmat sifati | 1-5 yulduz |
| Vaqtga rioya | 1-5 yulduz |
| Tozalik | 1-5 yulduz |
| Tavsiya | "Tavsiya qilasizmi?" Ha/Yo'q |
| Izoh | Textarea - batafsil fikr |
| Rasm qo'shish | Tadbir rasmlari |
| Yuborish | Sharhni saqlash |

**MUHIM:** Mijoz XIZMAT PAKETINI baholaydi, alohida providerni EMAS!

---

## 3. Profil Sahifalari

### 3.1 Profile (Shaxsiy kabinet)
```
Route: /profile
```

| Section | Elementlar |
|---------|------------|
| Avatar | Profil rasmi + tahrirlash |
| Asosiy info | Ism, Familiya, Telefon, Email |
| Statistika | Buyurtmalar soni, Sarflangan summa |
| Menyu | Sozlamalar, Manzillar, To'lov, Yordam |

---

### 3.2 Edit Profile (Profilni tahrirlash)
```
Route: /profile/edit
```

| Element | Tavsif |
|---------|--------|
| Avatar | Rasm yuklash/o'zgartirish |
| Ism | Text input |
| Familiya | Text input |
| Email | Email input |
| Tug'ilgan sana | Date picker |
| Telefon | O'zgartirish (SMS tasdiqlash) |
| Saqlash | O'zgarishlarni saqlash |

---

### 3.3 Saved Addresses (Saqlangan manzillar)
```
Route: /profile/addresses
```

| Element | Tavsif |
|---------|--------|
| Manzillar ro'yxati | Saqlangan manzillar |
| Yangi qo'shish | Yangi manzil qo'shish |
| Asosiy belgilash | Default manzil tanlash |
| Tahrirlash | Mavjud manzilni o'zgartirish |
| O'chirish | Manzilni o'chirish |

**Manzil formasi:**
| Element | Tavsif |
|---------|--------|
| Nom | "Uy", "To'yxona", "Ish joyi" |
| Shahar | Dropdown |
| Tuman | Dropdown |
| Ko'cha/Mahalla | Text input |
| Uy/Xonadon | Text input |
| Mo'ljal | Qo'shimcha izoh |
| Xarita | Xaritadan tanlash |

---

### 3.4 Payment Methods (To'lov usullari)
```
Route: /profile/payment
```

| Element | Tavsif |
|---------|--------|
| Saqlangan kartalar | **** **** **** 1234 |
| Yangi karta | Karta qo'shish |
| Click | Click hisobi ulash |
| Payme | Payme ulash |
| O'chirish | Kartani o'chirish |

---

### 3.5 Settings (Sozlamalar)
```
Route: /profile/settings
```

| Section | Elementlar |
|---------|------------|
| Til | UZ / RU / EN |
| Bildirishnomalar | Push, SMS, Email sozlamalari |
| Maxfiylik | Ma'lumotlar ko'rinishi |
| Xavfsizlik | Parol o'zgartirish, 2FA |
| Hisobni o'chirish | Account delete |

---

### 3.6 Notifications (Bildirishnomalar)
```
Route: /notifications
```

| Tur | Tavsif |
|-----|--------|
| Buyurtma | Status o'zgarishlari |
| Promo | Aksiya va chegirmalar |
| Eslatma | Yaqinlashayotgan tadbirlar |
| Tizim | Muhim xabarlar |

---

## 4. Qo'shimcha Sahifalar

### 4.1 Chat (Xabarlar)
```
Route: /chat
Route: /chat/:orderId
```

**MUHIM:** Mijoz TASHKILOT bilan yozishadi, alohida provider bilan EMAS!

| Element | Tavsif |
|---------|--------|
| Chat ro'yxati | Buyurtmalar bo'yicha suhbatlar |
| Xabar yozish | Text input + Yuborish |
| Rasm yuborish | Attachment |
| Buyurtma info | Qaysi buyurtma haqida |

---

### 4.2 Help & Support (Yordam)
```
Route: /help
```

| Section | Elementlar |
|---------|------------|
| FAQ | Ko'p so'raladigan savollar |
| Qo'llanma | Foydalanish bo'yicha |
| Aloqa | Support bilan bog'lanish |
| Shikoyat | Muammo xabar qilish |

---

### 4.3 About (Dastur haqida)
```
Route: /about
```

| Element | Tavsif |
|---------|--------|
| Loyiha haqida | CaterPro tavsifi |
| Versiya | App versiyasi |
| Foydalanish shartlari | Terms of Service |
| Maxfiylik siyosati | Privacy Policy |
| Ijtimoiy tarmoqlar | Instagram, Telegram, Facebook |

---

## 5. Sahifalar Xaritasi (Sitemap)

```
/
├── /login
├── /register
├── /forgot-password
├── /home
├── /services                    ← Xizmat paketlari katalogi
│   └── /services/:id            ← Paket tafsiloti
├── /booking/:serviceId          ← Buyurtma berish
│   └── /booking/success/:id
├── /orders
│   └── /orders/:orderId
├── /review/:orderId
├── /chat
│   └── /chat/:orderId
├── /notifications
├── /profile
│   ├── /profile/edit
│   ├── /profile/addresses
│   ├── /profile/payment
│   └── /profile/settings
├── /help
└── /about
```

---

## 6. Navigatsiya

### Bottom Navigation (Mobile)
| Icon | Nom | Route |
|------|-----|-------|
| 🏠 | Bosh sahifa | /home |
| 🍽️ | Xizmatlar | /services |
| 📦 | Buyurtmalar | /orders |
| 💬 | Xabarlar | /chat |
| 👤 | Profil | /profile |

### Header (Desktop)
| Element | Tavsif |
|---------|--------|
| Logo | Bosh sahifaga link |
| Xizmatlar | Mega menu (kategoriyalar) |
| Qidiruv | Global search |
| Bildirishnomalar | Bell icon + badge |
| Profil | Dropdown menu |

---

## 7. Muhim Farqlar (Eski vs Yangi Model)

| Eski Model ❌ | Yangi Model ✅ |
|--------------|---------------|
| Mijoz providerni tanlaydi | Mijoz XIZMAT PAKETINI tanlaydi |
| Provider profili ko'rinadi | Faqat PAKET tafsiloti ko'rinadi |
| Mijoz-Provider chat | Mijoz-TASHKILOT chat |
| Provider reytingi | XIZMAT reytingi |
| Provider bilan kelishuv | Tashkilot bilan kelishuv |

**Afzalliklari:**
1. Mijoz uchun sodda - faqat paket tanlaydi
2. Tashkilot providerlarni optimal taqsimlaydi
3. Sifat nazorati tashkilot qo'lida
4. Provider band bo'lsa, boshqasi tayinlanadi
