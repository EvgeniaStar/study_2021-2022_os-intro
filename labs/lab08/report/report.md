---
## Front matter
title: "Отчет по лабораторной работ №8"
subtitle: "Дисциплина: операционные системы"
author: "Старикова Евгения Дмитриевна"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Познакомиться с операционной системой Linux.Получить практические навыки рабо-
ты с редактором vi,установленным по умолчанию практически во всех дистрибутивах.

# Задание

Задание 1. Создание нового файла с использованием vi
Задание 2. Редактирование существующего файла


# Выполнение лабораторной работы
## Задание 1
1. Вызываем vi и создаём файл hello.sh (рис. [-@fig:001])

![Название рисунка](/home/edstarikova/Изображения/sceen.jpg){ #fig:001 width=70% }
1. Нажмите клавишу i и вводите текст.
1. Нажимаем клавишу "Esc" чтобы перейти в командный режим после ввода текста.
1. Нажимаем : для перехода в режим последней строки и внизу экрана видим приглашение
1. Нажимаем "w"(записать) и  "q" (выйти), далее наживаем Enter для сохранения и завершения работы.
1. Делаем фыйл исполняемым.
## Задание 2

1. Вызовите vi на редактирование файла vi ~/work/os/lab06/hello.sh
1. Установите курсор в конец слова HELL второй строки.
1. ПерейдитеврежимвставкиизаменитенаHELLO.Нажмите Esc длявозвратавкомандый режим.
1. Установите курсор на четвертую строку и сотрите слово LOCAL.
1. Перейдите в режим вставки и наберите следующий текст: local, нажмите Esc для
возврата в командный режим.
1. Установитекурсорнапоследнейстрокефайла.Вставьтепосленеёстроку,содержащую
следующийтекст: echo $HELLO.
1. Нажмите Esc для перехода в командный режим.
1. Удалите последнюю строку.
1. Введите команду отмены изменений u для отмены последней команды.
1. Введитесимвол : дляпереходаврежимпоследнейстроки.Запишитепроизведённые
изменения и выйдите из vi.

# Выводы

Приобрела навыки использования редактора vi

# Контрольные вопросы

