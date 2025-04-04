---
date: 2013-04-10
categories:
  - it
  - tex
tags:
  - LaTeX
author: Anton Sergienko
author-email: anton.b.sergienko@gmail.com
license: CC BY 4.0
license-url: https://github.com/Harrix/harrix.dev/blob/main/LICENSE.md
permalink-source: https://github.com/Harrix/harrix.dev-articles-2013/blob/main/double-index-in-latex/double-index-in-latex.md
permalink: https://harrix.dev/ru/articles/2013/double-index-in-latex/
lang: ru
---

# Двойной индекс в LaTeX

![Featured image](featured-image.svg)

Столкнулся с проблемой двойного индекса с применением `\bar`: вызывалась ошибка `Double subscript`. Заодно покажу и другие варианты отображения двойного индекса.

Итак, дан простейший код:

```tex
${\bar{a}_x}_y$
```

То есть нужно сделать двойной индекс для буквы с верхним подчеркиванием. При этом выдается ошибка в MiKTex по поводу двойного индекса, хотя без `\bar` двойной индекс проставляется замечательно.

На [http://tex.stackexchange.com](http://tex.stackexchange.com/questions/107846/double-subscript-with-bar) подсказали решение:

```tex
$\bar{a}{ { }_x}_y$
```

Что дает результат:

![Компилированный результат первого решения](img/result_01.png)

_Рисунок 1 — Компилированный результат первого решения_

Находил сам два костыля:

```tex
${\overline{a}_x}_y$

$\bar{a}_{x_y}$
```

Дают такой результат:

![Компилированный результат костылей](img/result_02.png)

_Рисунок 2 — Компилированный результат костылей_

И, как обещал, показываю другие примеры использования двойных индексов:

```tex
1. $ a_x{}_y $

2. $ a_{x_y} $

3. $ {a_x}_y $

4. $ a_{xy} $
```

Эти примеры дают такой результат:

![Компилированный результат использования двойных индексов](img/result_03.png)

_Рисунок 3 — Компилированный результат использования двойных индексов_
