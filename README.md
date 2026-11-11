# 🐍 Pytonchi.uz — Pythonni Noldan Oson O'rganish Platformasi

O'zbek tilida Python dasturlash tilini yangi boshlovchilar uchun noldan, oson va interaktiv o'rgatuvchi zamonaviy veb-platforma (**pytonchi.uz**).

---

## 🌟 Asosiy Imkoniyatlar (Key Features)

1. **⚡ Brauzerda To'g'ridan-to'g'ri Python Kodini Bajarish (Pyodide / WebAssembly):**
   - Hech qanday server sozlash talab qilinmaydi.
   - Kod o'quvchining o'z brauzerida xavfsiz va bir zumda ishlaydi (Monaco Editor / VS Code asosi).
2. **📖 O'zbek Tilidagi 7 ta Qadamma-qadam Darslar:**
   - 1-Dars: Salom Python va `print()` funksiyasi.
   - 2-Dars: O'zgaruvchilar va Ma'lumot turlari (`str`, `int`, `float`, `bool`).
   - 3-Dars: `input()` va `f-string` orqali matn tuzish.
   - 4-Dars: Qaror qabul qilish (`if`, `elif`, `else` va indentation).
   - 5-Dars: Takrorlanish kuchi (`for` va `while` sikllari).
   - 6-Dars: To'plamlar: Ro'yxat (`list`) va Lug'at (`dict`).
   - 7-Dars: O'z Funksiyangizni Yaratish (`def` va `return`).
3. **🤖 Aqlli AI Ustozi (Error Explainer):**
   - O'quvchi xato qilganda (masalan, `IndentationError`, `SyntaxError`, `NameError`, `TypeError`), AI xatoni o'zbek tilida bolalarcha sodda va tushunarli qilib tushuntirib beradi va to'g'ri kod namunasini ko'rsatadi.
4. **🎮 Gamifikatsiya va Natijalar:**
   - Har bir to'g'ri bajarilgan vazifa va test uchun **XP ballari**.
   - Kunlik ketma-ketlik (**Streak**) olovi.
   - O'quvchi darajasi (**Level**).
   - Maxsus yutuq nishonlari (**Badges**: "Birinchi Qadam", "Yarim Yo'l", "Python Qahramoni").
5. **🏆 Peshqadamlar Jadvali (Leaderboard):**
   - Eng faol va ko'p XP to'plagan o'quvchilar ro'yxati.
6. **🔐 Xavfsiz Autentifikatsiya & Yagona Super Admin Qoidasi:**
   - JWT tokenlar va bcrypt xesh bilan ro'yxatdan o'tish va kirish.
   - Tizimda qat'iy ravishda faqat **1 ta yagona Bosh Administrator** (`username: admin`) bo'ladi. Boshqalarga admin huquqi berilishi taqiqlangan.
   - Foydalanuvchilar faqat O'quvchi (Student) yoki O'qituvchi (Teacher) bo'lishi mumkin.
7. **⚙️ Maxsus Administrator Paneli (/admin):**
   - Platforma faolligi statistikasi (foydalanuvchilar, darslar, umumiy XP).
   - Darslar CRUD: yangi dars yaratish, tahrirlash, o'chirish.
   - Testlar CRUD: darslarga test savollarini qo'shish va boshqarish.
   - O'quvchilar va O'qituvchilar boshqaruvi: qidirish, natijalarni ko'rish va o'qituvchilik ruxsatini berish.
   - Standart admin: `username: admin`, `parol: admin123`.
8. **🎓 O'qituvchi Boshqaruv Studiyasi (/teacher):**
   - **Guruhlar & Sinflar:** O'qituvchi 6 xonali unikal kodli guruh ochadi; o'quvchi kod orqali so'rov yuboradi, o'qituvchi bitta bosishda tasdiqlaydi.
   - **Shaxsiy AI Kalitlari (BYOK):** Server bitta umumiy limitga bog'lanib qolmasligi uchun har bir o'qituvchi o'z profiliga shaxsiy **Google Gemini** yoki **xAI Grok** API kalitini kiritadi va tekshiradi.
   - **Hujjatdan Dars Yaratish:** Word (.docx), PDF (.pdf) yoki matnli konspektlarni yuklab, avtomatik darsga aylantirish.
   - **AI Test Generatori:** O'qituvchining shaxsiy kaliti orqali 10 ta yoki 20 ta test savolini bir necha soniyada tuzish va darsga biriktirish.
9. **📱 Universal Moslashuvchanlik (Phone, Tablet, Laptop Responsive UI):**
   - **Telefon (Mobile <768px):** Pastki mobil menyu (Bottom Nav: Darslar, Muharrir, Guruh, Reyting), segmentli almashish (`[Nazariya] | [Kod] | [Natija]`) va tortib ochiluvchi Drawer menyusi.
   - **Planshet (Tablet 768–1024px):** 68px ixcham piktogrammali rels (Sidebar Rail) va 50/50 qulay ishchi maydoni.
   - **Noutbuk / Kompyuter (>1024px):** Linear/Notion uslubidagi yig'iluvchi keng Sidebar va to'liq uch ustunli professional dasturlash studiyasi.
   - **Admin va O'qituvchilar uchun:** Doimiy ochiq vertikal chap menyu.
10. **🔄 Ikki Yo'nalishli Ta'lim — Kurs Almashtirgich (Course Switcher):**
   - **Ommaviy Mustaqil Ta'lim:** Har qanday oddiy odam saytga kirib, admin tuzgan 7+ darslar va topshiriqlarni mustaqil o'rganadi.
   - **Ustoz / Sinf Ta'limi:** Guruhga a'zo bo'lgan o'quvchilar sidebar tepasidagi almashtirgich orqali o'z ustozi tuzgan maxsus dars xaritasi, ma'ruza konspektlari va topshiriqlariga bir zumda o'tishadi.

---

## 🚀 O'rnatish va Ishga Tushirish (Quick Start)

### 1. Loyihani yuklab olish va virtual muhit yaratish:
```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 2. Bog'liqliklarni o'rnatish:
```bash
pip install -r requirements.txt
```

### 3. Darslar bazasini to'ldirish (Seeding):
```bash
python -m backend.app.seeds.curriculum
```

### 4. Serverni ishga tushirish:
```bash
python run.py
```

Brauzeringizda oching:
- 🌐 **Platforma:** [http://localhost:8000](http://localhost:8000)
- 📚 **API Swagger Hujjatlari:** [http://localhost:8000/docs](http://localhost:8000/docs)

---

## 🧪 Testlarni Ishga Tushirish
Barcha backend testlarini tekshirish uchun:
```bash
pytest tests/ -v
```

---

## 📂 Loyiha Tuzilishi (Project Structure)
```
DARS/
├── backend/
│   └── app/
│       ├── __init__.py
│       ├── auth.py              # JWT va parol xeshlash
│       ├── database.py          # SQLite va SQLAlchemy ulanishi
│       ├── models.py            # Foydalanuvchi, dars va test modellari
│       ├── schemas.py           # Pydantic JSON sxemalari
│       ├── main.py              # FastAPI dasturi va statik fayllar ulash
│       ├── routers/
│       │   ├── auth.py          # /api/auth marshrutlari
│       │   ├── lessons.py       # /api/lessons va /api/quizzes marshrutlari
│       │   ├── ai.py            # /api/ai/explain tahlilchisi
│       │   └── leaderboard.py   # /api/leaderboard
│       └── seeds/
│           └── curriculum.py    # O'zbek tilidagi 7 ta dars va testlar
├── frontend/
│   └── public/
│       ├── index.html           # Tailwind, Monaco, Pyodide interfeysi
│       └── app.js               # Frontend mantiq va brauzer Python runneri
├── tests/
│   └── test_api.py              # Avtomatlashtirilgan pytest testlari
├── requirements.txt             # Python paketlari
├── run.py                       # Serverni bir buyruq bilan yoqish
└── README.md
```
# Pytonchi.uz
