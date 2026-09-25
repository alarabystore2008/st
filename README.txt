متجر العربي - نسخة Firebase المؤمّنة

الملفات:
- index.html: واجهة المتجر، تقرأ المنتجات والتقييمات من Firestore.
- admin.html: لوحة الإدارة، الدخول فيها يتم عبر Firebase Authentication (Email/Password).
- firebase-config.js: إعدادات Firebase الخاصة بتطبيق الويب.
- firestore.rules: قواعد أمان Firestore.

ما تم تغييره:
1) أزيلت كلمة المرور القديمة 123 من admin.html.
2) لوحة الإدارة تستخدم Firebase Authentication.
3) المنتجات يمكن للجميع قراءتها، لكن إضافة/تعديل/حذف المنتجات تتطلب مستخدمًا مسجّلًا في Firebase Authentication.
4) التقييمات ما زالت قابلة للقراءة والإضافة للزوار كما في التصميم السابق.
5) لم تعد جلسة الإدارة تعتمد على localStorage.

خطوات النشر:
1) في Firebase Authentication فعّل Email/Password وأنشئ مستخدم المدير.
2) ارفع هذه الملفات إلى GitHub Pages.
3) في Firebase Console > Firestore > Rules، انسخ محتوى firestore.rules ثم انشر القواعد.
4) افتح admin.html وسجّل دخول المدير بالبريد الإلكتروني وكلمة المرور اللذين أنشأتهما في Firebase.
