# Yahya Tech — الموقع الرسمي

موقع شخصي ثابت (HTML/CSS/JS) ليحيى الحمزة، يعرض التطبيقات وروابط التحميل والخدمات ووسائل التواصل.

- الرابط المقترح: `https://ehea1973com-star.github.io/`
- لا يحتاج خادمًا أو قاعدة بيانات.
- يعمل على GitHub Pages مجانًا، ويمكن رفعه أيضًا إلى Cloudflare Pages أو Netlify.

## محتويات الموقع

```text
YahyaWebsite/
├── index.html
├── 404.html
├── README.md
├── robots.txt
├── sitemap.xml
├── .nojekyll
├── assets/
│   ├── style.css
│   ├── script.js
│   └── logo.svg
└── apps/
    ├── SmartPhoneDetective-v1.3.0.apk
    ├── NoorAlFajr-v1.3.1.apk
    ├── YahyaManager2-v2.0.0-release.apk
    └── SHA256SUMS.txt
```

## بصمات ملفات APK

```text
702d048bfb939d103c0054d651afdf84b0bdcd54ff988ac76461d0c0ae49f291  NoorAlFajr-v1.3.1.apk
a64a74907cfba15272fc2ee32a10644e151b1aef050afdff081f98b33b423527  SmartPhoneDetective-v1.3.0.apk
fc8aa09f62eb3e52753dace24aecc6dfab08b085e901ba1f68231efe31423629  YahyaManager2-v2.0.0-release.apk
```

## النشر على GitHub Pages

### الطريقة الموصى بها: موقع رئيسي باسم المستخدم

1. افتح GitHub وأنشئ مستودعًا جديدًا باسم:
   `ehea1973com-star.github.io`
2. اجعله **Public**.
3. ارفع **محتويات** مجلد `YahyaWebsite` إلى جذر المستودع، بحيث يكون `index.html` في الصفحة الرئيسية للمستودع، وليس داخل مجلد إضافي.
4. من المستودع: `Settings` ثم `Pages`.
5. اختر:
   - Source: `Deploy from a branch`
   - Branch: `main`
   - Folder: `/ (root)`
6. اضغط `Save` وانتظر من دقيقة إلى ثلاث دقائق.
7. سيصبح الموقع متاحًا على:
   `https://ehea1973com-star.github.io/`

### طريقة بديلة: موقع داخل مستودع موجود

إذا رفعت الموقع داخل مستودع مثل `Yahya-Editor-Android-2`:

- ضع الملفات في جذر المستودع أو في مجلد `docs/`.
- من `Settings > Pages` اختر الفرع والمجلد المناسب.
- سيكون الرابط:
  `https://ehea1973com-star.github.io/Yahya-Editor-Android-2/`

في هذه الحالة عدّل هذه القيم داخل `index.html`:

- `<link rel="canonical" href="...">`
- `<meta property="og:url" content="...">`
- `<meta property="og:image" content="...">`
- رابط `sitemap.xml`

## إضافة تطبيق جديد

1. أضف ملف APK إلى مجلد `apps/` باسم إنجليزي بدون مسافات، مثل:
   `MyApp-v1.0.0.apk`
2. افتح `index.html` وابحث عن:
   `<div class="apps-grid">`
3. انسخ بطاقة تطبيق كاملة من:
   `<article class="app-card reveal">` إلى `</article>`
4. عدّل:
   - أيقونة البطاقة: `icon-cyan` أو `icon-gold` أو `icon-violet` أو `icon-rose`
   - العنوان
   - رقم الإصدار
   - الوصف
   - `Android 5.0+` و`حجم الملف` واللغة
   - رابط التحميل: `href="apps/اسم-الملف.apk"`
   - رابط التفاصيل إن وجد
5. احفظ الملف وارفع التعديل إلى GitHub.

### ملاحظات مهمة للتحميل

- يمكن رفع APK صغير مباشرة إلى GitHub، لكن واجهة الويب تسمح عادةً بملفات حتى 25 MB تقريبًا.
- الحد الأقصى لملف واحد في GitHub هو 100 MB.
- للملفات الكبيرة استخدم **GitHub Releases**، ثم ضع رابط الإصدار المباشر في البطاقة.
- حجم موقع GitHub Pages المنشور يجب أن يبقى أقل من 1 GB.
- لا ترفع ملفات keystore أو كلمات المرور أو أي مفاتيح توقيع إلى الموقع أو المستودع.

## تحديث تطبيق موجود

1. ارفع الإصدار الجديد باسم واضح، مثل:
   `SmartPhoneDetective-v1.4.0.apk`
2. عدّل رقم الإصدار ورابط التحميل داخل `index.html`.
3. يمكنك الاحتفاظ بالملف القديم أو حذفه بعد التأكد من نجاح الإصدار الجديد.

## نسخة احتياطية ومرايا مجانية

- ارفع المجلد نفسه إلى **Cloudflare Pages** أو **Netlify** للحصول على رابط بديل.
- ملف ZIP الجاهز موجود في مجلد التنزيلات على الهاتف:
  `YahyaWebsite-GitHubPages.zip`
- يمكن استخدام الملف نفسه في Netlify Drop:
  `https://app.netlify.com/drop`

## ملاحظة عن الاستمرارية

GitHub Pages مجاني، لكنه مرتبط ببقاء حساب GitHub والمستودع. لا يوجد ضمان مطلق بأن أي خدمة مجانية لن تتوقف أو تتغير. للحفاظ على الموقع:

- احتفظ بنسخة من الملفات على جهازك.
- استخدم مرآة على Cloudflare Pages أو Netlify.
- يمكنك لاحقًا ربط نطاق خاص بك.

## الدومين الخاص (اختياري)

من `Settings > Pages > Custom domain` أضف النطاق، ثم اضبط سجلات DNS حسب تعليمات GitHub. بعد الربط فعّل `Enforce HTTPS`.

## معاينة محلية

افتح `index.html` مباشرة في المتصفح. الموقع لا يستخدم طلبات شبكة داخلية، لذلك تعمل روابط التطبيقات والتصميم من الملفات المحلية.
