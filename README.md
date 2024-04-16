# Windows Bundle 2.6 (!ВЫШЕЛ!)

[
![logo](https://github.meigo.live/snapshot.png)
](https://meigo.net/)

- [**Discord-сервер**](https://discord.gg/CzjhTt2XBz)
- [**Поддержать разработчика**](https://www.donationalerts.com/r/meigostudios)
- [**Пакет расширений для DevelNext**](https://github.com/meigoc/jppm-windows-ext/releases/)
- [**JPPM api-docs**](api-docs/README.md)

<svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-star-fill starred-button-icon d-inline-block mr-2">
    <path d="M8 .25a.75.75 0 0 1 .673.418l1.882 3.815 4.21.612a.75.75 0 0 1 .416 1.279l-3.046 2.97.719 4.192a.751.751 0 0 1-1.088.791L8 12.347l-3.766 1.98a.75.75 0 0 1-1.088-.79l.72-4.194L.818 6.374a.75.75 0 0 1 .416-1.28l4.21-.611L7.327.668A.75.75 0 0 1 8 .25Z"></path>
</svg>

## Changelog
```php
--- 2.7 ---
// Разработка начата! 2.7 будет обновлением которое пофиксит все баги и ошибки в старых и новых версиях.
[Add] Новый класс ProcessManager
О классе читать тут: https://github.com/meigoc/jppm-windows-ext/blob/main/api-docs/classes/bundle/windows/ProcessManager.md
[Fix] некоторые исправления

--- 2.6 ---
[Change] Изменена структура пакета
[Add] Новый класс WindowsTime для работы с часовыми поясами в Windows. Это является аналогом tzutil.exe в windows. Класс работает на версии ОС Windows 7 и выше!
[Add] WindowsTime::get() // Получить ID текущего часового пояса
[Add] WindowsTime::list() // Получить список всех ID часовых поясов
[Add] WindowsTime::set("Russian Standard Time") // Установить часовой пояс по ID (Например: Russian Standard Time)
[Add] WindowsTime::set_dstoff("Pacific Standard Time") // Суффикс _dstoff отключает корректировку перехода на летнее время для данного часового пояса (если применимо)
[Add] Новый класс WindowsServices для работы с службами в Windows.
[Add] WindowsServices::get("AnyTextID") // Получить информацию о службе Windows по ID
[Add] WindowsServices::getAll // Получить информацию о всех службах Windows 
[Add] WindowsServices::delete("AnyTextID") // Удалить службу Windows по ID
[Add] WindowsServices::set // Установить необходимые значения службе Windows по ID
[Add] WindowsServices::new // Создать службу Windows
[Add] Windows::disableMonitor() // Выключить монитор
[Add] Windows::LogOff() // Выход из системы. Останавливает все процессы, связанные с контекстом безопасности текущего пользователя, завершает его сеанс  и отображает диалоговое окно входа в систему.

--- 2.5 ---
[Change] изменена информация о пакете (скриншот ниже)
[Add] проверка обновлений
[Add] новый класс CPU
[Add] новый класс QuickAPI (только DFFI)
[Add] Встроен пакет DFFI
[Add] CPU::AddressWidth => 64
[Add] CPU::Architecture => 9
[Add] CPU::AssetTag => To Be Filled By O.E.M.
[Add] CPU::Caption => Intel64 Family 6 Model 158 Stepping 11
[Add] CPU::CpuStatus => 1
[Add] CPU::CreationClassName => Win32_Processor
[Add] CPU::CurrentClockSpeed => 3600
[Add] CPU::CurrentVoltage => 10
[Add] CPU::Description => Intel64 Family 6 Model 158 Stepping 11
[Add] CPU::DeviceID => CPU0
[Add] CPU::Level => 6
[Add] CPU::LoadPercentage => 7
[Add] CPU::Manufacturer => GenuineIntel
[Add] CPU::MaxClockSpeed => 3600
[Add] CPU::Name => Intel(R) Core(TM) i3-9100F CPU @ 3.60GHz
[Add] CPU::NumberOfCores => 4
[Add] CPU::NumberOfEnabledCore => 4
[Add] CPU::NumberOfLogicalProcessors => 4
[Add] CPU::PartNumber => To Be Filled By O.E.M.
[Add] CPU::PowerManagementSupported => FALSE
[Add] CPU::ProcessorId => BFEBFBFF000906EB
[Add] CPU::ProcessorType => 3
[Add] CPU::Role => CPU
[Add] CPU::SerialNumber => To Be Filled By O.E.M.
[Add] CPU::SocketDesignation => LGA1151
[Add] CPU::Status => OK
[Add] CPU::StatusInfo => 3
[Add] CPU::ThreadCount => 4
[Add] CPU::VirtualizationFirmwareEnabled => FALSE
[Add] CPU::VMMonitorModeExtensions => FALSE
[Add] QuickAPI::MakeScreenshot();
[Add] QuickAPI::GetCursorPos();
[Add] QuickAPI::SetCursorPos();
[Add] QuickAPI::MessageBoxA(); // только англ.символы

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
[Add] Windows::print() // Отправить файл на печать. Используется принтер по умолчанию. Необходимо наличие установленного пакета офиса.
[Add] Windows::getFileMeta() 
[Fix] Windows::getPrinter() // Функция работала некорректно

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
