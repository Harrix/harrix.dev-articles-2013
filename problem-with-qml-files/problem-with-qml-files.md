---
date: 2013-03-21
categories: [it, programming]
tags: [Qt, QtQuick, QML]
author: Anton Sergienko
author-email: anton.b.sergienko@gmail.com
license: CC BY 4.0
license-url: https://github.com/Harrix/harrix.dev/blob/main/LICENSE.md
---

# Проблема с названием QML файлов в QtQuick 2

Недавно была обнаружена одна неприятная вещь с работой с Qt Quick 2. А именно с тем, что при создании дополнительного QML файла этот самый файл системой не виделся. В результате ошибка нашлась. Всё было в регистре букв в названии QML файла.

Допустим вы создаете простейшее QtQuick 2.0 в системе Qt 5.0.1 for Windows 32-bit. И создаете дополнительный QML файл как компонент.

**Название дополнительных файлов QML должно начинаться с большой буквы!**

То есть можно назвать файл `Hbutton.qml`, но при названии `hbutton.qml` система его не увидит и будет писать ошибку.
