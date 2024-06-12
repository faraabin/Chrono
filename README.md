---

![Logo](images/Logo.png)
# ماژول کرونو
ماژول کرونو برای [اندازه گیری زمان در نرم افزار نهفته](doc/%D8%A7%D9%86%D8%AF%D8%A7%D8%B2%D9%87%20%DA%AF%DB%8C%D8%B1%DB%8C%20%D8%B2%D9%85%D8%A7%D9%86%20%D8%AF%D8%B1%20%D9%86%D8%B1%D9%85%20%D8%A7%D9%81%D8%B2%D8%A7%D8%B1%20%D9%86%D9%87%D9%81%D8%AA%D9%87.md) است. این ماژول با استفاده از یک تیک سخت افزاری یا نرم افزاری، تمام توابع پایه لازم برای اندازه گیری زمان را در اختیار کاربر قرار می دهد.
## اندازه گیری زمان در نرم افزار نهفته
از آنجایی که یکی از بارزترین ویژگی های نرم افزار نهفته، اجرای کد در زمان بندی های مشخص است، [اندازه گیری زمان در نرم افزار نهفته](doc/%D8%A7%D9%86%D8%AF%D8%A7%D8%B2%D9%87%20%DA%AF%DB%8C%D8%B1%DB%8C%20%D8%B2%D9%85%D8%A7%D9%86%20%D8%AF%D8%B1%20%D9%86%D8%B1%D9%85%20%D8%A7%D9%81%D8%B2%D8%A7%D8%B1%20%D9%86%D9%87%D9%81%D8%AA%D9%87.md) اهمیت ویژه ای دارد.
 نرم افزار نهفته معمولا برای کنترل، مشاهده کردن و یا جمع آوری و ذخیره اطلاعات سیستم ها به کار می رود. در تمام این کاربردها، زمان بندی دقیق اجرای نرم افزار، مورد نظر توسعه دهنده است. و این یکی از تفاوت های مهم بین نرم افزار نهفته و نرم افزارهای غیر نهفته (کامپیوتری) است. در نرم افزارهای کامپیوتری معمولا پارامترهایی مانند متوسط سرعت اجرای برنامه، متوسط خروجی اطلاعات و پارامترهایی از این دست اهمیت دارند. در حالی که در نرم افزارهای نهفته، اجرای هر بخشی از کد در زمان بندی مشخص حائز اهمیت است.

## قابلیت ها
- قابل استفاده با تیک سخت افزاری و نرم افزاری
- تیک مورد نیاز میتواند به صورت اشاره گر به متغیر و یا به صورت یک تابع دریافت شود.
- دریافت مقدار تیک خام و تیک بر حسب میلی ثانیه
- محاسبه و ارائه حداکثر زمان قابل اندازه گیری
- توابع تاخیر بر حسب میکروثانیه، میلی ثانیه و ثانیه
- توابع Timeout بر حسب میکروثانیه، میلی ثانیه و ثانیه برای تشخیص رسیدن به یک زمان مشخص پس از لحظه ای خاص
- توابع Elapsed بر حسب میکروثانیه، میلی ثانیه و ثانیه برای تعیین زمان سپری شده از لحظه ای خاص
- توابع Left بر حسب میکروثانیه، میلی ثانیه و ثانیه برای تعیین زمان باقیمانده تا رسیدن به زمانی خاص
- تابع Interval برای اندازه گیری دوره زمانی 
- تابع Span برای تعیین بازه زمانی بین دو تیک بر حسب میکروثانیه، میلی ثانیه و ثانیه 

## چگونه استفاده کنید
- مخزن را کلون کرده و فایل ها را به پروژه خود اضافه کنید.
- [تنظیمات ماژول](#تنظیمات-ماژول) را در فایل 'chrono_config.h' تعیین کنید.
- تیک لازم را در پروژه ایجاد کنید. (این تیک میتواند به صورت سخت افزاری و بوسیله یک تایمر و یا به صورت نرم افزاری ایجاد شود. توضیحات بیشتر در این مورد در مقاله [اندازه گیری زمان در نرم افزار نهفته](doc/%D8%A7%D9%86%D8%AF%D8%A7%D8%B2%D9%87%20%DA%AF%DB%8C%D8%B1%DB%8C%20%D8%B2%D9%85%D8%A7%D9%86%20%D8%AF%D8%B1%20%D9%86%D8%B1%D9%85%20%D8%A7%D9%81%D8%B2%D8%A7%D8%B1%20%D9%86%D9%87%D9%81%D8%AA%D9%87.md) ارایه شده است.)
- با فراخوانی تابع 'fChrono_Init' ماژول کرونو را راه اندازی کنید. این تابع سه ورودی دارد. ورودی اول مشخص میکند که حداکثر مقدار تیک چقدر است (بدین معنی که تیک پس از رسیدن به این مقدار ریست شده و مجدد از صفر شروع میشود). ورودی دوم واحد زمانی هر تیک را مشخص میکند (این عدد مشخص میکند که هر تیک برابر چند نانوثانیه است). و ورودی سوم هم اشاره گر به متغیر تیک است و یا اشاره گر به تابعی است که مقدار تیک را برمیگرداند.
- حالا ماژول آماده استفاده است.
- در فایل 'chrono.c' اطلاعات کامل در مورد نحوه استفاده از ماژول نوشته شده است.
- در زیر نحوه استفاده از توابع مختلف ماژول کرونو  در مقیاس میکروثانیه نوشته شده است. نحوه استفاده از بقیه مقیاس های زمانی مشابه یکدیگر است.
```c

//Example 1: Initialize module
//tickValue is pointer to 32bit register that contain tick value
//tickValue increment every us. so, each tick value is 1000 ns
//top value of tick is maximum of uisgned 32bit variable that is 0xFFFFFFFF
fChrono_Init(0xFFFFFFFF, 1000, tickValue);

//Example 2: Generate Delay
fChrono_DelayUs(1);

//Example 3: Measure execution time of user code
sChrono myChrono; //create an instance of chrono
fChrono_Start(&myChrono); //start instance
//User code that it's execution time should be measured
//...
timeUs_t elapsedUs = fChrono_ElapsedUs(&myChrono);
printf("Code execution time is %u us\n", elapsedUs);

//Example 4: Show left time to a specified time
sChrono myChrono; //create an instance of chrono
fChrono_StartTimeoutUs(&myChrono, 10000); //start instance
while(1)
{
	printf("Left time is %u us\n", fChrono_LeftUs(&myChrono));
}

//Example 5: Check timeout
sChrono myChrono; //create an instance of chrono
fChrono_StartTimeoutUs(&myChrono, 10000); //start instance
while(1)
{
	if(fChrono_IsTimedOutUs(&myChrono) == true)
	{
		printf("10000us timeout is eached.\n");
		break;
	}
}

//Example 6: Measure interval of user code execution
sChrono myChrono; //create an instance of chrono
fChrono_Start(&myChrono); //start instance
while(1)
{
	timeUs_t interval = fChrono_IntervalUs(&myChrono);
    printf("Runtime interval: %f\n", interval);

	//User code that it's execution interval shuld be measured
	//...
}

//Example 7: Calculate timespan
tick_t startTick = fChrono_GetTick();
//User code
//...
tick_t endTick = fChrono_GetTick();
timeUs_t diffUs = fChrono_TimeSpanUs(startTick, endTick);
printf("Timespan is %f us\n", diffUs);

```

## تنظیمات ماژول
در فایل 'chrono_config.h' تنظیماتی برای استفاده از ماژول وجود دارد.
- باید مشخص شود که تیک بوسیله متغیر قابل دسترسی است یا تابع
- نوع متغیر استفاده شده برای تیک باید مشخص شود که هر یک از انواع primitive از جنس unsigned قابل استفاده است. این مقدار بر اساس این تعیین میشود که اندازه تیک موجود در سیستم چند بیت است.
- نوع متغیر استفاده شده برای زمان باید مشخص شود که هر یک از انواع primitive از جنس unsigned و یا float و double قابل استفاده است. این نوع برای هر یک از مقیاس های ثانیه، میلی ثانیه و میکروثانیه به طور جداگانه باید مشخص شود.

 >[! ] تنظیمات تیک بوسیله متغیر یا تابع
 > در صورتی که مقدار تیک تماما با استفاده از یک متغیر ساخته شده باشد و بتوان اشاره گر آن متغیر را به ماژول کرونو معرفی کرد، باید از نوع متغیر استفاده کرد. مانند استفاده از یک تایمر هم اندازه با سایز تیک برای تولید آن
 > در صورتی که مقدار تیک در یک متغیر واحد در دسترس نباشد، باید از تابع بدین منظور استفاده کرد. به عنوان مثال اگر از دو تایمر 16 بیتی به صورت cascade برای ایجاد یک تیک 32 بیتی استفاده شود، در این صورت 16 بیت بالا و پایین تیک در دو حافظه متفاوت ذخیره شده اند و به صورت یک متغیر 32 بیتی قابل دسترس نیستند. بلکه باید بوسیله یک تابع این دو مقدار 16 بیتی در کنار هم قرار گرفته و یک متغیر 32 بیتی را برگرداند. 


 >[! ] تنظیمات نوع متغیر زمان
 > از آنجایی که ماژول کرونو برای نرم افزار نهفته توسعه داده شده و با توجه به محدودیت منابع موجود در نرم افزار نهفته (سرعت پردازش و حافظه رم) و به جهت امکان مدیریت مصرف منابع، امکانی برای تعیین نوع متغیر استفاده شده برای ذخیره زمان فراهم شده است.
 > کاربر با توجه به سایز تیک، حداکثر مقدار آن و همچنین مقدار زمان هر تیک بر حسب نانوثانیه (که این پارامترها به عنوان ورودی به تابع Init داده می شود)، میتواند محاسبه کند که حداکثر زمان قابل اندازه گیری توسط ماژول کرونو چقدر است. (البته این مقدار را خود ماژول کرونو هم محاسبه کرده و میتوان از طریق API ها مقدار آن را خواند) بر اساس این مقدار، کاربر می تواند تعیین کند که از چه نوع متغیر Primitive برای ذخیره زمان می خواهد استفاده کند. این نوع هم به حداکثر مقدار قابل اندازه گیری و هم به میزان دقت مورد نیاز کاربر بستگی دارد. ماژول کرونو از این نوع متغیر هم برای ذخیره سازی زمان و هم برای محاسبه زمان استفاده می کند. بنابراین هم در میزان حافظه مصرف شده و هم در سرعت انجام محاسبات زمان و cast کردن ها تاثیر دارد.
## شروع استفاده
برای کلون کردن ماژول کرونو میتوانید از دستور زیر استفاده کنید : 
```bash
git clone <ssh code>
```
## وابستگی ها
ماژول کرونو تنها به کتابخانه های پایه زیر نیاز دارد : 
- stdint
- stdbool
- stddef
## پلتفرم های پشتیبانی شده
ماژول کرونو در زبان های ++C/C قابل استفاده بوده و به هیچ میکروکنترلر خاصی وابستگی ندارد.
## مثال ها
در مخزن جداگانه ای به نام [example_chrono](https://github.com/faraabin/chrono-example) دو مثال برای تیک به صورت متغیر و تیک به صورت تابع وجود دارد. این مثال ها بر روی بورد Nucleo-L432KC و در محیط Keil نوشته شده است.
## مستندات
- در فولدر 'doc/html' فایل [راهنمای API](doc/html/index.html) موجود است.
- در ابتدای فایل c راهنمای کامل نحوه استفاده از ماژول کرونو نوشته شده است.
- مثال هایی برای استفاده از ماژول کرونو در مخزن جداگانه ای به نام 'chrono-example' موجود است.
- در فولدر 'doc' مقاله ای در مورد مبانی [اندازه گیری زمان در نرم افزار نهفته](doc/%D8%A7%D9%86%D8%AF%D8%A7%D8%B2%D9%87%20%DA%AF%DB%8C%D8%B1%DB%8C%20%D8%B2%D9%85%D8%A7%D9%86%20%D8%AF%D8%B1%20%D9%86%D8%B1%D9%85%20%D8%A7%D9%81%D8%B2%D8%A7%D8%B1%20%D9%86%D9%87%D9%81%D8%AA%D9%87.md) موجود است. 
## الزامات
- این ماژول برای کار نیاز به یک تیک دارد. این تیک میتواند : 
	- به صورت نرم افزاری ایجاد شود.
	- به صورت سخت افزاری و بوسیله یک تایمر 32 بیتی موجود در میکروکنترلر ایجاد شود.
	- به صورت سخت افزاری و بوسیله یک تایمر 16 بیتی و اینتراپت سرریز آن در میکروکنترلر ایجاد شود.
	- در صورت استفاده از SoC ها به صورت یک ماژوب شمارنده در بخش FPGA پیاده سازی شود.
## محدودیت ها
اندازه گیری زمان در این روش محدود به حداکثر زمانی است که مقدار متغیر یک بار سرریز می شود. به عنوان مثال اگر از یک شمارنده 32 بیتی استفاده شود و زمان هر تیک یک میکروثانیه باشد، این زمان حدود 71 ثانیه و در صورت استفاده از تیک  یک دهم میکروثانیه، این زمان حدود 7 ثانیه می شود. از آنجایی که در اکثریت قریب به اتفاق موارد، اندازه گیری زمانی نرم افزار در حد 
میکروثانیه و میلی ثانیه است، این محدودیت مشکل خاصی ایجاد نمی کند. برای اندازه گیری زمان های بیشتر معمولا دقت بالایی (در حد میکروثانیه) مدنظر نیست و از RTC استفاده می شود.



