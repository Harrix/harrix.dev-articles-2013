---
date: 2013-05-05
categories: [it, programming]
tags: [Qt, C++ Builder, Qt Gui]
author: Anton Sergienko
author-email: anton.b.sergienko@gmail.com
license: CC BY 4.0
license-url: https://github.com/Harrix/harrix.dev/blob/main/LICENSE.md
permalink-source: https://github.com/Harrix/harrix.dev-blog-2013/blob/main/analog-align-alclient-in-qt/analog-align-alclient-in-qt.md
permalink: https://harrix.dev/ru/blog/2013/analog-align-alclient-in-qt/
lang: ru
---

# Аналог Align alClient в Qt Gui Application

![Featured image](featured-image.svg)

В свое время я много программировал в C++ Builder 6. Но потом перешел на Qt. И если пользуешься этой системой, то не видишь свойств alClient по расширению компонент на всё окно. В литературе предлагают использовать Layout, но при добавлении соответствующих компонент всё растягивается, но только в не растягиваемых Layout. Как быть?

Использую Qt Creator 2.7.0 и Qt 5.0.1.

Итак создаем `Qt Gui Application`:

![Создание Qt Gui Application](img/new-project.png)

_Рисунок 1 — Создание Qt Gui Application_

Далее в окнах или все по умолчанию оставляете (если ничего не знаете) или меняйте на то, что вам нужно.

Перейдите на форму:

![Переход на форму](img/form_01.png)

_Рисунок 2 — Переход на форму_

![Переход на форму](img/form_02.png)

_Рисунок 3 — Переход на форму_

Добавьте какие-нибудь компоненты. Например, `pushButton` и `textEdit`:

![Новые компоненты на форме](img/add.png)

_Рисунок 4 — Новые компоненты на форме_

Теперь щелкните где-нибудь на форме правой кнопкой и выберете `Lay out` → `Lay out Vertically`:

![Lay out Vertically](img/layout_01.png)

_Рисунок 5 — Lay out Vertically_

Можно выбрать любой вариант, который вам нравится:

![Разные варианты разметки](img/layout_02.png)

_Рисунок 6 — Разные варианты разметки_

Всё! Теперь все элементы расширены до общего окна. К тому же будут изменять свои размеры при изменении окна:

![Внешний вид разметки](img/layout_03.png)

_Рисунок 7 — Внешний вид разметки_

![Внешний вид разметки в скомпилированном приложении](img/layout_04.png)

_Рисунок 8 — Внешний вид разметки в скомпилированном приложении_

Кстати, отменить такую привязку можно в том же меню в виде подменю `Break Layout`.

А вот какой тут аналог `TPanel`? Используйте для этого `Frame`:

![Компонент Frame](img/frame_01.png)

_Рисунок 9 — Компонент Frame_

Но, даже если вы добавите что-нибудь туда, то при использовании `Layout` все пойдет наперекосяк:

![Высота компонента неправильная](img/frame_02.png)

_Рисунок 10 — Высота компонента неправильная_

Для этого поменяйте у `Frame` свойство минимальной высоты или ширины (в зависимости от случая):

![Минимальная высота Frame](img/frame_03.png)

_Рисунок 11 — Минимальная высота Frame_

И все заработает:

![Компонент Frame с правильной высотой](img/frame_04.png)

_Рисунок 12 — Компонент Frame с правильной высотой_
