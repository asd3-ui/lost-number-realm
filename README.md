# 🏰 مملكة الأرقام المفقودة — The Lost Number Realm

لعبة تعليمية تفاعلية باللغة العربية للأطفال، مبنية كصفحة HTML وتُغلّف كتطبيق Android باستخدام Apache Cordova.

## بناء APK تلقائيًا

يعمل GitHub Actions عند الدفع إلى الفرع `main` أو `master`، ويمكن تشغيله يدويًا:

1. افتح تبويب **Actions** في المستودع.
2. اختر **Build Android APK**.
3. اضغط **Run workflow** عند الحاجة.
4. بعد نجاح البناء، افتح تشغيل workflow وانزل إلى **Artifacts**.
5. نزّل `LostNumberRealm-APK` واستخرج ملف APK.

> ملف APK الناتج غير موقّع للنشر على Google Play؛ يمكن استخدامه للاختبار، أما النشر العام فيتطلب إعداد توقيع Android.

## ملفات المشروع

- `index.html`: واجهة اللعبة ومنطقها.
- `.github/workflows/build_apk.yml`: بناء Android ورفع APK كـ Artifact.

يتطلب الـ workflow وجود `index.html` في جذر المستودع، ويستخدم Java 17 وAndroid SDK وCordova.
