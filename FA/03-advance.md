# سوالات پیشرفته جاوا اسکریپت

## مبانی جاوا اسکریپت

### 1. موتور جاوا اسکریپت چیه؟
> موتور جاوا اسکریپت برنامه‌ایه که کدهای جاوا اسکریپت رو اجرا می‌کنه. مثلاً V8 گوگل، SpiderMonkey موزیلا و Chakra مایکروسافت از این دسته هستن.

### 2. مفهوم context اجرای کد و call stack در جاوا اسکریپت رو توضیح بده.
> برای توضیح، context اجرای کد محیطیه که کد جاوا اسکریپت در اون اجرا میشه. این محیط شامل this binding، متغیرها، اشیاء و توابع میشه. call stack هم یه ساختار داده‌ای به نام stack هست که پیگیری فراخوانی‌های توابع رو انجام میده و به موتور جاوا اسکریپت کمک میکنه تا بدونه بعد از اجرای هر تابع باید به کجا برگرده.

### 3. حلقه رویداد (event loop) چیه و چطور کار می‌کنه؟
> حلقه رویداد اجازه میده جاوا اسکریپت عملیات غیرمسدودکننده (non-blocking) انجام بده با این که وظایف رو هر وقت که ممکن باشه به هسته سیستم (system kernel) واگذار کنه. این حلقه به‌طور مداوم call stack و callback queue رو بررسی می‌کنه و اگر call stack خالی باشه، اولین وظیفه از صف (queue) رو به call stack اضافه می‌کنه.

## توابع پیشرفته و closures

### 4. مفهوم توابع مرتبه‌بالا (higher-order functions) رو توضیح بده و یک مثال بزن.
> توابع مرتبه‌بالا توابعی هستن که می‌تونن توابع دیگه رو به عنوان آرگومان بپذیرن یا توابع رو به عنوان نتیجه برگردونن. مثال:
> ```javascript
> function higherOrder(fn) {
>   // یه تابع جدید برمی‌گردونه که مقداری می‌گیره و تابع ورودی رو روی اون اعمال می‌کنه
>   return function(value) {
>     return fn(value);
>   };
> }
> // تابعی به نام 'double' ایجاد کن که ورودی خود رو با استفاده از تابع higherOrder دو برابر کنه
> const double = higherOrder((x) => x * 2);
> console.log(double(5)); // 10
> ```


### 5. تولیدکننده‌ها (generators) چی هستن و چطور ازشون استفاده می‌کنیم؟
> تولیدکننده‌ها توابعی هستن که می‌تونن در وسط اجرا متوقف بشن و بعداً از همون جا ادامه پیدا کنن. برای تعریف تولیدکننده از سینتکس `function*` و کلیدواژه `yield` استفاده می‌کنیم. مثال:
> ```javascript
> function* generator() {
>   yield 1; // توقف کن و 1 رو برگردون
>   yield 2; // توقف کن و 2 رو برگردون
>   yield 3; // توقف کن و 3 رو برگردون
> }
> const gen = generator();
> console.log(gen.next().value); // 1
> console.log(gen.next().value); // 2
> console.log(gen.next().value); // 3
> ```

### 6. مفهوم memoization در جاوا اسکریپت رو توضیح بده.
> مفهوم memoization یه تکنیک بهینه‌سازی هست که برای سریع‌تر کردن فراخوانی‌های توابع استفاده میشه. این تکنیک با کش کردن نتایج فراخوانی‌های پرهزینه و برگشت دادن نتیجه کش شده زمانی که ورودی‌های مشابه دوباره اتفاق میفته، عمل می‌کنه.

## اشیاء و پروتوتایپ‌ها

### 7. تفاوت بین `Object.create()` و `Object.assign()` چیه؟
> برای توضیح، `Object.create()` یه شیء جدید با پروتوتایپ و ویژگی‌های مشخص‌شده ایجاد می‌کنه، در حالی که `Object.assign()` ویژگی‌ها رو از یک یا چند شیء منبع به یک شیء هدف کپی می‌کنه.

### 8. شیء `Proxy` چیه و چطور ازش استفاده می‌کنیم؟
> شیء `Proxy` برای تعریف رفتار سفارشی برای عملیات‌های بنیادی (مثل جستجوی ویژگی، انتساب، شمارش و فراخوانی تابع) استفاده میشه. مثال:
> ```javascript
> const target = {};
> const handler = {
>   get: function(obj, prop) {
>     // اگر ویژگی وجود داشته باشه مقدار اون رو برگردون، در غیر این صورت 42 رو برگردون
>     return prop in obj ? obj[prop] : 42;
>   }
> };
> const proxy = new Proxy(target, handler);
> console.log(proxy.answer); // 42
> ```

## ناهمزمانی و بهینه‌سازی عملکرد

### 9. تفاوت بین microtasks و macrotasks در حلقه رویداد چیه؟
> برای توضیح، microtasks کارهایی هستن که بعد از پایان عملیات فعلی اما قبل از رندرینگ اجرا میشن. مثال‌ها شامل promises و callback های `MutationObserver` هستن. از طرف دیگه، macrotasks کارهایی هستن که بعد از رندرینگ اجرا میشن. مثال‌ها شامل `setTimeout`، `setInterval` و وظایف I/O هستن.

### 10. وب ورکرا (Web Workers) چی هستن و چطور عملکرد رو بهبود میدن؟
> وب ورکرا اجازه میدن که کد جاوا اسکریپت رو در پس‌زمینه و در یک نخ جدا از نخ اصلی اجرا کنید، که این امکان رو فراهم می‌کنه که عملیات‌های سنگین پردازشی رو بدون مسدود کردن رابط کاربری (UI) انجام بدید.


## دستکاری پیشرفته DOM

### 11. مفهوم Shadow DOM چی هست و چطور ازش استفاده می‌کنیم؟
> برای توضیح، Shadow DOM یه استاندارد وب هست که به شما اجازه میده یک درخت DOM و استایل‌های CSS رو محصور کنید به‌طوری که از DOM اصلی سند پنهان و جدا بشه. این برای ایجاد کامپوننت‌های وب مفید هست.

### 12. چطور می‌تونید DOM رو به طور مؤثر بروزرسانی کنید تا از reflows و repaints کمینه کنید؟
> برای بروزرسانی مؤثر DOM، تغییرات DOM رو دسته‌بندی کنید، از `DocumentFragment` استفاده کنید، از layout thrashing کم کنید و برای انیمیشن‌ها از `requestAnimationFrame` استفاده کنید.

## مدیریت حافظه

### 13. مفهوم جمع‌آوری زباله (garbage collection) در جاوا اسکریپت چیه؟
> جمع‌آوری زباله فرآیندیه که به‌طور خودکار حافظه‌ای که دیگه استفاده نمیشه رو آزاد می‌کنه. یعنی اشیایی که دیگه بهشون نیازی نیست یا بهشون دسترسی نداریم، حذف میشن.

### 14. نشت حافظه (memory leaks) چیه و چطور می‌تونیم ازش جلوگیری کنیم؟
> نشت حافظه زمانی پیش میاد که حافظه‌ای که به یه چیزی اختصاص داده شده به‌درستی آزاد نشه، و این باعث میشه مصرف حافظه با گذشت زمان بیشتر بشه. برای جلوگیری از این مشکل، باید ارجاع‌ها به اشیایی که دیگه لازم نیستن رو حذف کنیم، از متغیرهای جهانی کمتر استفاده کنیم و از ابزارهایی مثل Chrome DevTools برای مانیتور کردن مصرف حافظه استفاده کنیم.

## مدیریت خطا پیشرفته

### 15. خطاهای سفارشی (custom errors) چی هستن و چطور می‌تونیم اون‌ها رو در جاوا اسکریپت ایجاد کنیم؟
> خطاهای سفارشی نوعی از خطاها هستن که توسط کاربر تعریف میشن و از کلاس داخلی `Error` ارث‌بری می‌کنن. مثال:
> ```javascript
> class CustomError extends Error {
>   constructor(message) {
>     super(message);
>     this.name = 'CustomError';
>   }
> }
> throw new CustomError('This is a custom error');
> ```

## ماژول‌ها و ابزارهای ساخت

### 16. تفاوت بین ماژول‌های ES6 و ماژول‌های CommonJS چیه؟
> ماژول‌های ES6 از دستورات `import` و `export` استفاده می‌کنن و به‌طور استاتیکی تحلیل میشن، که اجازه میده تا بخش‌های غیرضروری (tree shaking) حذف بشه. ماژول‌های CommonJS از `require` و `module.exports` استفاده می‌کنن و به‌صورت پویا بارگذاری میشن.

### 17. باندلرها (Bundlers) مثل Webpack چی هستن و چرا ازشون استفاده میشه؟
> باندلرهایی مثل Webpack ابزارهایی هستن که ماژول‌های جاوا اسکریپت رو به یک یا چند فایل بهینه‌شده برای مرورگر تبدیل می‌کنن. این ابزارها به مدیریت وابستگی‌ها، تقسیم کد (code splitting) و بهینه‌سازی خروجی برای تولید کمک می‌کنن.

## امنیت

### 18. رایج‌ترین آسیب‌پذیری‌های امنیتی در جاوا اسکریپت چی هستن و چطور می‌تونیم اون‌ها رو کاهش بدیم؟
> آسیب‌پذیری‌های رایج شامل XSS (Cross-Site Scripting)، CSRF (Cross-Site Request Forgery)، و تزریق کد (code injection) هستن. می‌تونیم این مشکلات رو با اعتبارسنجی و پاک‌سازی ورودی‌های کاربر، استفاده از Content Security Policy (CSP)، و پیاده‌سازی مکانیزم‌های احراز هویت و مجوزدهی مناسب کاهش بدیم.

## ویژگی‌های پیشرفته APIها و مرورگر

### 19. سرویس ورکرها (service workers) چی هستن و چطور اپلیکیشن‌های وب پیشرفته (PWAs) رو ممکن می‌کنن؟
> سرویس ورکرها اسکریپت‌هایی هستن که در پس‌زمینه اجرا میشن و امکاناتی مثل کش کردن، اعلان‌های اجباری (push notifications)، و همگام‌سازی در پس‌زمینه رو فراهم می‌کنن. این ویژگی‌ها امکان استفاده آفلاین و بهبود عملکرد اپلیکیشن‌های وب پیشرفته (PWAs) رو فراهم می‌کنن.

### 20. استفاده از IndexedDB در اپلیکیشن‌های وب رو توضیح بده.
> برای توضیح، IndexedDB یک API سطح پایین برای ذخیره حجم زیادی از داده‌های ساختاریافته در مرورگره. این API امکان دسترسی غیرهمزمان به داده‌ها رو فراهم می‌کنه و از تراکنش‌ها پشتیبانی می‌کنه، که اون رو برای ذخیره‌سازی آفلاین و نیازهای داده‌ای پیچیده مناسب می‌کنه.

### 21. وب‌ اسمبلی چیه و چطور با جاوا اسکریپت تعامل داره؟
> وب‌ اسمبلی یه فرمت باینری برای یه ماشین مجازی مبتنی بر استکه که برای کامپایل کردن زبان‌های سطح بالا مثل C، C++، و Rust طراحی شده. این تکنولوژی اجازه میده که کد با سرعت بالا توی مرورگر اجرا بشه و می‌تونه از طریق API جاوا اسکریپت باهاش تعامل داشته باشه.

## الگوها و روش‌های پیشرفته

### 22. مفهوم برنامه‌نویسی تابعی رو توضیح بده و بگو چطور به جاوا اسکریپت مربوط میشه؟
> برنامه‌نویسی تابعی یه پارادایم برنامه‌نویسیه که محاسبات رو به عنوان ارزیابی توابع ریاضی در نظر می‌گیره و از تغییر حالت و داده‌های متغیر اجتناب می‌کنه. جاوا اسکریپت از برنامه‌نویسی تابعی پشتیبانی می‌کنه از طریق توابع کلاس اول (first-class functions)، توابع مرتبه‌بالا (higher-order functions)، و متدهایی مثل `map`، `reduce` و `filter`.

### 23. الگوی مشاهده‌گر (observer pattern) چیه و چطور توی جاوا اسکریپت پیاده‌سازی میشه؟
> الگوی مشاهده‌گر یه الگوی طراحی هست که توش یه شیء (subject) یه لیست از وابستگی‌ها (observables) رو نگه می‌داره و به اونا از تغییرات وضعیت اطلاع میده. این الگو می‌تونه با استفاده از event listenerها یا کتابخانه‌هایی مثل RxJS برای برنامه‌نویسی واکنشی پیاده‌سازی بشه.
### 24. چطور می‌تونیم debouncing و throttling رو توی جاوا اسکریپت پیاده‌سازی کنیم؟
> برای توضیح، debouncing اطمینان حاصل می‌کنه که یه تابع فقط بعد از گذشت یه تاخیر مشخص از آخرین فراخوانی اجرا بشه. throttling هم اطمینان حاصل می‌کنه که یه تابع حداکثر یک بار در یه بازه زمانی مشخص فراخوانی بشه. مثال:
> ```javascript
> function debounce(fn, delay) {
>   let timer;
>   return function(...args) {
>     // تایمر قبلی رو پاک کن، اگر وجود داشت، و یه تایمر جدید تنظیم کن
>     clearTimeout(timer);
>     timer = setTimeout(() => fn.apply(this, args), delay);
>   };
> }
> function throttle(fn, limit) {
>   let lastCall = 0;
>   return function(...args) {
>     const now = Date.now();
>     // اگر به اندازه کافی از فراخوانی قبلی گذشته باشه، تابع رو اجرا کن
>     if (now - lastCall >= limit) {
>       lastCall = now;
>       fn.apply(this, args);
>     }
>   };
> }
> ```

### 25. مفهوم duck typing در جاوا اسکریپت چیه؟
> برای توضیح، Duck typing مفهومی هست که در اون قابلیت استفاده یه شیء بر اساس وجود متدها و ویژگی‌های خاصی سنجیده میشه، نه بر اساس نوع واقعی اون شیء. معمولاً این مفهوم رو با عبارت "اگر شبیه اردک به نظر میاد و صدای اردک میده، پس اردکه" توضیح میدن.

### 26. بهینه‌سازی فراخوانی در انتها (tail call optimization) چیه و چطور توی جاوا اسکریپت کار می‌کنه؟
> بهینه‌سازی فراخوانی در انتها یه ویژگی در بعضی از موتورهای جاوا اسکریپته که فراخوانی‌های بازگشتی که در موقعیت انتهایی (آخرین عمل در تابع) قرار دارن رو بهینه می‌کنه. این کار باعث استفاده بهینه‌تر از حافظه میشه و می‌تونه از بروز خطاهای stack overflow جلوگیری کنه.
