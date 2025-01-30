---
title: استفاده از کتابخانه leafletjs
---

###  مقدمه

برای نمایش یک نقشه و استفاده از API بهترین راه استفاده از کتابخانه ای است که با توجه به درخواست کاربر اقدام به ارسال درخواست به سرویس دهنده و نمایش خروجی نماید. یکی از بهترین کتابخانه های نمایش نقشه leafletjs است که از خروجی های تصویر محور یا رستری پشتیبانی می کند.
توجه داشته باشید leafletjs یک کتابخانه جاوا اسکریپت است و در وب و بعضی از سیستم عامل های موبایل قابلیت پیاده سازی را دارد.

## هدر صفحه
اگر قصد دارید از فایل های هاست شده در سرویس های توزیع محتوا استفاده نمایید این دو فایل که شامل کتابخانه و فایل های استایل است را به هد قالب HTML خود اضافه کنید
```html
<link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css" integrity="sha256-p4NxAoJBhIIN+hmNHrzRCf9tD/miZyoHS5obTRR9BMY=" crossorigin="" />
<script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js" integrity="sha256-20nQCchB9co0qIjJZRGuk2/Z9VM+kNiyxNV1lvTlZBo=" crossorigin=""></script>
```
سپس در بخش body صفحه به شرح زیر کد ها را قرار دهید

```html
<div id="map" style="height:89.5%;"></div>
    <script>
        //<![CDATA[
        var map = L.map('map').setView([35.69975547249546, 51.33803292808358], 14);
        L.control.scale({ imperial: false }).addTo(map);
        L.tileLayer('http://memaps.ir/hot/{z}/{x}/{y}.png', {
            attribution: '&copy; <a href="http://www.openstreetmap.org/copyright">OpenStreetMap</a> | <a href="https://parspack.com">استوار بر روی راهکارهای ابری پارس‌پک</a> ',
            maxZoom: 21,
            maxNativeZoom: 20
        }).addTo(map);


        var hash = L.hash(map)
        //]]>
    </script>
```
