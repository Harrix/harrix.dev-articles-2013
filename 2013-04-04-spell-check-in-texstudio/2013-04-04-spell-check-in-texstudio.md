---
categories: [it, tex]
tags: [LaTeX, Проверка орфографии]
download: files/russian_english.zip
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
