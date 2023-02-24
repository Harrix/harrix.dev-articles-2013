---
date: 2013-05-05
categories: [it, programming]
tags: [Qt, C++ Builder, Qt Gui]
author: Anton Sergienko
author-email: anton.b.sergienko@gmail.com
license: CC BY 4.0
license-url: https://github.com/Harrix/harrix.dev/blob/main/LICENSE.md
url-src: https://github.com/Harrix/harrix.dev-blog-2013/blob/main/analog-align-alclient-in-qt/analog-align-alclient-in-qt.md
url: https://harrix.dev/ru/blog/2013/analog-align-alclient-in-qt/
---

# Аналог Align alClient в Qt Gui Application

В свое время я много программировал в C++ Builder 6. Но потом перешел на Qt. И если пользуешься этой системой, то не видишь свойств alClient по расширению компонент на всё окно. В литературе предлагают использовать Layout, но при добавлении соответствующих компонент всё растягивается, но только в не растягиваемых Layout. Как быть?

Использую Qt Creator 2.7.0 и Qt 5.0.1.

Итак создаем `Qt Gui Application`:

![Создание Qt Gui Application](img/new-project.png)

Далее в окнах или все по умолчанию оставляете (если ничего не знаете) или меняйте на то, что вам нужно.

Перейдите на форму:

![Переход на форму](img/form_01.png)

![Переход на форму](img/form_02.png)

Добавьте какие-нибудь компоненты. Например, `pushButton` и `textEdit`:

![Новые компоненты на форме](img/add.png)

Теперь щелкните где-нибудь на форме правой кнопкой и выберете `Lay out` → `Lay out Vertically`:

![Lay out Vertically](img/layout_01.png)

Можно выбрать любой вариант, который вам нравится:

![Разные варианты разметки](img/layout_02.png)

Всё! Теперь все элементы расширены до общего окна. К тому же будут изменять свои размеры при изменении окна:

![Внешний вид разметки](img/layout_03.png)

![Внешний вид разметки в скомпилированном приложении](img/layout_04.png)

Кстати, отменить такую привязку можно в том же меню в виде подменю `Break Layout`.

А вот какой тут аналог `TPanel`? Используйте для этого `Frame`:

![Компонент Frame](img/frame_01.png)

Но, даже если вы добавите что-нибудь туда, то при использовании `Layout` все пойдет наперекосяк:

![Высота компонента неправильная](img/frame_02.png)

Для этого поменяйте у `Frame` свойство минимальной высоты или ширины (в зависимости от случая):

![Минимальная высота Frame](img/frame_03.png)

И все заработает:

![Компонент Frame с правильной высотой](img/frame_04.png)
