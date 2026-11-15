# 🏢 تنزيلات السيرفر الرئيسي — منظومة صولة للمؤسسات

**SPOS Solah Enterprise Server** — سيرفر الفرع كاملاً في **مثبّت أحادي الملف**:
قاعدة PostgreSQL 17 + لوحة إدارة عربية + تطبيق هاتف + نفق عام + محطات بلا حد.

**الترخيص يتفعّل تلقائياً** مع سيرفر تراخيص صولة (license.spos.ly) — **لا مفتاح ولا وسيط إطلاقاً**، وبعد الدفع يتحول إلى **دائم للأبد** تلقائياً.

> 🌐 **صفحة التحميل للزبائن:** https://spos-systems.github.io/downloads-pos-server-platform/

---

## التركيب — أمر واحد على أي جهاز Ubuntu/Debian نظيف

```bash
curl -fsSL https://github.com/spos-systems/downloads-pos-server-platform/releases/latest/download/SPOS-Solah-Enterprise-Setup.sh -o spos-setup.sh
sudo bash spos-setup.sh
```

- لا git ولا فلاشة ولا ملفات إضافية — **كل شيء داخل الملف الواحد**.
- المثبّت يثبّت Docker إن غاب، يولّد كلمات السر، يشغّل كل شيء، ثم يطبع **عنوان اللوحة وكلمة سرها**.
- **التفعيل التلقائي:** افتح اللوحة ← الترخيص ← اسم صاحب المحل ورقم هاتفه ← **«تفعيل تلقائي»** —
  يعمل الفرع فوراً، وبعد إتمام الدفع يتحول الترخيص إلى دائم تلقائياً مع المزامنة.

## خيارات المثبّت

| الخيار | الوظيفة |
| --- | --- |
| `--dir PATH` | مجلد التثبيت (الافتراضي `/opt/spos`) |
| `--port N` | منفذ اللوحة (الافتراضي `5150`) |
| `--no-tunnel` | تعطيل النفق العام (مفعّل فوراً افتراضياً) |

## الروابط الدائمة (تتبع أحدث إصدار دائماً)

| الحزمة | الرابط |
| --- | --- |
| المثبّت أحادي الملف ⭐ | https://github.com/spos-systems/downloads-pos-server-platform/releases/latest/download/SPOS-Solah-Enterprise-Setup.sh |
| حزمة المصدر (للوكيل) | https://github.com/spos-systems/downloads-pos-server-platform/releases/latest/download/SPOS-Solah-Enterprise-Server.zip |
| البصمات | https://github.com/spos-systems/downloads-pos-server-platform/releases/latest/download/SHA256SUMS.txt |

## v1.0.2 — أحدث إصدار

| الحزمة | الحجم | الرابط |
| --- | --- | --- |
| المثبّت أحادي الملف | 118 KB | https://github.com/spos-systems/downloads-pos-server-platform/releases/download/v1.0.2/SPOS-Solah-Enterprise-Setup-v1.0.2.sh |
| حزمة المصدر | 118 KB | https://github.com/spos-systems/downloads-pos-server-platform/releases/download/v1.0.2/SPOS-Solah-Enterprise-Server-v1.0.2.zip |
| البصمات | — | https://github.com/spos-systems/downloads-pos-server-platform/releases/download/v1.0.2/SHA256SUMS.txt |

## التفعيل التلقائي — كيف يعمل؟

- عند الضغط على «تفعيل تلقائي» يتصل السيرفر بخادم تراخيص صولة **بنفس بروتوكول بقية منتجات صولة**
  فيُسجَّل ويُصدر ترخيصه الموقّع فوراً — بلا أي مفتاح.
- يبدأ الفرع بالعمل في الحال، وبعد إتمام الدفع يحوّل المالك الترخيص إلى **دائم** من لوحة
  خادم التراخيص — والتحويل يصل السيرفر تلقائياً مع المزامنة اليومية.
- انقطاع الإنترنت لا يوقف المحل أبداً: التحقق محلي بتوقيع RSA مضمّن.

## المتطلبات

- أي جهاز **Ubuntu/Debian** نظيف (20.04 أو أحدث) — يصلح جهاز قديم دون شاشة.
- معالج i3+ وذاكرة 4GB تكفي لفرع كامل — **القرص هو المهم: SSD**.
- الإنترنت مطلوب وقت التركيب فقط — التشغيل بعدها **محلي بالكامل** داخل المحل.

## محطات الكاشير (ويندوز / لينكس)

من مستودع المحطات العام: **https://github.com/spos-systems/downloads-pos-pc-platform**

بعد تركيب السيرفر: من المحطة ← الإعدادات ← **قاعدة البيانات والشبكة** ← «وضع الجهاز الفرعي» ←
يظهر السيرفر في **الاكتشاف التلقائي** ← «طلب اقتران» ← اعتماده من **لوحة السيرفر الرئيسي** —
المحطة تتبنى الترخيص تلقائياً — بلا أي ترخيص إضافي مهما كثرت المحطات.

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

بصمات v1.0.2:

```text
1231fd048c5b4e0aa49115209d100b2189957cbffa2b1b82d0fcef42fecb196d  SPOS-Solah-Enterprise-Setup-v1.0.2.sh
25289d3e73cdd5b9de968c7835b1a40ee3417205d7524d96e2b7a5fc9d5adb2c  SPOS-Solah-Enterprise-Server-v1.0.2.zip
```

## الدعم الفني

📞 0935535606 • واتساب: +218 93 553 5606 • 🌐 spos.ly
