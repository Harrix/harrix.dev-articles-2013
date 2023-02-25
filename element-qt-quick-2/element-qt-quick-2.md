---
date: 2013-02-20
categories: [it, programming]
tags: [Qt, QtQuick, QML]
author: Anton Sergienko
author-email: anton.b.sergienko@gmail.com
license: CC BY 4.0
license-url: https://github.com/Harrix/harrix.dev/blob/main/LICENSE.md
url-src: https://github.com/Harrix/harrix.dev-blog-2013/blob/main/element-qt-quick-2/element-qt-quick-2.md
url: https://harrix.dev/ru/blog/2013/element-qt-quick-2/
lang: ru
---

# Как сослаться на элемент в папке с программой в QtQuick 2.0

![Featured image](featured-image.svg)

Работаю в основном с приложениями QtQuick 2.0 в виде, когда QML файлы через ресурсы зашиты в сам EXE файл. Вот пример построения базового приложения.

При этом доступ к элементам внутри QML идет через ресурсы. А как быть, если файл нужно считать из папки, а не из ресурсов?

Вроде решение и простое, но искал его долго. Итак, если файл в ресурсах, то обратиться легко, например:

```qml
Image {
  source: "qrc:/images/images/bk.png"
}
```

А если файл находится в папке с программой или в папках, но в папке, где программа есть? Например, видео в ресурсы всё не поместится и будет превышен размер EXE файла. Поступаем вот так:

```qml
Video {
  source: "file://video01.wmv"
}
```

То есть через структуру `file://`. Всё тоже самое относится к рисункам, аудио и так далее.
