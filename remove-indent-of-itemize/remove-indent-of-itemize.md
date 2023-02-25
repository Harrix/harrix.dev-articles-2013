---
date: 2013-04-06
categories: [it, tex]
tags: [LaTeX]
author: Anton Sergienko
author-email: anton.b.sergienko@gmail.com
license: CC BY 4.0
license-url: https://github.com/Harrix/harrix.dev/blob/main/LICENSE.md
url-src: https://github.com/Harrix/harrix.dev-blog-2013/blob/main/remove-indent-of-itemize/remove-indent-of-itemize.md
url: https://harrix.dev/ru/blog/2013/remove-indent-of-itemize/
lang: ru
---

# Как убрать отступ у списка itemize перед предыдущим текстом

![Featured image](featured-image.svg)

Ну, вопрос озвучен в названии статьи.

Допустим у нас есть такой документ, где через команду `\setlength` указан отступ между абзацами:

```tex
\documentclass[titlepage]{article}

\usepackage[T2A]{fontenc} % Поддержка русских букв
\usepackage[utf8]{inputenc} % Кодировка utf8
\usepackage[english, russian]{babel} % Языки: русский, английский
\usepackage{pscyr} % Нормальные шрифты

\setlength{\parskip}{0.3cm} % отступы между абзацами

\begin{document}

Первый абзац о всякой непонятной информации.

Описание списка:

\begin{itemize}
\item Первый пункт
\item Второй пункт
\item Третий пункт
\end{itemize}

\end{document}
```

Мы в итоге получим следующее:

![Проблема с отступом между списком и абзацем](img/list_01.png)

_Рисунок 1 — Проблема с отступом между списком и абзацем_

Как видим, между последней строкой нормального абзаца и списком слишком большой отступ. Надо исправлять. Для этого в преамбуле напишем:

```tex
\usepackage{enumitem}
\setlist{nolistsep, itemsep=0.3cm,parsep=0pt}
```

И наш документ примет вид:

```tex
\documentclass[titlepage]{article}

\usepackage[T2A]{fontenc} % Поддержка русских букв
\usepackage[utf8]{inputenc} % Кодировка utf8
\usepackage[english, russian]{babel} % Языки: русский, английский
\usepackage{pscyr} % Нормальные шрифты

\setlength{\parskip}{0.3cm} % отступы между абзацами

\usepackage{enumitem}
\setlist{nolistsep, itemsep=0.3cm,parsep=0pt}

\begin{document}

Первый абзац о всякой непонятной информации.

Описание списка:

\begin{itemize}
\item Первый пункт
\item Второй пункт
\item Третий пункт
\end{itemize}

\end{document}
```

![Исправленный отступ между абзацем и списком](img/list_02.png)

_Рисунок 2 — Исправленный отступ между абзацем и списком_

Что и требовалось.

Кстати, если добавить только это в преамбулу (не забывая про `\usepackage{enumitem}`), то получим:

```tex
\setlist{nolistsep}
```

![Список, где между элементами нет лишнего расстояния](img/list_03.png)

_Рисунок 3 — Список, где между элементами нет лишнего расстояния_

Если добавить только это в преамбулу, то получим:

```tex
\setlist{nolistsep, itemsep=0.3cm,parsep=0pt,leftmargin=1.5cm}
```

![Список, где между элементами расстояние определяется пользователем](img/result.png)

_Рисунок 4 — Список, где между элементами расстояние определяется пользователем_
