# 🚀 دليل النشر

## 🌐 النشر على Netlify

### 📋 المتطلبات
- حساب Netlify
- مستودع GitHub
- Node.js 18+

### 🔧 الخطوات

1. **رفع المشروع إلى GitHub**
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git remote add origin https://github.com/username/repo-name.git
   git push -u origin main
   ```

2. **ربط المستودع بـ Netlify**
   - اذهب إلى [netlify.com](https://netlify.com)
   - انقر على "New site from Git"
   - اختر GitHub وحدد المستودع

3. **إعدادات البناء**
   ```
   Build command: npm install --production=false && npm run build:client
   Publish directory: dist
   Node version: 18
   ```

4. **متغيرات البيئة (اختيارية)**
   ```
   NODE_VERSION: 18
   NODE_ENV: production
   ```

### ✅ النشر التلقائي
- كل تحديث في `main` branch سيتم نشره تلقائياً
- يمكنك تفعيل Preview Deploys للفروع الأخرى

## 🚀 النشر على Vercel

### 📋 المتطلبات
- حساب Vercel
- مستودع GitHub
- Node.js 18+

### 🔧 الخطوات

1. **رفع المشروع إلى GitHub** (نفس الخطوات أعلاه)

2. **ربط المستودع بـ Vercel**
   - اذهب إلى [vercel.com](https://vercel.com)
   - انقر على "New Project"
   - اختر GitHub وحدد المستودع

3. **إعدادات البناء**
   ```
   Framework Preset: Vite
   Build Command: npm run build:client
   Output Directory: dist
   Install Command: npm install
   ```

4. **متغيرات البيئة (اختيارية)**
   ```
   NODE_VERSION: 18
   NODE_ENV: production
   ```

### ✅ النشر التلقائي
- كل تحديث في `main` branch سيتم نشره تلقائياً
- Preview Deploys للفروع الأخرى

## ☁️ النشر على أي منصة أخرى

### 📋 المتطلبات العامة
- Node.js 18+
- npm أو yarn
- خادم ويب (Apache, Nginx, etc.)

### 🔧 الخطوات

1. **بناء المشروع**
   ```bash
   npm install
   npm run build:client
   ```

2. **رفع الملفات**
   - ارفع محتويات مجلد `dist` إلى مجلد `public_html` أو `www`
   - تأكد من وجود ملف `index.html` في المجلد الجذر

3. **إعداد الخادم**
   - تأكد من دعم SPA (Single Page Application)
   - أضف redirect rules لـ `/api/*` إذا كنت تستخدم backend منفصل

### 📁 هيكل الملفات المطلوب
```
public_html/
├── index.html
├── assets/
│   ├── css/
│   ├── js/
│   └── images/
└── favicon.ico
```

## 🔧 إعدادات إضافية

### 🌐 **CORS**
النظام يدعم CORS تلقائياً لجميع المصادر.

### 🔒 **HTTPS**
يُنصح بشدة باستخدام HTTPS في الإنتاج.

### 📱 **PWA**
النظام يدعم PWA تلقائياً.

### 🚀 **CDN**
يمكنك استخدام CDN لتحسين الأداء.

## 📊 مراقبة الأداء

### 📈 **Netlify Analytics**
- مراقبة الزيارات
- تحليل الأداء
- تقارير الأخطاء

### 📊 **Vercel Analytics**
- مراقبة الأداء
- تحليل المستخدمين
- تقارير مفصلة

### 🔍 **Google Analytics**
- إضافة Google Analytics
- تتبع الأحداث
- تقارير مخصصة

## 🚨 استكشاف الأخطاء

### ❌ **مشاكل شائعة**

1. **خطأ في البناء**
   - تأكد من Node.js 18+
   - تأكد من تثبيت التبعيات
   - راجع رسائل الخطأ

2. **مشاكل في النشر**
   - تأكد من صحة إعدادات البناء
   - تأكد من وجود ملف `index.html`
   - راجع logs النشر

3. **مشاكل في التشغيل**
   - تأكد من دعم SPA
   - تأكد من إعدادات الخادم
   - راجع console errors

### 🆘 **الحصول على المساعدة**

- **GitHub Issues**: للإبلاغ عن المشاكل
- **GitHub Discussions**: للمناقشات
- **Documentation**: للوثائق التفصيلية

## 🎯 أفضل الممارسات

### ✅ **قبل النشر**
- اختبر المشروع محلياً
- تأكد من عمل جميع الوظائف
- اختبر على أجهزة مختلفة

### ✅ **بعد النشر**
- اختبر جميع الصفحات
- اختبر الوظائف الأساسية
- راجع الأداء

### ✅ **الصيانة**
- راقب الأداء بانتظام
- احتفظ بنسخ احتياطية
- حدث النظام بانتظام

---

**🎉 النظام جاهز للنشر على أي منصة!**
