# نشر تطبيق «عروض قطر» على GitHub + Vercel

> ارفع **محتويات هذا المجلد كله** (مش ملف واحد) — لأن التطبيق محتاج:
> index.html · manifest.json · sw.js · icon-192.png · icon-512.png · apple-touch-icon.png · favicon.png · vercel.json

## الطريقة الأسهل (Vercel مباشرة — بدون GitHub)
1. ادخل vercel.com وسجّل دخول.
2. اضغط **Add New… → Project**.
3. لو ظهر خيار رفع مجلد، اسحب مجلد التطبيق. أو استخدم خطوة GitHub تحت.
4. Framework Preset: **Other** · Build Command: (سيبه فاضي) · Output Directory: (سيبه فاضي / .)
5. **Deploy** → هياخد دقيقة ويديك رابط https زي: `https://qatar-deals.vercel.app`
6. افتح الرابط على موبايلك → هيظهر **تثبيت التطبيق** بالأيقونة العنابي.

## عبر GitHub (مرشّح للتحديثات المستقبلية)
1. أنشئ Repository جديد على github.com (مثلًا `qatar-deals`).
2. ارفع كل ملفات هذا المجلد داخل الـRepo (Add file → Upload files → اسحب كل الملفات → Commit).
3. ادخل vercel.com → **Add New → Project → Import** واختر الـRepo.
4. Framework: **Other** → **Deploy**.
5. أي تعديل مستقبلي ترفعه على GitHub، Vercel ينشره تلقائيًا.

## ملاحظات
- لازم يكون https (Vercel بيوفّرها تلقائيًا) عشان التثبيت والـ Service Worker يشتغلوا.
- لو غيّرت الملفات لاحقًا، التطبيق المثبّت بيتحدّث تلقائيًا (رقم الكاش في sw.js بيتغيّر).
- البيانات والصور حاليًا مؤقتة في المتصفح (Prototype). للتخزين الدائم لكل المستخدمين، طبّق دليل Firebase المرفق.
