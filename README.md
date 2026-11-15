# 🏢 تنزيلات السيرفر الرئيسي — منظومة صولة للمؤسسات

**SPOS Solah Enterprise Server** — سيرفر الفرع كاملاً في **مثبّت أحادي الملف**:
قاعدة PostgreSQL 17 + لوحة إدارة عربية + تطبيق هاتف + نفق عام + محطات بلا حد —
ترخيص مؤسسات واحد يُشترى **مرة واحدة ويعمل للأبد** (بلا اشتراك ولا مقاعد).

> 🌐 **صفحة التحميل للزبائن:** https://spos-systems.github.io/downloads-pos-server-platform/

---

## التركيب — أمر واحد على أي جهاز Ubuntu/Debian نظيف

```bash
curl -fsSL https://github.com/spos-systems/downloads-pos-server-platform/releases/latest/download/SPOS-Solah-Enterprise-Setup.sh -o spos-setup.sh
sudo bash spos-setup.sh --license SPOS-ENTERPRISE-XXXXXXXX
```

- لا git ولا فلاشة ولا ملفات إضافية — **كل شيء داخل الملف الواحد** (الحزمة كاملة مضمّنة فيه).
- المثبّت يثبّت Docker إن غاب، يولّد كلمات السر، يشغّل كل شيء، يفعّل الترخيص تلقائياً بالمفتاح،
  ثم يطبع **عنوان اللوحة وكلمة سرها**.
- بلا مفتاح الآن؟ شغّل التركيب بدون `--license` ثم فعّل المفتاح من اللوحة ← **الترخيص**.

## خيارات المثبّت

| الخيار | الوظيفة |
| --- | --- |
| `--license KEY` | تفعيل ترخيص المؤسسات تلقائياً بعد التركيب |
| `--dir PATH` | مجلد التثبيت (الافتراضي `/opt/spos`) |
| `--port N` | منفذ اللوحة (الافتراضي `5150`) |
| `--no-tunnel` | تعطيل النفق العام (مفعّل فوراً افتراضياً) |

## الروابط الدائمة (تتبع أحدث إصدار دائماً)

| الحزمة | الرابط |
| --- | --- |
| المثبّت أحادي الملف ⭐ | https://github.com/spos-systems/downloads-pos-server-platform/releases/latest/download/SPOS-Solah-Enterprise-Setup.sh |
| حزمة المصدر (للوكيل) | https://github.com/spos-systems/downloads-pos-server-platform/releases/latest/download/SPOS-Solah-Enterprise-Server.zip |
| البصمات | https://github.com/spos-systems/downloads-pos-server-platform/releases/latest/download/SHA256SUMS.txt |

## v1.0.1 — الإصدار الأول (أحدث)

| الحزمة | الحجم | الرابط |
| --- | --- | --- |
| المثبّت أحادي الملف | 117 KB | https://github.com/spos-systems/downloads-pos-server-platform/releases/download/v1.0.1/SPOS-Solah-Enterprise-Setup-v1.0.1.sh |
| حزمة المصدر | 115 KB | https://github.com/spos-systems/downloads-pos-server-platform/releases/download/v1.0.1/SPOS-Solah-Enterprise-Server-v1.0.1.zip |
| البصمات | — | https://github.com/spos-systems/downloads-pos-server-platform/releases/download/v1.0.1/SHA256SUMS.txt |

## المتطلبات

- أي جهاز **Ubuntu/Debian** نظيف (20.04 أو أحدث) — يصلح جهاز قديم دون شاشة.
- معالج i3+ وذاكرة 4GB تكفي لفرع كامل — **القرص هو المهم: SSD**.
- الإنترنت مطلوب وقت التركيب فقط — التشغيل بعدها **محلي بالكامل** داخل المحل.

## محطات الكاشير (ويندوز / لينكس)

من مستودع المحطات العام: **https://github.com/spos-systems/downloads-pos-pc-platform**

بعد تركيب السيرفر: من المحطة ← الإعدادات ← **قاعدة البيانات والشبكة** ← «وضع الجهاز الفرعي» ←
يظهر السيرفر في **الاكتشاف التلقائي** ← «طلب اقتران» ← اعتماده من **لوحة السيرفر الرئيسي** ←
المحطة تتبنى **ترخيص المؤسسات الدائم** تلقائياً — بلا أي ترخيص إضافي مهما كثرت المحطات.

## الترقية

أعد تشغيل **نفس الملف** على نفس الجهاز:

```bash
sudo bash spos-setup.sh
```

نسخة احتياطية تلقائية للقاعدة قبل الترقية، وكل البيانات محفوظة.

## التحقق من الحزم

```bash
sha256sum -c SHA256SUMS.txt
```

بصمات v1.0.1:

```text
d6c647f144c9ce4baabf4d4ca7bd0d9fb662e1acc08b3b91576d1cd185a42a19  SPOS-Solah-Enterprise-Setup-v1.0.1.sh
bac946c1f7d426a527a2322cebaa84eab7cb167b66980cdf31f45bff02943669  SPOS-Solah-Enterprise-Server-v1.0.1.zip
```

## الدعم الفني

📞 0935535606 • واتساب: +218 93 553 5606 • 🌐 spos.ly
