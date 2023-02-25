---
date: 2013-04-04
categories: [it, tex]
tags: [LaTeX, Проверка орфографии]
download: https://github.com/Harrix/harrix.dev-blog-2013/raw/main/spell-check-in-texstudio/files/russian_english.zip
author: Anton Sergienko
author-email: anton.b.sergienko@gmail.com
license: CC BY 4.0
license-url: https://github.com/Harrix/harrix.dev/blob/main/LICENSE.md
url-src: https://github.com/Harrix/harrix.dev-blog-2013/blob/main/spell-check-in-texstudio/spell-check-in-texstudio.md
url: https://harrix.dev/ru/blog/2013/spell-check-in-texstudio/
lang: ru
---

# Проверка орфографии в TeXstudio

Для редактирования LaTex документов я использую связку [TeXstudio](https://www.texstudio.org/) и [MiKTeX](https://miktex.org/). Но вот проверки орфографии русского языка в TeXstudio по умолчанию нет.

Качаем архив русско-английского словаря [russian_english.zip](files/russian_english.zip).

Переходим в папку `dictionaries` в папке TexStudio. У меня это `C:\Program Files\texstudio\dictionaries` (раньше было `C:\Program Files (x86)\texstudio\dictionaries`). Если папки нет, то создайте её.

Распаковываем все файлы из архива в эту папку:

![Файлы словарей](img/dictionaries.png)

Перезапускаем программу TeXstudio.

Идем в настройки `Options` → `Configure TeXstudio…`:

![Настройки программы](img/options.png)

В разделе `Language Checking` в поле `Default Language` выбираем русский язык для проверки орфографии:

![Выбор языка](img/language-checking.png)

Теперь проверка орфографии появилась:

![Подчеркивание слов с ошибками](img/result.png)
