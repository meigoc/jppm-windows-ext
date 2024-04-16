# WindowsTime

- **class** `WindowsTime` (`bundle\windows\WindowsTime`)
- **package** `windows`
- **source** `bundle/windows/WindowsTime.php`

**Description**

Класс для работы с часовыми поясами в Windows. Это является аналогом tzutil.exe в windows. Класс работает на версии ОС Windows 7 и выше!

---

#### Static Methods

- `WindowsTime ::`[`get()`](#method-get) - _Получить ID текущего часового пояса_
- `WindowsTime ::`[`list()`](#method-list) - _Получить список всех ID часовых поясов_
- `WindowsTime ::`[`set()`](#method-set) - _Установить часовой пояс по ID (Например: Russian Standard Time)_
- `WindowsTime ::`[`set_dstoff()`](#method-set_dstoff) - _Суффикс _dstoff отключает корректировку перехода на летнее время для данного часового пояса (если применимо)_
---
# Static Methods

<a name="method-get"></a>

### get()
```php
WindowsTime::get(): string
```
Получить ID текущего часового пояса

---

<a name="method-list"></a>

### list()
```php
WindowsTime::list():
```
Получить список всех ID часовых поясов

---

<a name="method-set"></a>

### set()
```php
WindowsTime::set(string $arg): string
```
Установить часовой пояс по ID (Например: Russian Standard Time)

---

<a name="method-set_dstoff"></a>

### set_dstoff()
```php
WindowsTime::set_dstoff(string $arg): string
```
Суффикс _dstoff отключает корректировку перехода на летнее время для данного часового пояса (если применимо)
