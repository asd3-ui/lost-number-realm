# 🏰 مملكة الأرقام المفقودة — The Lost Number Realm

لعبة تعليمية تفاعلية باللغة العربية للأطفال، مبنية بواجهة HTML/CSS/JavaScript وتُغلّف كتطبيق Android باستخدام Capacitor.

## بناء APK تلقائيًا

يبدأ GitHub Actions تلقائيًا عند الدفع إلى الفرع `main` أو `master`، ويمكن تشغيله يدويًا:

1. افتح تبويب [Actions](../../actions/workflows/build_apk.yml).
2. اختر **Build Android APK**.
3. اضغط **Run workflow** عند الحاجة.
4. افتح آخر تشغيل وانتظر حتى تصبح حالته **Success**.
5. من قسم **Artifacts** نزّل `LostNumberRealm-APK`، ثم استخرج الملف `app-debug.apk`.

ينتج البناء ملف **Debug APK قابلًا للتثبيت للاختبار**. هذا الملف ليس إصدارًا موقّعًا للنشر على Google Play؛ النشر العام يتطلب إعداد توقيع إصدار Release.

## الملفات الأساسية

- `index.html`: واجهة اللعبة ومنطق الألعاب.
- `package.json`: تبعيات Capacitor وأمر تجهيز ملفات الويب.
- `capacitor.config.json`: معرّف التطبيق وإعداداته.
- `.github/workflows/build_apk.yml`: بناء APK ورفعه كـ Artifact.

## البناء محليًا

يتطلب Node.js 20 وJava 17 وAndroid SDK:

```bash
npm install
npm run build
npx cap add android
npx cap sync android
cd android
./gradlew assembleDebug
```

يوجد التطبيق الناتج في `android/app/build/outputs/apk/debug/app-debug.apk`.
