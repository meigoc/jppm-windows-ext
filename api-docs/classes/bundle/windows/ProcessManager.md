# ProcessManager

- **class** `ProcessManager` (`bundle\windows\ProcessManager`)
- **package** `windows`
- **source** `bundle/windows/ProcessManager.php`

---

#### Имя процесса

Примеры:
- **ProcessManager::StartTime('Notepad');** // Получение необходимого параметра по имени приложения (Notepad) <br>
- **ProcessManager::name('-id 6100');** // Получение необходимого параметра используя идентификатор процесса [PID] (-id 6100) <br>
Так-же имеется возможность передать объект процесса через конвейер в этот командлет. <br>
- **ProcessManager::Company('-InputObject <Process[]>');** <br>
($app)

#### Static Methods

- `ProcessManager ::`[`name($app)`](#method-name) - _Получить имя программы_
- `ProcessManager ::`[`StartTime($app)`](#method-starttime) - _Получить время запуска программы_
- `ProcessManager ::`[`CPU($app)`](#method-cpu) - _Получить нагруженность процесса_
- `ProcessManager ::`[`Company($app)`](#method-company) - _Получить издателя программы_
- `ProcessManager ::`[`MainWindowTitle($app)`](#method-mainwindowtitle) - _Получить заголовок главного окна_
- `ProcessManager ::`[`Path($app)`](#method-path) - _Получить путь к программе_
- `ProcessManager ::`[`Description($app)`](#method-description) - _Получить описание программы_
- `ProcessManager ::`[`WindowStyle($app)`](#method-windowstyle) - _Получить стиль окна_
