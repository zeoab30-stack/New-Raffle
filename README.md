# 🅩 Zeo Lottery / የዕጣ ሽልማት

## ይህ ምንድን ነው? / What is this?

ደንበኞችን የሚመዘግብ፣ ዕድል የሚያሰላ እና በቀጥታ በህዝብ ፊት ዕጣ የሚያወጣ ድህረ ገጽ መተግበሪያ ነው። በFirebase Firestore ላይ የተመሰረተ ስለሆነ በማንኛውም መሳሪያ (ስልክ/ኮምፒውተር) ላይ ተከፍቶ ውሂቡ ወዲያውኑ ይመሳሰላል።

A web app for registering raffle customers, calculating entries, and running a public live draw. Built on Firebase Firestore, so data instantly syncs across every device that opens the link.

---

## 🔗 ሊንክ / Live Link

```
https://<your-username>.github.io/<your-repo-name>/
```

*(ይህንን በራስህ GitHub Pages ሊንክ ተካው / replace with your actual GitHub Pages URL)*

---

## 🔒 የአስተዳዳሪ ቁጥጥር / Admin Control

**ማንም ደንበኛ ራሱን መመዝገብ ይችላል** (📝 ምዝገባ ገጽ) — PIN አያስፈልገውም።

**"🎉 ዕጣ" እና "⚙️ ማስተካከያ" ገጾች ግን በ PIN የተጠበቁ ናቸው።** ወደ እነዚህ ስትገባ የአስተዳዳሪ ኮድ ይጠየቃል።

- **ነባሪ PIN**: `1234`
- **ወዲያውኑ ይቀይሩት!** → ⚙️ ማስተካከያ ግቡ (የነባሪውን PIN ተጠቅመው) → "🔒 የአስተዳዳሪ ኮድ" ውስጥ አዲስ ኮድ ይጻፉ → "Save Settings" ይጫኑ
- PIN አንዴ ካስገቡ በኋላ በዚያው ብራውዘር/ትር ውስጥ እንደገና አይጠየቁም (እስከ ትር እስኪዘጉ ድረስ)
- ደንበኛ ከዝርዝር ውስጥ ማጥፋት (Delete) እንዲሁ PIN ይጠይቃል

⚠️ ይህ ጥበቃ ቀላል ደረጃ ነው (ለሱቅ/ጎራ ውስጣዊ አጠቃቀም የሚሆን) — ከፍተኛ ደህንነት ለሚያስፈልገው ውሂብ በቂ አይደለም። PIN ን ለታመኑ ሰራተኞች ብቻ አጋራ።

---

## 📋 አምስቱ ገጾች / The Five Tabs

| ገጽ | ማን ይጠቀማል | ምን ያደርጋል |
|---|---|---|
| 📝 ምዝገባ | ማንኛውም ሻጭ/ሠራተኛ | ደንበኛ ስም/ስልክ/ብር ያስገባል፣ ዕድል ራስ-ሰር ይሰላል |
| 📋 ዝርዝር | ሁሉም ማየት ይችላል | የተመዘገቡ ሁሉ ደንበኞች፣ መፈለጊያ፣ Excel export/import |
| 🎉 ዕጣ (PIN) | አስተዳዳሪ ብቻ | ቀጥታ ዕጣ ማውጫ ስነ-ስርዓት (ራፍል/ሎተሪ) |
| 🔄 እቁብ (PIN) | አስተዳዳሪ ብቻ | አባላት፣ ሳምንታዊ ዕጣ ማውጫ፣ ታሪክ |
| ⚙️ ማስተካከያ (PIN) | አስተዳዳሪ ብቻ | ተመን፣ ሽልማት፣ PIN ማስተካከል |

---

## 🔄 እቁብ / Equb (Rotating Savings)

የተለመደው የኢትዮጵያ እቁብ ስርዓት፦ አባላት በየሳምንቱ/ወሩ እኩል መጠን ያዋጣሉ፣ በዕጣ አንድ አባል ሙሉውን ገንዘብ ይወስዳል፣ አንዴ ካሸነፈ በዚያ ዙር ዳግም አይካተትም — ሁሉም እስኪያሸንፉ ድረስ።

Traditional Ethiopian rotating savings: members contribute an equal amount each round, one member is drawn at random to receive the full pot, and once a member wins they're excluded from further draws until everyone in the cycle has won.

**እንዴት ይሰራል / How it works:**
1. ⚙️ **የእቁብ ማስተካከያ** ውስጥ የመዋጮ መጠን እና ድግግሞሽ (ሳምንታዊ/ወርሃዊ) ያዘጋጁ
2. 👥 **አባላት** ውስጥ እያንዳንዱን አባል ስም/ስልክ ያስገቡ
3. በየሳምንቱ 🎲 **ዕጣ አውጣ** ይጫኑ — ገና ካላሸነፉ አባላት አንዱን በዘፈቀደ ይመርጣል
4. ሁሉም አባላት ካሸነፉ በኋላ **🔁 አዲስ ዙር ጀምር** ተጭነው እንደገና ይጀምራሉ (ሁሉም ዳግም ብቁ ይሆናሉ)
5. 📜 **ታሪክ** ውስጥ ያለፉ ዙሮች እና አሸናፊዎች ይመዘገባሉ

⚠️ ይህ የገንዘብ ስብስብ ስርዓት ራሱ ገንዘብ አይይዝም/አያስተላልፍም — አባላት ውጭ ጥሬ ገንዘብ ወይም telebirr ይዋጣሉ፣ መተግበሪያው የዕጣ ማውጫና መዝገብ ብቻ ነው።

---

## 🗓️ ከበዓል በፊት ማድረግ ያለብዎት / Before the Event

1. **⚙️ ማስተካከያ** ግቡ → የዕጣ ተመን (ለምሳሌ 500 ብር = 1 ዕድል) እና የሽልማት ስም/ፎቶ አረጋግጡ
   - **የሽልማት ፎቶ ለመጨመር**: ፎቶውን ወደ Google Drive፣ Imgur ወይም ሌላ ቦታ ስቀሉ → "Share" / "direct link" ያግኙ → ያንን ሊንክ በ"የፎቶ ሊንክ" ሳጥን ውስጥ ይለጥፉ
2. PIN ን ወደ የራስዎ ይቀይሩ
3. ሊንኩን ለሻጮች/ቅርንጫፎች አጋሩ፣ "Add to Home Screen" እንዲያደርጉ ንገሯቸው

## 🎉 በዕለቱ / On the Day

1. ደንበኞች ሲገዙ ሻጮች "📝 ምዝገባ" ውስጥ ይመዘግቧቸው
2. ለዕጣ ስነ-ስርዓት ጊዜ ሲደርስ "🎉 ዕጣ" ግቡ (PIN ያስፈልጋል)
3. ለ1ኛ/2ኛ/3ኛ "ዕጣ አውጣ" ተጫኑ — ውጤቱ ራስ-ሰር ይቀመጣል

## 🔄 ከበዓል በኋላ / After the Event

**ውሂብ ወደ Excel ማውረድ** (ለመዝገብ ማቆያ):
- 📋 ዝርዝር → "⬇️ ወደ Excel አውርድ" ተጫኑ

**ለቀጣይ ዝግጅት ውሂብ ማጽዳት** (አማራጭ):
- Firebase Console → Firestore Database → `raffle_participants` collection → ሁሉንም documents አጥፉ
- ወይም ይህን chat ውስጥ ጠይቁኝ፣ እረዳዎታለሁ

**ደህንነት ማጠናከር** (ውሂብ ካለቀ በኋላ፣ አማራጭ):
Firebase Console → Firestore Database → Rules ውስጥ ወደ ይህ ቀይሩ፦
```
allow read: if true;
allow write: if false;
```

---

## 🛠️ ቴክኒካዊ ዝርዝር / Technical Details

- **Frontend**: Single HTML file (`index.html`), vanilla JavaScript, no build step
- **Backend**: Firebase Firestore (real-time NoSQL database)
- **Hosting**: GitHub Pages (free, static hosting)
- **Firebase Project**: `new-raffle-c8912`
- **Firestore Collections**:
  - `raffle_participants` — one document per registered customer
  - `raffle/settings` — rate, prizes, PIN, privacy settings
  - `raffle/draw_results` — saved winner per prize tier
- **Free tier limits**: 50,000 reads/day, 20,000 writes/day — far more than a single promotion needs, no cost expected

## 📁 ፋይሎች / Files in this bundle

- `index.html` — ዋናው መተግበሪያ (upload this to GitHub)
- `manifest.json` — PWA installability config
- `sw.js` — offline caching (service worker)
- `icon-192.png`, `icon-512.png`, `icon-512-maskable.png` — Zeo Lottery app icons/logo
- `README.md` — this file

## 🔧 ወደፊት ማሻሻያ / Future Changes

ማንኛውም ለውጥ (አዲስ ገጽ፣ አዲስ ሽልማት አይነት፣ ዲዛይን ማስተካከያ) ካስፈለገ Claude chat ውስጥ ጠይቁ — `index.html` ተስተካክሎ ይላካል፣ በ GitHub ላይ ያለውን ፋይል በአዲሱ ብቻ ይተኩ (replace)።

---
*Zeo Lottery — reusable for any Zeo customer raffle or promotion.*
