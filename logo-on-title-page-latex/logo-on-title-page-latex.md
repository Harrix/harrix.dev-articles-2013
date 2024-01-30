---
date: 2013-04-06
categories: [it, tex]
tags: [LaTeX]
author: Anton Sergienko
author-email: anton.b.sergienko@gmail.com
license: CC BY 4.0
license-url: https://github.com/Harrix/harrix.dev/blob/main/LICENSE.md
permalink-source: https://github.com/Harrix/harrix.dev-articles-2013/blob/main/logo-on-title-page-latex/logo-on-title-page-latex.md
permalink: https://harrix.dev/ru/articles/2013/logo-on-title-page-latex/
lang: ru
---

# Логотип на титульной странице в LaTeX

![Featured image](featured-image.svg)

Как поставить логотип на титульной странице в LaTeX документе макета article?

Подключите модуль `titlepic`:

```tex
\usepackage{titlepic}
```

В преамбуле пропишите свойства картинки вставляемой, например, так:

```tex
\titlepic{\includegraphics[width=8cm]{harrix.png}}
```

Вместо `harrix.png` вставьте свой рисунок.

Убедитесь, что стиль документа прописан с атрибутом `titlepage`:

```tex
\documentclass[titlepage]{article}
```

Вызовите стандартную функцию `\maketitle`.

И картинка появится.

Например для данного документа:

```tex
\documentclass[titlepage]{article}

\usepackage[T2A]{fontenc} % Поддержка русских букв
\usepackage[utf8]{inputenc} % Кодировка utf8
\usepackage[english, russian]{babel} % Языки: русский, английский
\usepackage{pscyr} % Нормальные шрифты

\usepackage{graphicx}
\usepackage{titlepic}

\titlepic{\includegraphics[width=8cm]{harrix.png}}

\title{HarrixMathLibrary v.3.0.0}
\author{А.,Б. Сергиенко}
\date{1 апреля 2013г.}

\begin{document}

\maketitle

Текст контента.

\end{document}
```

Результат будет такой:

![Титульная страница с логотипом](img/result.png)

_Рисунок 1 — Титульная страница с логотипом_
