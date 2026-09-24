# المتجر النهائي — غرف نوم ومطابخ

هذه حزمة Full-stack مخصصة لـ Cloudflare Workers:
- واجهة متجر احترافية: `public/index.html`
- لوحة إدارة خاصة: `public/admin.html`
- API داخل Worker
- Cloudflare D1 للمنتجات
- Cloudflare R2 لصور المنتجات
- كلمة مرور الإدارة عبر Secret باسم `ADMIN_PASSWORD`

## النشر
1. أنشئ D1 باسم `ghoraf-store-db` ونفّذ `migrations/0001_init.sql`.
2. أنشئ R2 bucket باسم `ghoraf-store-images`.
3. ضع `database_id` الحقيقي في `wrangler.jsonc`.
4. أنشئ Secret باسم `ADMIN_PASSWORD`.
5. انشر Worker مع assets.
6. لوحة الإدارة: `/admin.html`

لا تضع كلمة المرور داخل الملفات.
قبل الإطلاق: استبدل صور الواجهة بصور المتجر النهائية، أضف رقم واتساب، اسم المتجر والشعار، ثم اربط نطاقًا مخصصًا.
