---
date: 2013-01-30
categories: [it, program]
tags: [Notepad++, Текстовой редактор]
update: 2018-07-30
author: Anton Sergienko
author-email: anton.b.sergienko@gmail.com
license: CC BY 4.0
license-url: https://github.com/Harrix/harrix.dev/blob/main/LICENSE.md
permalink-source: https://github.com/Harrix/harrix.dev-articles-2013/blob/main/notepad-plus-plus-plugins/notepad-plus-plus-plugins.md
permalink: https://harrix.dev/ru/articles/2013/notepad-plus-plus-plugins/
lang: ru
---

# Плагины Notepad++

![Featured image](featured-image.svg)

Известный редактор Notepad++, возможности которого можно расширить дополнительными плагинами, о некоторых я и расскажу.

## Про Plugin Manager

Создатель Notepad++ выпилил Plugin Manager из программы несколько лет назад (пишу в 2018) из-за наличия рекламы в данном инструменте. Поэтому его нужно устанавливать отдельно с официального репозитория: <https://github.com/bruderstein/nppPluginManager/releases>:

![Plugin Manager](img/npp-plugin-manager.png)

_Рисунок 1 — Plugin Manager_

Рекомендую устанавливать x86 версию Notepad++, если хотите пользоваться плагинами, так как многие плагины не перестроены на x64 версию. Соответственно нужно выбирать версию `UNI` у nppPluginManager.

Из архива достаньте обе папки `plugins` и `updater`, скопируйте их в папку Notepad++ (у меня это `C:\Program Files (x86)\Notepad++`).

Перезапустите Notepad++ и менеджер плагинов у вас появится:

![Меню Plugin Manager](img/npp-plugin-manager-menu.png)

_Рисунок 2 — Меню Plugin Manager_

## TextFX

Очень полезный плагин, который шел в предыдущих средах предустановленным, а теперь его надо устанавливать дополнительно.

Идем в `Плагины` → `Plugin Manager` → `Show Plugin Manager`. Ищем там плагин `TextFX Characters` и его устанавливаем. Версии x64 на 2018 год нет и скорее всего не будет:

![Меню плагина TextFX](img/textfx.png)

_Рисунок 3 — Меню плагина TextFX_

Полный обзор смотрите в статье [Обзор плагина TextFX в Notepad++](https://github.com/Harrix/harrix.dev-articles-2013/blob/main/textfx/textfx.md)<!-- https://harrix.dev/ru/articles/2013/textfx/ -->.

## Сортировка чисел

~~NppColumnSort — позволяет отсортировать строки как числа.~~

Сортируйте числа встроенной функцией `Правка` → `Операции со строками` → `Сортировка по Возрастанию целых чисел`:

![Сортировка по возрастанию целых чисел](img/sorting.png)

_Рисунок 4 — Сортировка по возрастанию целых чисел_

Пример текста:

```text
5
1
10
```

Данный текст будет отсортирован так:

```text
1
5
10
```

## Compare

Плагин для сравнения файлов.

Идем `Плагины` → `Plugin Manager` → `Show Plugin Manager`. Ищем там плагин `Compare` и его устанавливаем:

![Плагин Compare](img/compare_01.png)

_Рисунок 5 — Плагин Compare_

При выборе данного пункта меню происходит сравнение файлов:

![Сравнение файлов с помощью плагина Compare](img/compare_02.png)

_Рисунок 6 — Сравнение файлов с помощью плагина Compare_
