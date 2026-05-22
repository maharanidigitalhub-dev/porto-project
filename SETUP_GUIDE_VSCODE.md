# 📂 SETUP PORTO DI VS CODE - LOGO & FOTO MUNCUL

Supaya logo dan foto muncul, kamu perlu **3 things**:

1. ✅ File HTML (`Portfolio_-_Navy_WITH_BRANDING_ANIMATION.html`)
2. ✅ JavaScript (`image-slot.js`)
3. ✅ Assets folder (`logos/`, `uploads/`)

---

## 🎯 STEP 1: Setup Folder Structure

Di VS Code, buat struktur ini:

```
your-porto-project/
├── Portfolio - Navy.html  ← Ganti dengan file baru
├── image-slot.js           ← Copy dari bundle
├── logos/                  ← Copy folder ini
│   ├── msglow.png
│   ├── erha.png
│   ├── thomascook.png
│   └── ... (21 logos total)
└── uploads/                ← Copy folder ini
    ├── Logo Portfolio/
    ├── case-studies/
    └── ... (aset lainnya)
```

---

## 🚀 STEP 2: Copy Files dari Bundle

### Dari bundle outputs, copy:

**1. Main file:**
```
Portfolio_-_Navy_WITH_BRANDING_ANIMATION.html
    ↓
Rename: Portfolio - Navy.html (atau ganti file lama)
```

**2. JavaScript:**
```
image-slot.js
    ↓
Copy ke project root (same folder as HTML)
```

**3. Assets folders:**
```
logos/ folder    ↓ Copy ke project root
uploads/ folder  ↓ Copy ke project root
```

---

## 📋 STRUKTUR SETELAH SETUP

Folder kamu harus terlihat:

```
porto-project/
├── Portfolio - Navy.html (109 KB)
├── image-slot.js (31 KB)
├── logos/
│   ├── msglow.png (size-lg)
│   ├── msglow.svg
│   ├── erha.png (size-lg)
│   ├── erha.svg
│   ├── thomascook.png (size-lg)
│   ├── ... (21 brands)
│   └── hwd.png
└── uploads/
    ├── Logo Portfolio/
    │   ├── Logo MS Glow.png
    │   ├── Logo ERHA.png
    │   └── ... (21 logos)
    ├── case-studies/
    │   └── ... (case study images)
    └── ... (other assets)
```

---

## ✅ STEP 3: Verify Setup

Open **Portfolio - Navy.html** di browser:

### Cek ini:

**Page 1 (Hero)**
- [ ] Photo Ika muncul (right side)
- [ ] Background images load

**Page 6 (Brands)**
- [ ] 3-column layout
- [ ] 21 logo brands muncul
- [ ] Scroll animation: left tilt + center up + right tilt

**Page 9 (Notable)**
- [ ] 5 notable brand logos
- [ ] Case study images

**All pages**
- [ ] No broken image icons (?)
- [ ] No console errors (F12)

---

## 🔍 TROUBLESHOOTING

### Logo tidak muncul

**Cause 1: image-slot.js tidak di-load**
- Check: `<script src="image-slot.js"></script>` ada di HTML?
- Check: File `image-slot.js` ada di project root?
- Fix: Copy `image-slot.js` dari bundle ke project root

**Cause 2: Folder path salah**
- HTML: `<image-slot src="logos/msglow.png">`
- File harus: `project/logos/msglow.png`
- Fix: Copy `logos/` folder ke project root

**Cause 3: Browser cache**
- Refresh: Ctrl+Shift+R (hard refresh)
- Clear cache: F12 → Application → Clear cache
- Reload page

### Foto Ika tidak muncul

**Cause: Upload folder path salah**
- Check: `uploads/` folder ada?
- Check: Foto Ika ada di `uploads/`?
- Fix: Copy `uploads/` folder ke project root

### Console error: "image-slot.js not found"

**Solution:**
1. Check file exists: `image-slot.js` di project root
2. Check path di HTML: `<script src="image-slot.js"></script>` (no subdirectory)
3. Hard refresh browser (Ctrl+Shift+R)

### Console error: "Cannot load image from logos/..."

**Solution:**
1. Check folder exists: `logos/` di project root
2. Check file exists: `logos/msglow.png` (case-sensitive!)
3. Verify path matches in HTML: `src="logos/msglow.png"`

---

## 📂 FILES TO COPY

| File/Folder | From | To | Size |
|-------------|------|----|----|
| HTML | `Portfolio_-_Navy_WITH_BRANDING_ANIMATION.html` | `Portfolio - Navy.html` | 109 KB |
| JS | `image-slot.js` | `./image-slot.js` | 31 KB |
| Folder | `logos/` | `./logos/` | 14 MB |
| Folder | `uploads/` | `./uploads/` | ~25 MB |

---

## 🎯 FINAL CHECKLIST

- [ ] File structure matches above
- [ ] `Portfolio - Navy.html` di project root
- [ ] `image-slot.js` di project root
- [ ] `logos/` folder di project root (21 .png files)
- [ ] `uploads/` folder di project root
- [ ] HTML has `<script src="image-slot.js"></script>`
- [ ] No errors in console (F12)
- [ ] Logo muncul di page 6
- [ ] Foto muncul di page 1
- [ ] Animation jalan saat scroll page 6

---

## 🎬 SAAT SUDAH SETUP

### Logo & Foto Akan Muncul di:

**Page 1 (Hero)**
- Foto Ika (right side, 4:5 aspect ratio)

**Page 6 (Brands)** - 3 COLUMNS:
- **Left column** (7 logos):
  - MS Glow, ERHA, Thomas Cook, J99 Corp
  - Roove, Sudo Brew, Mirai Group Japan
  
- **Center column** (7 logos):
  - NOAA, Sukkha Citta, Spice Mantra, Prastore
  - Privilege Creative, Aunty Jis, Paletas
  
- **Right column** (7 logos):
  - Sari Ater Hotel, Ada Fashion, DNY, Almona
  - Buti, Homewell, Homeware Depo

**Page 11 (Notable)**
- MS Glow, RTI/Roove, Sudo Brew, PTPN, Irfan Hakim (5 logos)

**Case Studies** (Page 6)
- Brand & case study images

---

## 🚀 AFTER SETUP

1. **Test di browser**: Open HTML file
2. **Scroll page 6**: Check animation works
3. **Deploy**: Push folder ke server/hosting
4. **Live**: Akses dari internet

---

## ⚠️ IMPORTANT

- **Case sensitive**: `logos/` bukan `Logos/`
- **Path relative**: Semua path `src="logos/..."` relative to HTML file
- **All assets together**: Folder HTML, JS, logos, uploads harus sama directory
- **No breaking changes**: All pages 1-14 tetap sama, hanya page 6 animated

---

## 📞 QUICK REFERENCE

**Struktur BENAR:**
```
project/
├── Portfolio - Navy.html
├── image-slot.js
├── logos/          ← semua .png files
└── uploads/        ← semua sub-folders
```

**Struktur SALAH:**
```
project/
├── Portfolio - Navy.html
└── assets/
    ├── image-slot.js  ❌ (harus di root)
    ├── logos/         ❌ (harus di root)
    └── uploads/       ❌ (harus di root)
```

---

**Setup selesai?** Sekarang logo & foto akan muncul! 🎉
