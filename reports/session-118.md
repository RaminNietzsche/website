----------
title: گزارش جلسه ۱۱۸م گروه کاربران لینوکس مشهد
layout: page
author: Echo
published: 2012-10-11 10:40:00
meta: published by Echo on Thu, 10/11/2012 - 10:40
category: sessions
----------
جلسه ۱۱۸م گروه کاربران لینوکس مشهد در ساعت ۱۷ روز شنبه ۱۵ مهر ماه ۱۳۹۱، در محل
موقت برگذاری جلسات واقع در بلوار پیروزی برگذار شد.


<!--more-->


موضوعاتی که در این جلسه به آنها پرداخته شد عبارت بودند از:  
**۱. بررسی اخبار دنیای آزاد و متن باز توسط آرش موسوی**  
**۲. نکته خط فرمانی: «جستجو در لینوکس» توسط بیژن ابراهیمی**

جستجوی فرامین

  1. دستور type: از این دستور برای اطلاع از نوع دستوری که در محیط شل اجرا می‌شود، استفاده می‌شود. مثال:

$ type ls  
**ls is aliased to `ls color=auto'**

در این مثال مشخص می‌شود در واقع دستور ls در محیط فعلی الیاسی است که با اجرای
آن، دستور ls با پارامتر‌ رنگ جهت رنگی کردن خروجی اجرا می‌شود (جهت خوانایی
بیشتر).

  2. دستور which: مشخص‌می‌کند با اجرا شدن دستوری خاص، چه برنامه‌ای از روی دیسک اجرا می‌شود. مثال:

$ which ls  
**/bin/ls**

در اینجا مشخص می‌شود که فایل اجرایی دستور ls در چه مسیری قرار دارد

  3. دستور whereis: کارایی این دستور همانند دستور which است با این تفاوت که علاوه بر فایل‌های باینری، موقعیت فایل‌های دیگری همچون سورس‌ها و راهنما‌های مربوطه را نیز مشخص می‌کند. مثال:

$ whereis ls  
**ls: /bin/ls /usr/share/man/man1/ls.1.gz**

در اینجا علاوه بر موقعیت فایل باینری دستور ls، موقعیت فایل راهنمای این دستور
نیز بر روی دیسک مشخص می‌شود

جستجوی فایل‌ها

  1. دستور locate: ابزاری جهت پیدا کردن فایل‌ها بر روی دیسک باتوجه به نام فایل. مثال:

$ locate words  
**/usr/share/dict/words  
/usr/share/dict/words.predictionariescommon  
/usr/share/doc/pythonnevow/examples/files/words**

این دستور برای جستجو از فایلی که حاوی لیستی از فایل‌های موجود بر روی دیسک است
استفاده می‌کند. مزیت اینکار سرعت بسیار بالا در جستجوی فایل‌ها است. نقطه ضعف
این مکانیزم این است که این لیست به صورت روزانه تهیه می‌شود و شامل فایل‌هایی که
امروز ایجاد می‌شوند نمی‌شوند. برای رفع این مشکل، می‌توانید با دستور زیر، این
لیست را در مواقعی که به‌دنبال فایل‌های اخیرا ایجاد شده میگردید، به روز رسانی
نمایید (توجه داشته باشید که برای این منظور سنیاز به مجوز کاربر ریشه خواهید
داشت):

# updatedb

  2. دستور find: از این دستور برای جستجوی فایل به‌صورت سلسه‌مراتبی بر روی دیسک استفاده می‌شود. این دستور برخلاف دستور locate به صورت سلسله مراتبی تمامی فایل‌های موجود بر روی دیسک را پیمایش کرده و در صورت تائید الگوی درخواستی، آن را نمایش می‌دهد. مثال:

$ find ~/ name mashhadlug  
**/home/USER/Documents/mashhadlug**

برای اطلاعات بیشتر به راهنمای این دستور مراجعه نمایید:

$ man find

جستجوی فایل‌های یک برنامه

  1. dpkg search: گاهی اوقات نیاز خواهید داشت که بدانید فایل مشخصی بر روی دیسک متعلق به چه بسته‌ای بوده و به همراه چه بسته‌ای بر روی دیسک شما نصب شده است. برای این منظور می‌توانیم از دستور dpkg استفاده کنیم. با استفاده از پارامتر search می‌توان بدنبال فایلی با الگوی مشخص در بسته‌های نصب شده بر روی سیستم استفاده کرد. مثال

$ dpkg search /usr/share/dict/words  
**diversion by dictionariescommon from: /usr/share/dict/words  
diversion by dictionariescommon to:
/usr/share/dict/words.predictionariescommon  
dictionariescommon, wamerican: /usr/share/dict/words**



  2. aptfile: این دستور برخلاف فوق در بسته‌هایی که بر روی سیستم نصب نشده‌اند نیز توانایی جستجو دارد. برای اطلاع از نحوه استفاده از این ابزار به راهنمای آن مراجعه نمائید

$ man aptfile

**۳. پخش فیلم: پوچی پتنت‌ها (قسمت دوم/آخر)**

قسمت آخر فیلم پوچی پتنت‌ها در این جلسه به نمایش گذاشته شد. در صورت علاقه
می‌توانید این فیلم را از وبسایت رسمی آن به آدرس
[patentabsurdity.com](http://patentabsurdity.com/watch.html) دانلود نمائید.
زیر نویس فارسی هم به زودی در همین خبر برای دانلود قرار داده خواهد شد.  
**۴. آموزش نصب توزیع اوبونتو توسط مهدی باقری**  
در این جلسه به درخواست اعضای تازه‌وارد، نصب اوبونتو ۱۲.۰۴ با تمرکز بر بخش
پارتیشن‌بندی توسط مهدی باقری ارائه شد

**۵. بحث آزاد**

این جلسه در ساعت ۱۹:۰۰ خاتمه یافت.
