# TechMarket — 2025 yillik savdo tahlili (Excel dashboard)

![Dashboard](images/dashboard.png)

O'zbekistonda elektronika va maishiy texnika sotuvchi kompaniyaning 2025 yillik savdo ma'lumotlarini tozalab, tahlil qildim va Excelda interaktiv dashboard yasadim.

> **Eslatma:** ma'lumotlar sun'iy yaratilgan (sintetik dataset), haqiqiy kompaniyaga tegishli emas. Loyiha o'quv va portfolio maqsadida qilingan.

## Maqsad

Savdo ma'lumotiga qarab quyidagi savollarga javob topish:

- Qaysi viloyat eng ko'p daromad keltiradi?
- Qaysi mahsulot kategoriyalari asosiy daromad manbai?
- Savdo yil davomida qanday o'zgaradi, qaysi oylarda eng yuqori?
- Qaysi sotuv kanali (do'kon, onlayn sayt, Telegram bot) eng samarali?

## Ma'lumot haqida

| Ko'rsatkich | Qiymat |
|---|---|
| Davr | 2025 yil 1-yanvar – 31-dekabr |
| Buyurtmalar soni | 1 200 (tozalashdan keyin) |
| Hudud | O'zbekistonning 10 ta viloyati |
| Kategoriyalar | Smartfon, Noutbuk, Televizor, Maishiy texnika, Aksessuar |
| Kanallar | Do'kon, Onlayn sayt, Telegram bot |
| Valyuta | So'm (UZS) |

Xom ma'lumotda real hayotdagidek xatolar bor edi: takroriy qatorlar, bo'sh qiymatlar, bir xil narsaning turlicha yozilishi (`Toshkent`, `toshkent shahri`, `telegram`) va harf kattaligi farqlari.

## Qilingan ishlar

1. **Ma'lumotni tozalash**
   - Takroriy buyurtmalarni o'chirdim (1 212 → 1 200 qator).
   - Matnlarni standartlashtirdim (viloyat va kanal nomlari).
   - Bo'sh qiymatlarni (shahar, to'lov usuli) qayta ishladim.
2. **Hisoblash**
   - `Daromad = Miqdor × Narx × (1 − Chegirma)` formulasi.
3. **Pivot Table va PivotChart**
   - Oy/chorak, viloyat, kategoriya va kanal bo'yicha tahlil.
4. **Interaktiv dashboard**
   - KPI kartalar: jami daromad, buyurtmalar soni, o'rtacha chek.
   - 4 ta diagramma va chorak bo'yicha Slicer. Slicer bosilganda KPI kartalar va diagrammalar birga o'zgaradi.
5. **Xulosa va tavsiyalar** (pastda).

## Ishlatilgan vositalar

- Microsoft Excel
- Pivot Table, PivotChart, Slicer
- `GETPIVOTDATA`, `SUMIFS`, `COUNTA`
- Ma'lumotni tozalash: Remove Duplicates, Find & Replace, TRIM/PROPER
- *(Agar ishlatgan bo'lsangiz: Power Query)*

## Asosiy topilmalar

- **Toshkent shahri** jami daromadning taxminan **30%** ini beradi (~1,2 mlrd so'm) va keyingi viloyatdan taxminan 2,7 baravar ko'p.
- **Smartfon va noutbuk** daromadning taxminan **65%** ini tashkil qiladi.
- Savdo **oktabr–noyabrda** eng yuqori nuqtaga chiqadi (~490 mln so'm), yanvarga nisbatan taxminan 2,5 baravar ko'p.
- **Do'kon** kanali daromadning taxminan yarmini beradi, onlayn sayt va Telegram bot qolgan qismini bo'lishadi.

Umumiy ko'rsatkichlar: jami daromad **3 963 625 000 so'm**, o'rtacha chek **3 303 021 so'm**.

## Tavsiyalar

1. **Zaxirani oldindan tayyorlash.** Talab oktabrdan oshadi, shuning uchun sentabrda zaxira va marketingni kuchaytirish kerak.
2. **Viloyatlarda o'sish.** Toshkentdan tashqari viloyatlarda savdo past, ularda reklama va yetkazib berishni rivojlantirish imkoniyati bor.
3. **Onlayn kanallar.** Onlayn sayt va Telegram bot ulushini oshirish mumkin, ayniqsa yuqori narxli kategoriyalarda.

## Repository tuzilishi

```
techmarket-sales-analysis/
├── README.md
├── TechMarket_Dashboard.xlsx    # hamma varaqlar shu fayl ichida
└── images/
    └── dashboard.png
```

### Excel fayl varaqlari

| Varaq | Mazmuni |
|---|---|
| `README` | Loyiha tavsifi |
| `Dashboard` | Interaktiv dashboard |
| `Pivots` | Dashboard uchun Pivot jadvallar |
| `Sales_Clean` | Tozalangan ma'lumot |
| `Sales_Raw` | Xom ma'lumot (tozalashdan oldingi holat) |
| `Data_Dictionary` | Ustunlar izohi |

## Faylni ochish bo'yicha eslatma

Dashboardni to'liq ishlatish uchun faylni **Microsoft Excel**da oching (Slicer va PivotChart boshqa dasturlarda to'g'ri ishlamasligi mumkin). Agar manba bilan bog'liq yangilash xatosi chiqsa, **Refresh All** ni bosmang, fayl tayyor holatda saqlangan.

## Keyingi qadamlar

- Shu ma'lumotni SQL ga yuklab, so'rovlar bilan tahlil qilish.
- Dashboardni Power BI da qayta yasash.
- Python (pandas) bilan tahlil va vizualizatsiya qo'shish.

## Muallif

**[Ismingiz Familiyangiz]**
LinkedIn: [havola]
Email: [pochta]
