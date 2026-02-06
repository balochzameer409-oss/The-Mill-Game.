# 🎮 The Mill Game (نو گوٹی گیم)

<div dir="rtl">

## 📌 تعارف

یہ ایک روایتی **نو گوٹی (Mill Game)** کا جدید ویب ورژن ہے جو **Firebase** اور **WebRTC** ٹیکنالوجی استعمال کرتے ہوئے بنایا گیا ہے۔ اس گیم میں آپ دوستوں کے ساتھ آن لائن کھیل سکتے ہیں اور وائس چیٹ کے ذریعے بات بھی کر سکتے ہیں۔

## ⚠️ اہم ڈس کلیمر (DISCLAIMER)

### 🔒 ذاتی استعمال کے لیے

یہ پروجیکٹ میری **ذاتی استعمال** کے لیے بنایا گیا ہے۔ اس کوڈ میں موجود Firebase کنفیگریشن اور دیگر API keys میری پرسنل ہیں۔

### ⚠️ آپ کے لیے ہدایات

اگر آپ یہ گیم استعمال کرنا چاہتے ہیں تو:

1. **اپنا Firebase پروجیکٹ بنائیں** - https://firebase.google.com
2. **اپنی Firebase کنفیگریشن** کوڈ میں تبدیل کریں
3. **سیکیورٹی کوڈ ہٹا دیں** یا اپنے مطابق تبدیل کریں
4. **TURN/STUN Servers** اپنے استعمال کریں (voice chat کے لیے)

### 🚫 ممنوعات

- ❌ میرے Firebase credentials استعمال نہ کریں
- ❌ کوڈ میں موجود API keys کا غلط استعمال نہ کریں  
- ❌ کسی بھی قسم کی **غیر مجاز** یا **غیر قانونی** سرگرمیوں کے لیے استعمال نہ کریں
- ❌ بغیر اجازت تجارتی مقاصد کے لیے استعمال نہ کریں

### ✅ جائز استعمال

آپ یہ کوڈ **سیکھنے**، **تجربے** اور **اپنے ذاتی پروجیکٹس** کے لیے استعمال کر سکتے ہیں، بشرطیکہ:
- اپنی Firebase/API کنفیگریشن استعمال کریں
- کوڈ کو اپنی ضروریات کے مطابق customize کریں
- اصل سورس کو credit دیں

---

## 🎯 خصوصیات

### ✨ بنیادی فیچرز
- 🎮 **روایتی Mill Game** - کلاسک نو گوٹی کا کھیل
- 👥 **دو موڈ**: سنگل پلیئر (AI کے خلاف) اور آن لائن ملٹی پلیئر
- 🎨 **خوبصورت UI/UX** - جدید اور پرکشش ڈیزائن
- 📱 **موبائل فرینڈلی** - ہر ڈیوائس پر بہترین تجربہ

### 🌐 آن لائن فیچرز
- 🔥 **Firebase Realtime Database** - حقیقی وقت میں ڈیٹا سنک
- 🎲 **رینڈم گیم آئی ڈی** - آسان گیم شئیرنگ
- 👤 **کسٹم نام** - اپنی پسند کا نام استعمال کریں
- 📊 **گیم سٹیٹس** - لائیو اپڈیٹس

### 🎤 وائس چیٹ
- 📞 **WebRTC Voice Chat** - حقیقی وقت میں آواز
- 🎧 **کرسٹل کلیئر آڈیو** - HD audio quality
- 🔇 **Mute/Unmute** - مائیکروفون کنٹرول
- 📴 **آسان کال مینجمنٹ** - ایک کلک میں شروع/بند

### 🎵 دیگر خصوصیات
- 🔊 **ساؤنڈ ایفیکٹس** - ہر move پر آواز
- 📈 **Game History** - اپنی کارکردگی ٹریک کریں
- 💾 **LocalStorage** - ڈیٹا محفوظ رہتا ہے
- 🏆 **Win/Loss Counter** - مکمل اعدادوشمار

---

## 🛠️ ٹیکنالوجی اسٹیک

### Frontend
- HTML5
- CSS3 (Custom Styling)
- JavaScript (ES6+)
- Font Awesome Icons

### Backend Services
- Firebase Realtime Database
- Firebase Authentication (optional)

### WebRTC
- Peer-to-Peer Connection
- ICE/STUN/TURN Servers
- Real-time Audio Streaming

---

## 📥 انسٹالیشن اور سیٹ اپ

### 1️⃣ ریپوزٹری کلون کریں
```bash
git clone https://github.com/YOUR-USERNAME/mill-game.git
cd mill-game
```

### 2️⃣ Firebase سیٹ اپ

#### a) Firebase Console میں نیا پروجیکٹ بنائیں
1. https://console.firebase.google.com پر جائیں
2. "Add Project" پر کلک کریں
3. پروجیکٹ کا نام دیں

#### b) Realtime Database Enable کریں
1. "Build" > "Realtime Database" پر جائیں
2. "Create Database" پر کلک کریں
3. Test mode میں شروع کریں (بعد میں rules تبدیل کریں)

#### c) Firebase Config حاصل کریں
1. Project Settings > General میں جائیں
2. "Your apps" سیکشن میں Web App شامل کریں
3. Config code کاپی کریں

### 3️⃣ کوڈ میں تبدیلیاں

HTML فائل میں Firebase config تبدیل کریں:

```javascript
// ⚠️ یہ حصہ تلاش کریں اور اپنی values ڈالیں
const firebaseConfig = {
    apiKey: "آپ_کی_API_KEY",
    authDomain: "آپ_کا_AUTH_DOMAIN",
    databaseURL: "آپ_کا_DATABASE_URL",
    projectId: "آپ_کا_PROJECT_ID",
    storageBucket: "آپ_کا_STORAGE_BUCKET",
    messagingSenderId: "آپ_کا_MESSAGING_SENDER_ID",
    appId: "آپ_کی_APP_ID"
};
```

### 4️⃣ Security کوڈ ہٹانا (اختیاری)

اگر آپ کو سیکیورٹی restrictions کی ضرورت نہیں، تو یہ حصہ ہٹا دیں یا تبدیل کریں:

```javascript
// Lines 3131-3247 میں موجود SECURITY_CONFIG
// اسے اپنے domain کے مطابق تبدیل کریں یا ہٹا دیں
const SECURITY_CONFIG = {
    allowedDomains: [
        'آپ_کی_domain.com',
        'localhost'
    ],
    // ... باقی کنفیگ
};
```

### 5️⃣ لوکل ٹیسٹ

```bash
# کوئی بھی local server چلائیں
python -m http.server 8000
# یا
npx serve
```

Browser میں `http://localhost:8000` کھولیں

---

## 🎮 کیسے کھیلیں

### 🏠 سنگل پلیئر (AI کے خلاف)
1. "تنہا کھیلیں" پر کلک کریں
2. اپنا نام لکھیں
3. شروع ہوجائیں!

### 🌐 آن لائن ملٹی پلیئر
1. "آن لائن کھیلیں" پر کلک کریں
2. اپنا نام لکھیں
3. دو آپشن:
   - **نیا گیم**: Game ID ملے گی، دوست کو شئیر کریں
   - **Join کریں**: دوست کی Game ID درج کریں

### 🎤 وائس چیٹ استعمال
1. آن لائن گیم شروع کریں
2. نیچے دائیں کونے میں 🎧 آئیکن پر کلک کریں
3. Voice panel کھل جائے گا
4. 📞 سبز بٹن سے کال شروع/بند کریں
5. 🎤 بٹن سے مائیک on/off کریں

---

## 🎯 گیم کے قوانین

### 🎲 کھیل کے تین مراحل

#### مرحلہ 1: گوٹیاں رکھنا
- ہر کھلاڑی کے پاس 9 گوٹیاں ہیں
- باری باری گوٹیاں بورڈ پر رکھیں
- 3 گوٹیاں ایک لائن میں = "Mill" بنتی ہے

#### مرحلہ 2: گوٹیاں چلنا
- سب گوٹیاں رکھنے کے بعد
- پڑوسی خالی جگہ پر move کریں
- Mill بنائیں اور مخالف کی گوٹی اٹھائیں

#### مرحلہ 3: اڑنا (Flying)
- جب صرف 3 گوٹیاں بچیں
- کسی بھی خالی جگہ پر جا سکتے ہیں

### 🏆 جیتنے کی شرط
مخالف کے پاس:
- صرف 2 گوٹیاں بچیں
- یا کوئی valid move نہ ہو

---

## 🔧 Troubleshooting

### Firebase کنکشن کی خرابی
```
❌ مسئلہ: "Firebase not connected"
✅ حل: 
- Firebase config دوبارہ چیک کریں
- Database rules دیکھیں
- Internet connection check کریں
```

### Voice Chat کام نہیں کر رہی
```
❌ مسئلہ: آواز سنائی نہیں دیتی
✅ حل:
- Browser میں microphone permission دیں
- HTTPS استعمال کریں (HTTP پر WebRTC کام نہیں کرتا)
- Firewall/VPN چیک کریں
```

### Domain Security Error
```
❌ مسئلہ: "Unauthorized Domain"
✅ حل:
- SECURITY_CONFIG میں اپنی domain شامل کریں
- یا پورا security code ہٹا دیں (lines 3131-3247)
```

---

## 📚 فولڈر اسٹرکچر

```
mill-game/
│
├── index.html          # مین گیم فائل (تمام code یہاں)
├── README.md           # یہ فائل
├── LICENSE             # لائسنس فائل
│
└── assets/             # (اختیاری) اگر الگ files بنانا چاہیں
    ├── css/
    ├── js/
    └── sounds/
```

---

## 🤝 تعاون (Contributing)

اگر آپ اس پروجیکٹ میں بہتری لانا چاہتے ہیں:

1. Repository کو Fork کریں
2. نئی Branch بنائیں (`git checkout -b feature/AmazingFeature`)
3. تبدیلیاں Commit کریں (`git commit -m 'Add some feature'`)
4. Branch Push کریں (`git push origin feature/AmazingFeature`)
5. Pull Request کھولیں

---

## 📄 لائسنس

یہ پروجیکٹ **MIT License** کے تحت ہے - تفصیلات کے لیے [LICENSE](LICENSE) فائل دیکھیں۔

### ⚖️ شرائط:
- ✅ ذاتی استعمال کی اجازت ہے
- ✅ تبدیلی کی اجازت ہے
- ✅ تقسیم کی اجازت ہے
- ❌ میرے credentials استعمال نہ کریں
- ❌ غیر قانونی کام کے لیے استعمال نہ کریں

---

## 👨‍💻 بنانے والا

**Baloch Zameer**
- GitHub: [@balochzameer409](https://github.com/balochzameer409-oss)
- یہ پروجیکٹ محبت سے 🇵🇰 پاکستان میں بنایا گیا

---

## 🙏 شکریہ

اس پروجیکٹ میں استعمال شدہ ٹیکنالوجیز:
- [Firebase](https://firebase.google.com/) - Backend services
- [WebRTC](https://webrtc.org/) - Real-time communication
- [Font Awesome](https://fontawesome.com/) - Icons
- اور تمام open source libraries

---

## 📞 رابطہ اور سپورٹ

اگر آپ کو کوئی مسئلہ درپیش ہو یا سوال ہو:

1. **GitHub Issues** میں رپورٹ کریں
2. **Pull Request** بھیجیں
3. **Discussion** شروع کریں

---

## 🔮 مستقبل کی منصوبہ بندی

- [ ] Tournament mode شامل کریں
- [ ] Leaderboard system بنائیں
- [ ] مزید themes شامل کریں
- [ ] Mobile app version (React Native)
- [ ] AI difficulty levels
- [ ] Replay system
- [ ] Chat messages (text)

---

## ⚡ فوری شروعات

```bash
# 1. Clone
git clone https://github.com/YOUR-USERNAME/mill-game.git

# 2. اپنی Firebase config ڈالیں
nano index.html  # یا کوئی editor

# 3. Local server چلائیں
python -m http.server 8000

# 4. Browser میں کھولیں
http://localhost:8000
```

---

<div align="center">

### 🎮 مزے کریں اور Fair Play کریں! 🎮

**اگر پسند آئے تو ⭐ Star دینا نہ بھولیں!**

---

**Made with ❤️ in Pakistan 🇵🇰**

</div>

</div>
```
