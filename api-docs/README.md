#### **English** / [Русский](README.ru.md)

---

## windows
> version 2.7 (beta), created by JPPM.
> ⚠️ Api-docs новых классов находится в разработке!

Пакет для взаимодействия с API Windows

### Install
**JPPM:**
```php
jppm add windows@git+https://github.com/meigoc/jppm-windows-ext
```
**DevelNext:**
```php
// Файл:
[1] Скачайте пакет (.dnbundle).
[2] Перейдите во вкладку "Проект" на панели рядом с формами и модулями.
[3] Перейдите в "Пакеты"
[4] Нажмите кнопку "Добавить пакет из файла"
[5] Выберите пакет (.dnbundle).
[6] Готово.
// Используя ссылку:
[1] Скачайте пакет (.dnbundle).
[2] Перейдите во вкладку "Проект" на панели рядом с формами и модулями.
[3] Перейдите в "Пакеты"
[4] Нажмите кнопку "Добавить пакет по URL"
[5] Введите ссылку "https://github.com/meigoc/jppm-windows-ext/releases/download/2.7-beta/windows-2.7.dnbundle"
[6] Готово!
```
- [`У меня есть своя сборка DevelNext`](developers/install.md)- _Нажми сюда, если ты являешься разработчиком/создателем сборки (модификации) DevelNext и желаешь встроить пакет Windows прямо в DevelNext._

### API
**Classes**

#### `bundle\windows`

- [`COM`](classes/bundle/windows/COM.md)- _Класс для работы с COM-портами_
- [`Lan`](classes/bundle/windows/Lan.md)- _Local Area Network_
- [`Metadata`](classes/bundle/windows/Metadata.md)
- [`Prepare`](classes/bundle/windows/Prepare.md)- _Класс позволяет создавать подготовленные запросы (как в PDO)._
- [`Registry`](classes/bundle/windows/Registry.md)- _Класс для работы с реестром Windows_
- [`Startup`](classes/bundle/windows/Startup.md)- _Класс содержит функции для работы с автозапуском_
- [`Task`](classes/bundle/windows/Task.md)
- [`Windows`](classes/bundle/windows/Windows.md)
- [`WindowsException`](classes/bundle/windows/WindowsException.md)- _Класс исключения, выбрасываемого функциями пакета Windows_
- [`WindowsScriptHost`](classes/bundle/windows/WindowsScriptHost.md)- _Методы класса позволяют вызывать функции API Windows, выполнять системные скрипты_
- [`WindowsServices`](classes/bundle/windows/WindowsServices.md)- _Класс для работы с службами в Windows_
- [`WindowsTime`](classes/bundle/windows/WindowsTime.md)- _Класс для работы с часовыми поясами в Windows. Это является аналогом tzutil.exe в windows. Класс работает на версии ОС Windows 7 и выше!_
- [`Wlan`](classes/bundle/windows/Wlan.md)- _Wireless lan_
- [`ProcessManager`](classes/bundle/windows/ProcessManager.md)- _Класс для работы с процессами (управление программами)_

#### `bundle\windows` (другое)

- [`CPU`](classes/bundle/windows/CPU.md)- _Класс для работы с CPU_
- [`VideoDriver`](classes/bundle/windows/VideoDriver.md)- _Класс для работы с VideoDriver_
- [`OS`](classes/bundle/windows/OS.md)- _Класс для работы с OS_

#### `bundle\windows\result`

- [`abstractItem`](classes/bundle/windows/result/abstractItem.md)
- [`abstractResult`](classes/bundle/windows/result/abstractResult.md)
- [`comItem`](classes/bundle/windows/result/comItem.md)
- [`lanAdapter`](classes/bundle/windows/result/lanAdapter.md)
- [`registryItem`](classes/bundle/windows/result/registryItem.md)
- [`registryResult`](classes/bundle/windows/result/registryResult.md)
- [`startupItem`](classes/bundle/windows/result/startupItem.md)
- [`taskItem`](classes/bundle/windows/result/taskItem.md)- _Экземпляр данного класса содержит информацию об одном процессе_
- [`taskResult`](classes/bundle/windows/result/taskResult.md)- _Экземпляр класса содержит список процессов, который был сформирован в одном из методов класса Task_
- [`wlanInterface`](classes/bundle/windows/result/wlanInterface.md)
- [`wshResult`](classes/bundle/windows/result/wshResult.md)
