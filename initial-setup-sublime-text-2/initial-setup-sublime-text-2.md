---
date: 2013-01-05
categories: [it, program]
tags: [Sublime Text 2, Текстовой редактор, Установка]
related-id: sublime-text-2
author: Anton Sergienko
author-email: anton.b.sergienko@gmail.com
license: CC BY 4.0
license-url: https://github.com/Harrix/harrix.dev/blob/main/LICENSE.md
url-src: https://github.com/Harrix/harrix.dev-blog-2013/blob/main/initial-setup-sublime-text-2/initial-setup-sublime-text-2.md
permalink: https://harrix.dev/ru/blog/2013/initial-setup-sublime-text-2/
lang: ru
---

# Первоначальная настройка Sublime Text 2

![Featured image](featured-image.svg)

Сейчас всё больше становится популярным текстовой редактор `Sublime Text 2`. Но к сожалению «из коробки» редактор не очень приспособлен к работе. В статье описываются первоначальные настройки программы. Все примеры описываются для среды Windows.

## Где скачать программу

Стабильную версию программы можно скачать по адресу: <https://www.sublimetext.com/2>.

А последнюю рабочую версию можно скачать по адресу: <https://www.sublimetext.com/dev>.

После установки получим программу с таким внешним видом:

![Внешний вид программы](img/first-open.png)

_Рисунок 1 — Внешний вид программы_

## Где находятся настройки программы

Настройки программы делятся на несколько типов.

Общие настройки:

![Общие настройки](img/common-settings.png)

_Рисунок 2 — Общие настройки_

Настройки пользователя:

![Настройки пользователя](img/user-settings.png)

_Рисунок 3 — Настройки пользователя_

При сохранении изменений в этих файлах программа автоматически поменяет свои настройки.

## Многие файлы с русским текстом открываются с крякозябрами. Как исправить

Если мы откроем многие файлы с русским текстом, то получим следующее:

![Крякозябры](img/error.png)

_Рисунок 4 — Крякозябры_

Для этого исправим кодировку по умолчанию в настройках программы.

Идем в общие настройки `Preferences` → `Settings — Default`.

Находим там строки:

```json
// The encoding to use when the encoding can''t be determined automatically.
// ASCII, UTF-8 and UTF-16 encodings will be automatically detected.
"fallback_encoding": "Western (Windows 1252)",
```

Исправляем на такие:

```json
// The encoding to use when the encoding can''t be determined automatically.
// ASCII, UTF-8 and UTF-16 encodings will be automatically detected.
"fallback_encoding": "Cyrillic (Windows 1251)",
```

И сохраняем настройки `Ctrl` + `S`.

Теперь при открытии файлов с русским текстом всё будет отображаться корректно:

![Крякозябры исчезли](img/without-error.png)

_Рисунок 5 — Крякозябры исчезли_

## Установка Package Control

В дальнейшей работе вы скорее всего будете устанавливать дополнительные плагины. Для этого лучшего всего установить дополнительный менеджер пакетов `Package Control`:

Войдите в консоль. Для этого нажмите `Ctrl` + `Ё`:

![Консоль](img/console_01.png)

_Рисунок 6 — Консоль_

Введите в консоли строчку:

```python
import urllib2,os;pf='Package Control.sublime-package';ipp=sublime.installed_packages_path();os.makedirs(ipp) if not os.path.exists(ipp) else None;open(os.path.join(ipp,pf),'wb').write(urllib2.urlopen('http://sublime.wbond.net/'+pf.replace(' ','%20')).read())
```

Нажмите `Enter` и ждём, пока всё скачается:

![Процесс ожидания в консоли](img/console_02.png)

_Рисунок 7 — Процесс ожидания в консоли_

Перезапускаем программу и теперь в настройках в настройках у нас есть `Package Control`: `Preferences` → `Package Control`:

![Package Control](img/console_03.png)

_Рисунок 8 — Package Control_

![Package Control](img/console_04.png)

_Рисунок 9 — Package Control_

Теперь заходя в `Package Control` вы сможете устанавливать плагины для `Sublime Text 2` быстрее и проще.

Вроде с основными настройками справились. В начале статьи есть список статей данного блога по данной программе, в которых вы можете почерпнуть что-то полезное.
