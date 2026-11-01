ЗаборЧик — автономная версия для установки на Android

Файлы: index.html, manifest.webmanifest, sw.js, icon-192.png, icon-512.png.
Работает без интернета, шрифты системные.

1) Установка без APK (PWA)
   Выложите все файлы папки на хостинг по https (GitHub Pages, Netlify, Cloudflare Pages).
   Откройте адрес в Chrome на телефоне: меню ⋮ → «Установить приложение».

2) APK через PWABuilder (проще всего)
   Выложите на хостинг (пункт 1), откройте pwabuilder.com, вставьте адрес сайта,
   выберите Android и скачайте пакет. На телефоне разрешите установку из неизвестных источников.

3) APK через Capacitor (нужны Node.js и Android Studio)
   mkdir zaborchik && cd zaborchik
   npm init -y
   npm i @capacitor/core @capacitor/cli @capacitor/android
   npx cap init ЗаборЧик ru.zaborchik.app --web-dir www
   mkdir www  (положите сюда все файлы из этой папки)
   npx cap add android
   npx cap sync
   npx cap open android
   В Android Studio: Build → Build Bundle(s) / APK(s) → Build APK(s).
   Файл появится в android/app/build/outputs/apk/debug/app-debug.apk.

Экспорт JPEG: на телефоне откроется меню «Поделиться», на компьютере файл скачается.
