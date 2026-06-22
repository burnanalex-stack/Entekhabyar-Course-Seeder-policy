# Privacy Policy — Entekhabyar Course Seeder

**Last updated: 2026-06-22**

This privacy policy describes how the **Entekhabyar Course Seeder** Chrome extension
("the extension") handles data. The extension is a tool for **authorized operators** who
sync the Islamic Azad University course catalog into the Entekhabyar service.

> **Not affiliated with Islamic Azad University.** The extension is an independent tool. It
> is not produced, endorsed by, or affiliated with Islamic Azad University (IAU) or the
> `eserv.iau.ir` portal. All university trademarks belong to their owners.

## What the extension reads but never sends off your device

- **IAU session cookies** (`JSESSIONID`, `cipxyz`): read locally only, to (a) detect whether
  you are logged into `eserv.iau.ir` and (b) make course-search requests within your existing
  session. These cookies are **never transmitted** to the Entekhabyar backend or any third party.
- **A CSRF token and term reference** captured from the IAU course-search page: stored locally
  on your device and used only to submit the course-search form to `eserv.iau.ir`.

## What the extension collects and sends to the Entekhabyar backend

Data is sent **only** to the Entekhabyar backend at `https://api.entekhabyar.com`, and only
when you actively unlock the extension or start a sync:

- **The 5-digit seeder code** you enter — sent to `/api/seeder/auth` once to verify you are an
  authorized operator and obtain a session token.
- **The operator/student name and student code** — read from the IAU course-search page and
  included in the sync so the catalog can be attributed to the correct department.
- **The parsed course catalog** — public course-offering data (course titles, codes, instructors,
  capacity, schedule, exam times, department names/codes) parsed from the portal's HTML.
- **Sync metadata** — academic term, university name, and per-sync statistics.

The extension does **not** send your IAU username, password, or session cookies to any server.

## What the extension stores on your device

The extension stores the following locally in `chrome.storage.local` (it stays on your computer):

- Your seeder session token and display name/role.
- The captured CSRF token and term reference (used only for the active session).
- Login-state flags and last-sync statistics.

You can clear all of this at any time by logging out within the extension or by removing the
extension from Chrome.

## How the data is used

Collected data is used **solely** to operate the course-sync feature: verifying authorized
access and updating the Entekhabyar course database. We do **not**:

- sell or rent your data,
- use it for advertising,
- share it with third parties beyond the Entekhabyar backend, or
- use it to determine creditworthiness or for lending purposes.

## Permissions

The extension requests only the permissions it needs: `cookies` (detect login state),
`storage` (local settings/token), `downloads` (save a JSON backup if the backend is
unreachable), `webNavigation` (show portal connection status), and host access to
`eserv.iau.ir`, `iau.ir`, and `api.entekhabyar.com`.

## Contact

Questions about this policy: **burnanalex@gmail.com**

---

# سیاست حریم خصوصی — افزونه انتخاب‌یار (Course Seeder)

**آخرین به‌روزرسانی: ۱۴۰۵/۰۴/۰۱ (2026-06-22)**

این سند توضیح می‌دهد که افزونه‌ی کروم **انتخاب‌یار (Entekhabyar Course Seeder)** چه داده‌هایی را
پردازش می‌کند. این افزونه ابزاری برای **ثبت‌کننده‌های مجاز** است که فهرست دروس دانشگاه آزاد اسلامی
را با سرویس انتخاب‌یار همگام‌سازی می‌کنند.

> **وابسته به دانشگاه آزاد اسلامی نیست.** این افزونه ابزاری مستقل است و هیچ وابستگی، تأیید یا ارتباطی
> با دانشگاه آزاد اسلامی یا سامانه‌ی `eserv.iau.ir` ندارد. تمام نشان‌های تجاری دانشگاه متعلق به مالکان
> آن‌هاست.

## آنچه افزونه می‌خواند اما هرگز از دستگاه شما خارج نمی‌کند

- **کوکی‌های نشست دانشگاه** (`JSESSIONID`, `cipxyz`): فقط به‌صورت محلی خوانده می‌شوند تا (الف) مشخص شود
  که شما وارد سامانه‌ی `eserv.iau.ir` شده‌اید و (ب) درخواست‌های جستجوی درس در همان نشست شما ارسال شود.
  این کوکی‌ها **هرگز** به سرور انتخاب‌یار یا هیچ شخص ثالثی ارسال نمی‌شوند.
- **توکن CSRF و شناسه‌ی ترم** که از صفحه‌ی جستجوی درس گرفته می‌شود: فقط روی دستگاه شما ذخیره می‌شود و
  تنها برای ارسال فرم جستجو به `eserv.iau.ir` استفاده می‌گردد.

## آنچه افزونه جمع‌آوری و به سرور انتخاب‌یار ارسال می‌کند

داده‌ها **فقط** به سرور انتخاب‌یار در آدرس `https://api.entekhabyar.com` و تنها هنگامی که شما افزونه را
باز می‌کنید یا همگام‌سازی را آغاز می‌کنید ارسال می‌شوند:

- **کد ۵ رقمی ثبت‌کننده** که وارد می‌کنید — برای تأیید مجاز بودن شما و دریافت توکن نشست.
- **نام و شماره‌ی دانشجویی ثبت‌کننده** — از صفحه‌ی جستجوی درس خوانده می‌شود تا فهرست دروس به گروه
  آموزشی درست نسبت داده شود.
- **فهرست دروس پردازش‌شده** — داده‌های عمومی دروس ارائه‌شده (عنوان درس، کد، استاد، ظرفیت، برنامه‌ی
  کلاسی، زمان امتحان، نام و کد گروه‌ها) که از HTML سامانه استخراج می‌شود.
- **اطلاعات همگام‌سازی** — ترم تحصیلی، نام دانشگاه و آمار هر همگام‌سازی.

افزونه **نام کاربری، رمز عبور یا کوکی‌های نشست** شما را به هیچ سروری ارسال نمی‌کند.

## آنچه روی دستگاه شما ذخیره می‌شود

افزونه موارد زیر را به‌صورت محلی در `chrome.storage.local` ذخیره می‌کند (روی رایانه‌ی شما می‌ماند):

- توکن نشست ثبت‌کننده و نام/نقش نمایشی شما.
- توکن CSRF و شناسه‌ی ترم (فقط برای نشست فعال).
- وضعیت ورود و آمار آخرین همگام‌سازی.

می‌توانید هر زمان با «خروج» در افزونه یا حذف افزونه از کروم، همه‌ی این داده‌ها را پاک کنید.

## نحوه‌ی استفاده از داده‌ها

داده‌های جمع‌آوری‌شده **تنها** برای کارکرد همگام‌سازی دروس استفاده می‌شوند: تأیید دسترسی مجاز و
به‌روزرسانی پایگاه داده‌ی انتخاب‌یار. ما داده‌های شما را **نمی‌فروشیم**، برای **تبلیغات** استفاده
نمی‌کنیم، با شخص ثالثی فراتر از سرور انتخاب‌یار به اشتراک نمی‌گذاریم و برای **اعتبارسنجی مالی یا
وام‌دهی** به کار نمی‌بریم.

## دسترسی‌ها

افزونه فقط دسترسی‌های موردنیاز را می‌خواهد: `cookies` (تشخیص وضعیت ورود)، `storage` (تنظیمات و توکن
محلی)، `downloads` (ذخیره‌ی نسخه‌ی پشتیبان JSON در صورت در دسترس نبودن سرور)، `webNavigation` (نمایش
وضعیت اتصال به سامانه) و دسترسی میزبان به `eserv.iau.ir`، `iau.ir` و `api.entekhabyar.com`.

## تماس

پرسش درباره‌ی این سیاست: **burnanalex@gmail.com**
