# iran-cities
Iran-cities is the most accurate database of city, county, province and villages of Iran. Based on official released data.

<div dir="rtl">
  
# بانک اطلاعات(دیتابیس) جامع و کامل اسامی استانها، شهرستانها، شهرها و روستاهای ایران

iran-cities .بانک اطلاعاتی حاوی تمامی تقسیمات کشوری ایران می باشد
    سطوح تقسیمات سیاسی کشور ایران از بالاترین سطح تا پایین ترین آن به ترتیب شامل : استان، شهرستان، بخش و دهستان میباشد. بدینگونه که هر استان از چند شهرستان، هر شهرستان از چند بخش و هر بخش از چند دهستان تشکیل میشود. لازم به ذکر است که هر دهستان نیز شامل تعدادی نقاط روستایی، مکان و مزرعه میباشد که عناصر تقسیماتی نامیده میشوند.

![Divisions of Iran](/docs/images/iran_divisions.png)
    
این دیتابیس حاوی تمامی عناصر تقسیماتی کشور یعنی استان، شهرستان، بخش، شهر، دهستان و روستا/آبادی های ایران می باشد که به طور کامل براساس اطلاعات رسمی ارائه شده توسط مرکز آمار ایران ساخته شده است. برنامه نویسان و توسعه دهندگان نرم افزار می توانند براساس نیاز خود از کل یا بخشی از این داده ها در پروژه های خود استفاده نمایند.
    
    
# تاریخچه
این بانک را زمانی ایجاد کردم که ناامید شدم! برای پروژه ای نیاز به بانک اطلاعاتی دقیق تمامی شهرهای ایران را داشتم، اما با جستجوی فراوان در اینترنت حتی یک نمونه کامل و بدون نقص پیدا نکردم.
قبل از اینکه جستجو کنم به نظرم یافتن چنین چیزی بسیار ساده و پیش پا افتاده بود، اما در کمال تعجب نبود!
    
با بررسی بانک های موجود بر روی اینترنت اشکالات زیر مشاهده گردید:
- برخی از آنها بسیار قدیمی بودند و بسیاری از مناطق و شهرها در آنها لیست نشده بود، مثلا شامل استان البرز نبودند.
- برخی از آنها تنها شامل برخی از شهرهای ایران بودند
- برخی از آنها به اشتباه نام شهرستان های ایران را به عنوان لیست شهرهای ایران درج کرده بودند.
- برخی از آنها بسیاری از شهرهای ایران را از قلم انداخته بودند، مثلا در یک بررسی سطحی مشخص شد که به عنوان مثال فاقد شهرهای لواسان در استان تهران و ساوه در استان مرکزی هستند.
- علاوه بر اینها در اکثر آنها به جای استفاده از حروف فارسی از حروف معادل عربی (ي و ك) استفاده شده بود که برای جستجوی کاربران در اغلب سیستم عامل ها مشکل زا است.

به طور خلاصه اغلب بانک های موجود از روی چند منبع ناقص و قدیمی کپی شده بودند و دارای ایرادات فراوانی بودند.

این بانک تمام این اشکالات را برطرف کرده است و به طور کامل از روی آخرین داده های رسمی ایجاد گردیده است.


# نسخه 2.۰
این نسخه به روز رسانی فروردین 1399 می باشد. پس از استخراج و پاکسازی داده ها، این نسخه شامل ۳۱ استان، 434 شهرستان، 1071 بخش، 2601 دهستان، 1518 شهر و 97915 روستا(آبادی و آبادی بلوکه) می باشد. بدیهی است در صورت به روز رسانی آمار رسمی، نسخه جدید هم براساس آخرین داده ها به روزآوری خواهد شد.

همچنین این ویژگیها نسبت به نسخه قبلی افزوده شده اند:
- افزودن دهستان ها و روستاها(به تفکیک آبادی و آبادی-بلوکه مانند مرغداری ها و واحدهای صنعتی)
- افزودن نواحی شهری و شهرداری که در شهرهای بزرگ وجود دارد(مناطق شهرداری مثل تهران منطقه 1، منطقه 2 و ...)
- نام جداول از city, county, province به ostan, shahr و ... تغییر داده شده است.
    
# نسخه ۱.۰
این بانک براساس براساس آخرین تقسیمات کشوری تا پایان سال ۱۳۹۴ که توسط مرکز آمار ایران ارائه شده است ایجاد گردیده است. در زمان ایجاد این نسخه(فروردین 1396) این آخرین اطلاعات ارائه شده توسط مرکز آمار است که براساس آن  کشور ایران از ۳۱ استان، ۴۲۹ شهرستان، ۱۰۵۷ بخش، ۲۵۸۹ دهستان و ۱۲۴۵ شهر تشکیل یافته‌است. 
بدیهی است در صورت به روز رسانی آمار رسمی، نسخه جدید این بانک هم براساس آخرین داده ها به روزآوری خواهد شد.


# ساختار
ساختار شامل جدول های 'ostan', 'shahrestan', 'bakhsh', 'dehestan', 'shahr', 'abadi' می باشد که نکات زیر قابل توجه می باشند:
- حداکثر کلیدهای خارجی در داخل جدول ها گنجانده شده است تا سهولت لازم برای طراحی انواع رابطه بین جداول براساس نیاز وجود داشته باشد
- داده ها به دو فرمت CSV و SQL ارائه شده است که باید قابلیت import کردن به تمامی دیتابیس های سازگار با SQL استاندارد(مانند MySQL, MSSQL, Oracle , غیره) را داشته باشد
- در جدول shahr، فیلد shahr_type برای جداسازی شهر و ناحیه شهری تعبیه شده است
- در جدول abadi، فیلد abadi_type برای جداسازی آبادی/روستا از آبادی-بلوکه تعبیه شده است


![sample regions of Iran](/docs/images/sample_regions.png)
![sample queries on iran-cities](/docs/images/sample_queries.png)

</div>

# License
MIT License

Created by Ahmad Azizi https://github.com/ahmadazizi/
