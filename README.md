# Поддержка JPPM будет добавлена тогда, когда поднимут JPPM!

[
![logo](https://github.meigo.live/snapshot.png)
](https://meigo.net/)

- [**Пакет расширений для DevelNext**](https://github.com/meigoc/jppm-windows-ext/releases/)

## Changelog
```php
--- 2.5 ---
// ВСЕ ЕЩЁ РАЗРАБАТЫВАЕТСЯ, ТО ЧТО СДЕЛАНО НИЖЕ ЭТО ДОБАВЛЕНО В БЕТА-ВЕРСИЮ, КАЧАТЬ ТУТ: https://github.com/meigoc/jppm-windows-ext/releases/tag/2.5-beta
[Add] Новый класс QuickAPI (только DFFI)
[Add] QuickAPI::MakeScreenshot();
[Add] QuickAPI::GetCursorPos();

--- 2.4 ---
[Del] OS::getArchitecture() // уже существует + данный метод оказался не рабочий
[Change] изменена информация о пакете (скриншот ниже)
[Add] новый класс VideoDriver
[Add] VideoDriver::getName() // Получить полное название видеокарты
[Add] VideoDriver::BitsPerPixel() // Получить биты на пиксели
[Add] VideoDriver::CurrentHorizontalResolution() // Получить горизонтальное разрешение экрана
[Add] VideoDriver::CurrentVerticalResolution() // Получить вертикальное разрешение экрана
[Add] VideoDriver::getDriverDate() // Получить дату драйвера
[Add] VideoDriver::getDriverVersion() // Получить версию драйвера
[Add] VideoDriver::getCurrentRefreshRate() // Получить герцовку монитора
[Add] VideoDriver::getMinRefreshRate() // Получить минимальную герцовку монитора
[Add] VideoDriver::getMaxRefreshRate() // Получить максимальную герцовку монитора
[Add] VideoDriver::getStatus() // Получить статус видеокарты (например: OK)
[Add] VideoDriver::getVideoModeDescription() // Получить описание видеокарты
[Add] VideoDriver::getCurrentNumberOfColors() // Получить текущее кол-во цветов

--- 2.3 ---
[Change] Изменена информация пакета .dnbundle
[Add] Класс OS
[Add] OS::getManufacturer() // Производитель ОС
[Add] OS::getArchitecture() // (МОЖЕТ НЕ РАБОТАТЬ!)
[Add] OS::getRegisteredUser() // Почта аккаунта Microsoft
[Add] OS::getPortableOperatingSystem() // Является ли система портативной (true/false)
[Add] OS::getInstallDate() // Дата установки
[Add] OS::getBuildNumber() // Номер сборки
[Add] OS::getFullName() // Полное имя, например: Майкрософт Windows 11 Pro
[Add] OS::getName() // Краткое имя, например: Windows 11

--- 2.2 ---
?

--- 2.1.1 ---
[Add] Windows::getSystemDrive()
Migrate to jppm

--- 2.1 ---
[Add] Windows::reboot()
[Add] Windows::shutdown()
[Add] Windows::pressKey()
[Add] Windows::getKeyboardLayoutName()
[Add] Windows::getKeyboardLayout()

--- 1.3 ---
[Add] Windows::runAsAdmin()
[Add] Windows::requireAdmin()
[Add] Windows::setDate()
[Add] Windows::setTime()
[Add] Windows::getUsers()
[Fix] Startup::getList() - Возвращает элементы автозагрузки для всех пользователей, а не только для текущего
[Fix] Мелкие исправления

--- 1.2 ---
[Add] Class COM
[Add] Windows::getTemperature()
[Fix] Bug fixes

--- 1.1 ---
[Change] Создана подробная документация
[Change] Disable WMIC cache
[Add] Windows::getBatteryTimeRemaining()
[Add] Windows::getBatteryPercent()
[Add] Windows::getBatteryVoltage()
[Add] Windows::isBatteryCharging()
[Add] Windows::setBrightnessLevel()
[Add] Windows::getBrightnessLevel()
[Add] Windows::setVolumeLevel()
[Add] Windows::getVolumeLevel()
[Add] Windows::setMute()
[Add] Windows::getMute()
[Add] Windows::getRAM()
[Add] Windows::getTotalRAM()
[Add] Windows::getBIOS()
[Add] Windows::getPrinter()

--- 1.0 ---
[Change] Изменена функция обращения к системному API 
[Change] Функции для работы с реестром (regRead, regSub, regDelete, regAdd) перемещены в отдельный класс Registry
[Change] Функции для работы с автозапуском (startupAdd, startupDelete, startupCheck, startupGet) перемещены в отдельный класс Startup
[Change] Функции для работы с процессами (getTaskList, taskKill, taskExists) перемещены в отдельный класс Task
[Fix] Windows::getDriveSerial() возвращал некорректное значение
[Add] Работа с lnk ярлыками Windows::createShortcut(), Windows::getShortcutTarget()
[Del] Удалены из ресурсов все скрипты и сторонние утилиты
[Del] Windows::getProductKey() - работала не на всех системах
[Del] Windows::setVolume() - работала не на всех системах
[Del] Windows::setBrightness() - работала не на всех системах
[Del] Windows::getInstalledSoftware()
[Del] Windows::emptyBin()
[Del] Windows::scanNetwork()
[Del] Windows::getInstallTime()
[Del] WindowsScriptHost::jScript()

--- 0.5 ---
[Change] Модуль переделан в пакет расширений
[Add] Встроена утилита nircmd, что позволило расширить функционал
[Add] Windows::getArch()
[Add] Windows::scanNetwork()
[Add] Windows::expandEnv()
[Add] Windows::setVolume()
[Add] Windows::setBrightness()
[Add] Windows::emptyBin()
[Add] Windows::speak()

--- 0.4.0.3 ---
[Fix] Windows::regRead();

--- 0.4.0.2 ---
[Add] Windows::getAdmin();
[Fix] Windows::getMAC();
```

## Install package via jppm
```
jppm add windows@git+https://github.com/meigoc/jppm-windows-ext
```

## Build bundle
```
jppm bundle:build
```
