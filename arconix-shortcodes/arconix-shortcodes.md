---
date: 2013-02-20
categories: [it, web]
tags: [Wordpress]
update: 2018
author: Anton Sergienko
author-email: anton.b.sergienko@gmail.com
license: CC BY 4.0
license-url: https://github.com/Harrix/harrix.dev/blob/main/LICENSE.md
permalink-source: https://github.com/Harrix/harrix.dev-articles-2013/blob/main/arconix-shortcodes/arconix-shortcodes.md
permalink: https://harrix.dev/ru/articles/2013/arconix-shortcodes/
lang: ru
---

# Обзор плагина Arconix Shortcodes для WordPress

![Featured image](featured-image.svg)

Малопопулярный плагин с шорткодами был выбран мной из ряда других в первую очередь простотой и красивыми по умолчанию элементами без ядовитых цветов, градиентов и так далее. Умеет делать кнопки, текстовые блоки, и другие красивые вещи.

- [Установка](#установка)
- [Текстовые блоки](#текстовые-блоки)
- [Спойлеры](#спойлеры)
- [Кнопки](#кнопки)
- [Вкладки](#вкладки)
- [Разное](#разное)
  - [Пояснение при наведении на слово — всплывающая подсказка (В общем объяснение чего-то)](#пояснение-при-наведении-на-слово--всплывающая-подсказка-в-общем-объяснение-чегото)
  - [Выделенный текст](#выделенный-текст)
  - [Ссылка на ваш сайт](#ссылка-на-ваш-сайт)
  - [Данные о текущем годе](#данные-о-текущем-годе)
  - [Ссылка на сайт Wordpress](#ссылка-на-сайт-wordpress)

**Update 2018.** Пользовался этим плагином, когда держал собственный сайт на Wordpress.

## Установка

Страница плагина на <https://wordpress.org/plugins/arconix-shortcodes/>.

Устанавливается, как и все остальные плагины. В режиме редактирования статьи справа внизу появляется следующая панель:

![Панель Arconix Shortcodes в WordPress](img/arconix-shortcode-list.png)

_Рисунок 1 — Панель Arconix Shortcodes в WordPress_

Как я понял, она носит лишь информативный характер. Ну что ж, пусть плагин и не удобен в использовании, зато результат его удобен. К тому же я лично многие из них повесил на плагин [AddQuicktag](https://wordpress.org/plugins/addquicktag/).

## Текстовые блоки

Ради них и взял фактически этот плагин:

```html
[box]Простой блок[/box]
```

![Простой блок](img/box.png)

_Рисунок 2 — Простой блок_

```html
[box color="blue"]Блок с синей заливкой[/box]
```

![Блок с синей заливкой](img/box-blue.png)

_Рисунок 3 — Блок с синей заливкой_

```html
[box color="green"]Блок с зеленой заливкой[/box]
```

![Блок с зеленой заливкой](img/box-green.png)

_Рисунок 4 — Блок с зеленой заливкой_

```html
[box color="grey"]Блок с серой заливкой[/box]
```

![Блок с серой заливкой](img/box-grey.png)

_Рисунок 5 — Блок с серой заливкой_

```html
[box color="red"]Блок с красной заливкой[/box]
```

![Блок с красной заливкой](img/box-red.png)

_Рисунок 6 — Блок с красной заливкой_

```html
[box color="tan"]Блок с дубильной заливкой[/box]
```

![Блок с дубильной заливкой](img/box-tan.png)

_Рисунок 7 — Блок с дубильной заливкой_

```html
[box color="yellow"]Блок с желтой заливкой[/box]
```

![Блок с желтой заливкой](img/box-yellow.png)

_Рисунок 8 — Блок с желтой заливкой_

```html
[box color="orange"]Блок с оранжевой заливкой[/box]
```

![Блок с оранжевой заливкой](img/box-orange.png)

_Рисунок 9 — Блок с оранжевой заливкой_

```html
[box style="alert"]Блок с предупреждением[/box]
```

![Блок с предупреждением](img/box-alert.png)

_Рисунок 10 — Блок с предупреждением_

```html
[box style="comment"]Блок с комментарием[/box]
```

![Блок с комментарием](img/box-comment.png)

_Рисунок 11 — Блок с комментарием_

```html
[box style="download"]Блок с загрузкой[/box]
```

![Блок с загрузкой](img/box-download.png)

_Рисунок 12 — Блок с загрузкой_

```html
[box style="info"]Блок с информацией[/box]
```

![Блок с информацией](img/box-info.png)

_Рисунок 13 — Блок с информацией_

```html
[box style="tip"]Блок с советом[/box]
```

![Блок с советом](img/box-tip.png)

_Рисунок 14 — Блок с советом_

```html
[box icon="fa-bolt" color="orange"]Блок с оранжевой заливкой и иконкой[/box]
```

![Блок с оранжевой заливкой и иконкой](img/box-orange-bolt.png)

_Рисунок 15 — Блок с оранжевой заливкой и иконкой_

Обратите внимание, что вы можете указать свою иконку в виде названия любой иконки из шрифта [Font-Awesome](https://fontawesome.com/icons).

## Спойлеры

Вот это полезная штука. Мне нравится:

```html
[toggle title="Спойлер"]Текст спойлера[/toggle]
```

<video controls autoplay loop muted src="img/toggle_01.mp4"></video>

img/toggle_01.mp4

https://github.com/Harrix/harrix.dev-articles-2013/blob/main/arconix-shortcodes/img/toggle_01.mp4

https://github.com/Harrix/harrix.dev-articles-2013/raw/main/arconix-shortcodes/img/toggle_01.mp4

![DELETE](img/toggle_01.delete.gif)

_Рисунок 16 — DELETE_

Или вот так нагляднее:

<video controls autoplay loop muted src="img/toggle_02.mp4"></video>

![DELETE](img/toggle_02.delete.gif)

_Рисунок 17 — DELETE_

## Кнопки

Кнопки, при нажатии на которые, производится переход на какую-то страницу.

Простая кнопка:

```html
[button url="http://blog.harrix.org" style="flat"]Кнопка[/button]
```

![Простая кнопка](img/button.png)

_Рисунок 18 — Простая кнопка_

Кнопка может быть нескольких цветов (`color = black, blue, green, grey, orange, pink, red, white`):

```html
[button url="http://blog.harrix.org" color="black" style="flat"]Кнопка[/button]
```

![Кнопка черная](img/button-black.png)

_Рисунок 19 — Кнопка черная_

```html
[button url="http://blog.harrix.org" color="blue" style="flat"]Кнопка[/button]
```

![Кнопка синяя](img/button-blue.png)

_Рисунок 20 — Кнопка синяя_

```html
[button url="http://blog.harrix.org" color="green" style="flat"]Кнопка[/button]
```

![Кнопка зеленая](img/button-green.png)

_Рисунок 21 — Кнопка зеленая_

```html
[button url="http://blog.harrix.org" color="grey" style="flat"]Кнопка[/button]
```

![Кнопка серая](img/button-grey.png)

_Рисунок 22 — Кнопка серая_

```html
[button url="http://blog.harrix.org" color="orange" style="flat"]Кнопка[/button]
```

![Кнопка оранжевая](img/button-orange.png)

_Рисунок 23 — Кнопка оранжевая_

```html
[button url="http://blog.harrix.org" color="red" style="flat"]Кнопка[/button]
```

![Кнопка красная](img/button-red.png)

_Рисунок 24 — Кнопка красная_

```html
[button url="http://blog.harrix.org" color="white" style="flat"]Кнопка[/button]
```

![Кнопка белая](img/button-white.png)

_Рисунок 25 — Кнопка белая_

Кнопки могут быть трех размеров (`size = small, medium, large`):

```html
[button url="http://blog.harrix.org" size="small" style="flat"]Кнопка[/button]
```

![Кнопка маленькая](img/button-small.png)

_Рисунок 26 — Кнопка маленькая_

```html
[button url="http://blog.harrix.org" size="medium" style="flat"]Кнопка[/button]
```

![Кнопка средняя](img/button-medium.png)

_Рисунок 27 — Кнопка средняя_

```html
[button url="http://blog.harrix.org" size="large" style="flat"]Кнопка[/button]
```

![Кнопка большая](img/button-large.png)

_Рисунок 28 — Кнопка большая_

Кнопки могут быть трех стилей (`style = classic, flat, clear`):

```html
[button url="http://blog.harrix.org" style="classic"]Кнопка[/button]
```

![Кнопка классическая](img/button-classic.png)

_Рисунок 29 — Кнопка классическая_

```html
[button url="http://blog.harrix.org" style="flat"]Кнопка[/button]
```

![Кнопка плоская](img/button-flat.png)

_Рисунок 30 — Кнопка плоская_

```html
[button url="http://blog.harrix.org" style="clear"]Кнопка[/button]
```

![Кнопка контурная](img/button-clear.png)

_Рисунок 31 — Кнопка контурная_

Страница может открываться либо в той же вкладке или в новой (`target = self, blank`).

В той же:

```html
[button url="http://blog.harrix.org" target="self" style="flat"]Кнопка[/button]
```

В другой вкладке:

```html
[button url="http://blog.harrix.org" target="blank" style="flat"]Кнопка[/button]
```

Все параметры могут сочетаться:

```html
[button url="http://blog.harrix.org" color="orange" size="large"]Кнопка[/button]
```

![Кнопка классическая, оранжевая и большая](img/button-orange-classic-large.png)

_Рисунок 32 — Кнопка классическая, оранжевая и большая_

```html
[button url="http://blog.harrix.org" color="black" size="small"
target="blank"]Кнопка[/button]
```

_Рис. Кнопка классическая, черная и маленькая_

![Кнопка классическая, черная и маленькая](img/button-black-classic-small.png)

_Рисунок 33 — Кнопка классическая, черная и маленькая_

## Вкладки

```html
[tabs] [tab title="Вкладка 1"] Первый блок информации [/tab] [tab title="Вкладка
2"] Второй блок информации [/tab] [tab title="Вкладка 3"] Третий блок информации
[/tab] [/tabs]
```

![Вкладки](img/tabs.png)

_Рисунок 34 — Вкладки_

## Разное

### Пояснение при наведении на слово — всплывающая подсказка (В общем объяснение чего-то)

```html
[abbr title="По моему скромному мнению"]ИМХО[/abbr]
```

<video controls autoplay loop muted src="img/abbr.mp4"></video>

![DELETE](img/abbr.delete.gif)

_Рисунок 35 — DELETE_

### Выделенный текст

```html
[highlight]текст[/highlight]
```

![Выделенный текст](img/highlight.png)

_Рисунок 36 — Выделенный текст_

### Ссылка на ваш сайт

```html
[site-link]
```

<video controls autoplay loop muted src="img/site-link.mp4"></video>

![DELETE](img/site-link.delete.gif)

_Рисунок 37 — DELETE_

### Данные о текущем годе

```html
[the-year before="©" start="2001" after="All Rights Reserved"]
```

![Данные о текущем годе](img/the-year.png)

_Рисунок 38 — Данные о текущем годе_

### Ссылка на сайт Wordpress

```html
[wp-link]
```

<video controls autoplay loop muted src="img/wp-link.mp4"></video>

![DELETE](img/wp-link.delete.gif)

_Рисунок 39 — DELETE_

Более подробную исходную документацию можете прочитать тут: <https://www.tychesoftwares.com/docs/docs/shortcodes/>.
