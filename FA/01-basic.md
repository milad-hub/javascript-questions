# سوالات سطح پایه JavaScript

## متغیرها و انواع داده

### 1. تفاوت بین `let`, `const`, و `var` چیه؟
> تفاوت در اینه که `var` تابع-محدوده (function-scoped) هست، ولی `let` و `const` بلوک-محدوده (block-scoped) هستن. `let` اجازه به‌روزرسانی میده ولی نه اعلام دوباره، در حالی که `const` اجازه هیچ‌کدوم رو نمیده.

### 2. انواع مختلف داده در JavaScript چیا هستن؟
> انواع داده‌های اولیه شامل `Number`, `String`, `Boolean`, `Undefined`, `Null`, `Symbol`, و `BigInt` هستن. داده‌های غیر اولیه شامل `Object` (که شامل `Array`, `Function` و غیره میشه) هستن.

### 3. چطوری بررسی می‌کنی که یک متغیر یک آرایه هست؟
> با استفاده از متد `Array.isArray(variable)` می‌تونی بررسی کنی.

### 4. عملگر `typeof` چیه؟
> عملگر `typeof` یک رشته برمی‌گردونه که نوع عملوند ارزیابی‌نشده رو نشون میده.

## عملگرها و ساختارهای کنترلی

### 5. تفاوت بین `==` و `===` چیه؟
> تفاوت در اینه که `==` تبدیل نوع (type coercion) انجام میده و برابری مقدار رو بررسی می‌کنه، در حالی که `===` هم برابری مقدار و هم برابری نوع (strict equality) رو بررسی می‌کنه.

### 6. چطوری با استثناها در JavaScript برخورد می‌کنی؟
> با استفاده از بلوک‌های `try`, `catch`, و `finally` می‌تونی با استثناها برخورد کنی. `try` یک بلوک کد رو برای خطاها تست می‌کنه، `catch` خطا رو مدیریت می‌کنه، و `finally` کدی رو اجرا می‌کنه بعد از بلوک‌های `try` و `catch`، بدون توجه به نتیجه.

## توابع

### 7. تابع callback چیه؟
> تابع callback تابعیه که به عنوان آرگومان به توابع دیگه پاس داده میشه و سپس داخل تابع خارجی اجرا میشه تا یک کار خاص رو کامل کنه.

### 8. کلیدواژه `this` در JavaScript رو توضیح بده.
> کلیدواژه `this` بستگی به زمینه اجرا داره. در یک متد، `this` به شیء اشاره می‌کنه. در یک تابع، `this` به شیء سراسری (یا undefined در حالت strict) اشاره می‌کنه. در یک event handler، `this` به عنصری که رویداد رو دریافت کرده اشاره می‌کنه.

### 9. شیء `arguments` چیه؟
> شیء `arguments` یک شیء شبیه به آرایه هست که داخل توابع در دسترسه و حاوی مقادیر آرگومان‌هایی هست که به تابع پاس داده شدن.

### 10. پارامترهای پیش‌فرض در JavaScript چیه؟
> پارامترهای پیش‌فرض به شما اجازه میدن تا پارامترهای تابع رو با مقادیر پیش‌فرض مقداردهی کنید اگه هیچ مقداری پاس داده نشه یا undefined پاس داده بشه.
> ```javascript
> function greet(name = 'Guest') { console.log(`Hello, ${name}`); }
> ```

## آرایه‌ها و اشیاء

### 11. چطوری یک شیء در JavaScript ایجاد می‌کنی؟
> اشیاء می‌تونن با استفاده از literal‌های شیء، سازنده‌ها (constructors)، یا متد `Object.create` ایجاد بشن.

### 12. چطوری دو شیء رو در JavaScript ادغام می‌کنی؟
> با استفاده از `Object.assign` یا spread operator می‌تونی دو شیء رو ادغام کنی.
> ```javascript
> const merged = Object.assign({}, obj1, obj2);
> const merged = {...obj1, ...obj2};
> ```

### 13. چطوری یک عنصر رو به ابتدای یک آرایه اضافه می‌کنی؟
> با استفاده از متد `unshift` می‌تونی یک عنصر رو به ابتدای یک آرایه اضافه کنی.
> ```javascript
> array.unshift(element);
> ```

### 14. چطوری آخرین عنصر از یک آرایه رو حذف می‌کنی؟
> با استفاده از متد `pop` می‌تونی آخرین عنصر رو حذف کنی.
> ```javascript
> array.pop();
> ```

### 15. چطوری یک کپی سطحی از یک آرایه ایجاد می‌کنی؟
> با استفاده از متد `slice` یا spread operator می‌تونی یک کپی سطحی ایجاد کنی.
> ```javascript
> const copy = array.slice();
> const copy = [...array];
> ```

### 16. چطوری یک شیء شبیه به آرایه رو به یک آرایه تبدیل می‌کنی؟
> با استفاده از `Array.from` یا spread operator می‌تونی یک شیء شبیه به آرایه رو به یک آرایه تبدیل کنی.
> ```javascript
> const array = Array.from(arrayLike);
> const array = [...arrayLike];
> ```

## رشته‌ها

### 17. رشته template literals چیه و چطوری ازشون استفاده می‌کنی؟
> رشته template literals به شما این امکان رو میده که از بیان‌های جاسازی‌شده، رشته‌های چند خطی و جایگزینی رشته استفاده کنی. این رشته‌ها با backticks (`) به جای کوتیشن‌های تک یا دوتایی محصور میشن.
> ```javascript
> const name = 'John';
> const message = `Hello, ${name}`;
> ```

### 18. چطوری یک رشته رو به عدد تبدیل می‌کنی در JavaScript؟
> با استفاده از `parseInt(string)`, `parseFloat(string)`, `Number(string)`, یا عملگر یونری `+` می‌تونی یک رشته رو به عدد تبدیل کنی.

## دستکاری DOM

### 19. تفاوت بین `innerHTML` و `innerText` چیه؟
> تفاوت در اینه که `innerHTML` تمام متن شامل تگ‌های HTML رو برمی‌گردونه، در حالی که `innerText` فقط محتوای متنی بدون تگ‌های HTML رو برمی‌گردونه.

### 20. چطوری می‌تونی رفتار پیش‌فرض رو در یک event handler جلوگیری کنی؟
> با فراخوانی متد `event.preventDefault()` داخل event handler می‌تونی از رفتار پیش‌فرض جلوگیری کنی.

## رویدادها

### 21. رویداد event delegation چیه؟
> رویداد event delegation به شما اجازه میده تا از یک event listener واحد برای مدیریت رویدادهای مشابه در چندین عنصر استفاده کنی با بهره‌گیری از propagation (bubbling) رویداد در درخت DOM.

### 22. رویداد event bubbling چیه؟
> رویداد event bubbling نوعی propagation رویداد هست که در اون رویداد اول در عنصر هدف تریگر میشه و سپس به ترتیب در هر یک از عناصر جدی اون تا ریشه سند تریگر میشه.

## متفرقه

### 23. ویژگی `NaN` در JavaScript چیه؟
> ویژگی `NaN` مخفف "Not-a-Number" هست و یک مقدار رو نشون میده که از یک خطای محاسباتی ناشی میشه که نتیجه عددی تعریف نشده‌ای تولید می‌کنه.

### 24. دستور `use strict` چیه؟
> دستور `"use strict"` حالت strict رو فعال می‌کنه که کمک می‌کنه خطاهای رایج کدنویسی رو بگیری و از انجام برخی اقدامات جلوگیری کنی. این کار باعث میشه کد JavaScript امن‌تر و بهینه‌تر بشه.

### 25. کد polyfill چیه؟
> کد polyfill کدی هست که یک ویژگی رو در مرورگرهای وبی که به صورت بومی از اون ویژگی پشتیبانی نمی‌کنن، پیاده‌سازی می‌کنه و تضمین می‌کنه که در مرورگرهای مختلف سازگاری برقرار بشه.

### 26. مکانیزم CORS چیه؟
> مکانیزم CORS (Cross-Origin Resource Sharing) مکانیزمی هست که به منابع محدود در یک صفحه وب اجازه میده از یک دامنه دیگه غیر از دامنه‌ای که منبع از اون نشأت گرفته درخواست بشن.

### 27. مفهوم hoisting در JavaScript چیه؟
> مفهوم hoisting رفتار JavaScript در انتقال اعلامیه‌ها به بالای دامنه جاری هست. اعلامیه‌های متغیر (با استفاده از `var`) و اعلامیه‌های تابع hoist میشن، ولی مقداردهی اولیه اون‌ها نه.

### 28. چطوری بررسی می‌کنی که یک شیء در JavaScript خالی هست یا نه؟
> با بررسی طول کلیدهای شیء می‌تونی بررسی کنی که خالی هست یا نه:
> ```javascript
> Object.keys(obj).length === 0;
> ```

### 29. هدف از `JSON.stringify` چیه؟
> هدف از `JSON.stringify` تبدیل یک شیء JavaScript به یک رشته JSON هست.

### 30. هدف از `JSON.parse` چیه؟
> هدف از `JSON.parse` تبدیل یک رشته JSON به یک شیء JavaScript هست.
