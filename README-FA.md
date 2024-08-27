<style>
  @import url('https://fonts.googleapis.com/css2?family=Vazirmatn:wght@100..900&display=swap');
  body {
    font-family: 'Vazirmatn', sans-serif;
    direction: rtl;
    text-align: right;
  }
  h2 {
    color: #4CAF50;
    font-family: 'Vazirmatn', sans-serif;
    text-align: right;
  }
  h3 {
    color: #2196F3;
    font-family: 'Vazirmatn', sans-serif;
    text-align: right;
  }
  ul {
    font-family: 'Vazirmatn', sans-serif;
    line-height: 1.6;
    text-align: right;
    list-style-type: none;
    padding: 0;
  }
  a {
    text-decoration: none;
    color: #333;
  }
  a:hover {
    color: #2196F3;
  }
  .view-link {
    display: inline-block;
    padding: 6px 12px;
    margin: 8px 0;
    background-color: #f1f1f1;
    color: #333;
    border: 1px solid #ccc;
    border-radius: 5px;
    font-size: 14px;
    text-align: center;
    text-decoration: none;
    font-weight: bold;
  }
  .view-link:hover {
    background-color: #e0e0e0;
    border-color: #b0b0b0;
  }
  .container {
    display: flex;
    justify-content: flex-end;
    flex-wrap: wrap;
    gap: 20px;
  }
  .card {
    flex: 1;
    min-width: 250px;
    border: 1px solid #ccc;
    border-radius: 10px;
    padding: 10px;
    background-color: #f9f9f9;
    text-align: right;
  }
</style>

# سوالات جاوا اسکریپت

<p>تو این ریپازیتوری کلی فایل آموزشی درباره جاوا اسکریپت و ویژگی‌های مختلف نسخه‌های مختلف ECMAScript جمع‌آوری شده. هر فایل به صورت Markdown نوشته شده و با مثال‌های عملی، ویژگی‌ها و مفاهیم رو به طور کامل توضیح میده.</p>

## 📚 فهرست مطالب

<div class="container">
  <div class="card">
    <h3>📘 مباحث جاوا اسکریپت</h3>
    <ul>
      <li><a href="#basic">مباحث پایه‌ای</a></li>
      <li><a href="#intermediate">مباحث متوسط</a></li>
      <li><a href="#advanced">مباحث پیشرفته</a></li>
    </ul>
  </div>
  <div class="card">
    <h3>🧩 ویژگی‌های ECMAScript</h3>
    <ul>
      <li><a href="#es5">ES5 - 2009</a></li>
      <li><a href="#es6">ES6 - 2015</a></li>
      <li><a href="#es7">ES7 - 2016</a></li>
      <li><a href="#es8">ES8 - 2017</a></li>
      <li><a href="#es9">ES9 - 2018</a></li>
      <li><a href="#es10">ES10 - 2019</a></li>
      <li><a href="#es11">ES11 - 2020</a></li>
      <li><a href="#es12">ES12 - 2021</a></li>
      <li><a href="#es13">ES13 - 2022</a></li>
      <li><a href="#es14">ES14 - 2023</a></li>
      <li><a href="#es15">ES15 - 2024</a></li>
    </ul>
  </div>
</div>

---

<h2 id="basic">مباحث پایه‌ای</h2>
<p><a href="FA/01-basic.md" class="view-link">مشاهده فایل</a></p>
<ul>
  <li>معرفی جاوا اسکریپت</li>
  <li>انواع داده‌ها و متغیرها</li>
  <li>عملگرها و عبارات</li>
  <li>ساختارهای شرطی</li>
  <li>حلقه‌ها</li>
</ul>

<h2 id="intermediate">مباحث متوسط</h2>
<p><a href="FA/02-intermediate.md" class="view-link">مشاهده فایل</a></p>
<ul>
  <li>توابع و حوزه متغیرها</li>
  <li>کار با آرایه‌ها و اشیاء</li>
  <li>مدیریت خطاها</li>
  <li>مفهوم callback و Promise</li>
  <li>آشنایی با DOM و BOM</li>
</ul>

<h2 id="advanced">مباحث پیشرفته</h2>
<p><a href="FA/03-advance.md" class="view-link">مشاهده فایل</a></p>
<ul>
  <li>برنامه‌نویسی شیء‌گرا</li>
  <li>مدیریت حافظه و بهینه‌سازی</li>
  <li>متدهای پیشرفته کار با آرایه‌ها و رشته‌ها</li>
  <li>معرفی و استفاده از `async/await`</li>
  <li>مفاهیم ماژولاریتی و مدیریت ماژول‌ها</li>
</ul>

---

<h2 id="es5">مباحث ES5 - 2009</h2>
<p><a href="FA/04-ES5-2009.md" class="view-link">مشاهده فایل</a></p>
<ul>
  <li><a href="FA/04-ES5-2009.md#use-strict-در-جاوا-اسکریپت">"use strict" و مزایای اون</a></li>
  <li><a href="FA/04-ES5-2009.md#دسترسی-به-کاراکترهای-رشته-با-استفاده-از-ایندکس">دسترسی به کاراکترهای رشته با استفاده از ایندکس</a></li>
  <li><a href="FA/04-ES5-2009.md#رشته‌های-چند-خطی">رشته‌های چند خطی</a></li>
  <li><a href="FA/04-ES5-2009.md#استفاده-از-کلمات-رزرو-شده-به-عنوان-نام-ویژگی">استفاده از کلمات رزرو شده به عنوان نام ویژگی</a></li>
  <li><a href="FA/04-ES5-2009.md#متدهای-جدید-string-و-array">متدهای جدید String و Array</a></li>
  <li><a href="FA/04-ES5-2009.md#معرفی-json-و-متدهای-مرتبط">معرفی JSON و متدهای مرتبط</a></li>
  <li><a href="FA/04-ES5-2009.md#ویژگی‌های-جدید-object-و-متدهای-آنها">ویژگی‌های جدید Object و متدهای اون‌ها</a></li>
</ul>

<h2 id="es6">مباحث ES6 - 2015</h2>
<p><a href="FA/05-ES6-2015.md" class="view-link">مشاهده فایل</a></p>
<ul>
  <li><a href="FA/05-ES6-2015.md#کلمه-کلیدی-let-در-جاوا-اسکریپت">کلمه کلیدی let و const</a></li>
  <li><a href="FA/05-ES6-2015.md#توابع-پیکانی-arrow-functions">توابع پیکانی (Arrow Functions)</a></li>
  <li><a href="FA/05-ES6-2015.md#تخریب-شیء-و-آرایه-object-destructuring">تخریب شیء و آرایه (Destructuring)</a></li>
  <li><a href="FA/05-ES6-2015.md#عملگر-spread">عملگر Spread</a></li>
  <li><a href="FA/05-ES6-2015.md#حلقه-forof">حلقه For/of</a></li>
  <li><a href="FA/05-ES6-2015.md#کلاس‌ها-در-جاوا-اسکریپت">کلاس‌ها و استفاده از اون‌ها</a></li>
  <li><a href="FA/05-ES6-2015.md#وعده‌ها-promises-در-جاوا-اسکریپت">وعده‌ها (Promises)</a></li>
  <li><a href="FA/05-ES6-2015.md#نوع-داده-symbol">نوع داده Symbol</a></li>
  <li><a href="FA/05-ES6-2015.md#پارامترهای-پیش‌فرض-تو-توابع">پارامترهای پیش‌فرض و Rest</a></li>
</ul>

<h2 id="es7">مباحث ES7 - 2016</h2>
<p><a href="FA/06-ES7-2016.md" class="view-link">مشاهده فایل</a></p>
<ul>
  <li><a href="FA/06-ES7-2016.md#عملگر-توان-در-جاوا-اسکریپت">عملگر توان (**)</a></li>
  <li><a href="FA/06-ES7-2016.md#عملگر-اختصاص-توان">عملگر اختصاص توان (**=)</a></li>
  <li><a href="FA/06-ES7-2016.md#متد-arrayincludes">متد Array.includes</a></li>
</ul>

<h2 id="es8">مباحث ES8 - 2017</h2>
<p><a href="FA/07-ES8-2017.md" class="view-link">مشاهده فایل</a></p>
<ul>
  <li><a href="FA/07-ES8-2017.md#پدینگ-رشته-در-جاوا-اسکریپت">پدینگ رشته (padStart و padEnd)</a></li>
  <li><a href="FA/07-ES8-2017.md#متد-objectentries-و-objectvalues">متد Object.entries و Object.values</a></li>
  <li><a href="FA/07-ES8-2017.md#سینتکس-asyncawait">سینتکس async/await</a></li>
  <li><a href="FA/07-ES8-2017.md#کاماهای-پایانی-در-توابع">کاماهای پایانی در توابع</a></li>
</ul>

<h2 id="es9">مباحث ES9 - 2018</h2>
<p><a href="FA/08-ES9-2018.md" class="view-link">مشاهده فایل</a></p>
<ul>
  <li><a href="FA/08-ES9-2018.md#حلقه-asynchronous-iteration">حلقه Asynchronous Iteration</a></li>
  <li><a href="FA/08-ES9-2018.md#متد-promisefinally">متد Promise.prototype.finally</a></li>
  <li><a href="FA/08-ES9-2018.md#ویژگی‌های-object-rest">ویژگی‌های Object Rest</a></li>
  <li><a href="FA/08-ES9-2018.md#ویژگی‌های-جدید-regexp">ویژگی‌های جدید RegExp</a></li>
</ul>

<h2 id="es10">مباحث ES10 - 2019</h2>
<p><a href="FA/09-ES10-2019.md" class="view-link">مشاهده فایل</a></p>
<ul>
  <li><a href="FA/09-ES10-2019.md#متدهای-stringprototypetrimstart-و-stringprototypetrimend">متدهای String.prototype.trimStart و trimEnd</a></li>
  <li><a href="FA/09-ES10-2019.md#متد-objectfromentries">متد Object.fromEntries</a></li>
  <li><a href="FA/09-ES10-2019.md#ویژگی-optional-catch-binding">ویژگی Optional Catch Binding</a></li>
  <li><a href="FA/09-ES10-2019.md#متدهای-arrayprototypeflat-و-arrayprototypeflatmap">متدهای Array.prototype.flat و flatMap</a></li>
</ul>

<h2 id="es11">مباحث ES11 - 2020</h2>
<p><a href="FA/10-ES11-2020.md" class="view-link">مشاهده فایل</a></p>
<ul>
  <li><a href="FA/10-ES11-2020.md#ویژگی-bigint">BigInt</a></li>
  <li><a href="FA/10-ES11-2020.md#متد-stringprototypematchall">متد String.prototype.matchAll</a></li>
  <li><a href="FA/10-ES11-2020.md#عملگر-nullish-coalescing">عملگر Nullish Coalescing (??)</a></li>
  <li><a href="FA/10-ES11-2020.md#عملگر-optional-chaining">عملگر Optional Chaining (?.)</a></li>
</ul>

<h2 id="es12">مباحث ES12 - 2021</h2>
<p><a href="FA/11-ES12-2021.md" class="view-link">مشاهده فایل</a></p>
<ul>
  <li><a href="FA/11-ES12-2021.md#متد-promiseany">متد Promise.any</a></li>
  <li><a href="FA/11-ES12-2021.md#متد-replaceall">متد replaceAll</a></li>
  <li><a href="FA/11-ES12-2021.md#جداکننده‌های-عددی-">جداکننده‌های عددی (`_`)</a></li>
</ul>

<h2 id="es13">مباحث ES13 - 2022</h2>
<p><a href="FA/12-ES13-2022.md" class="view-link">مشاهده فایل</a></p>
<ul>
  <li><a href="FA/12-ES13-2022.md#متد-arrayat-و-stringat">متد Array.at و String.at</a></li>
  <li><a href="FA/12-ES13-2022.md#فلگ-d-در-regexp">فلگ d در RegExp</a></li>
  <li><a href="FA/12-ES13-2022.md#متد-objecthasown">متد Object.hasOwn</a></li>
</ul>

<h2 id="es14">مباحث ES14 - 2023</h2>
<p><a href="FA/13-ES14-2023.md" class="view-link">مشاهده فایل</a></p>
<ul>
  <li><a href="FA/13-ES14-2023.md#متد-arrayfindlast">متد Array.findLast</a></li>
  <li><a href="FA/13-ES14-2023.md#متد-arrayfindlastindex">متد Array.findLastIndex</a></li>
  <li><a href="FA/13-ES14-2023.md#متد-arraytoreversed">متد Array.toReversed</a></li>
</ul>

<h2 id="es15">مباحث ES15 - 2024</h2>
<p><a href="FA/14-ES15-2024.md" class="view-link">مشاهده فایل</a></p>
<ul>
  <li><a href="FA/14-ES15-2024.md#متد-objectgroupby">متد Object.groupBy</a></li>
  <li><a href="FA/14-ES15-2024.md#متد-mapgroupby">متد Map.groupBy</a></li>
  <li><a href="FA/14-ES15-2024.md#ویژگی‌های-temporalplaindate-plaintime-plainmonthday-plainyearmonth">ویژگی‌های Temporal.PlainDate, PlainTime, PlainMonthDay, PlainYearMonth</a></li>
</ul>