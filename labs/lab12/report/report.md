---
## Front matter
title: "Отчет по лаборатоной работе №12"
subtitle: 
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

Изучить основы программирования в оболочке ОС UNIX. Научиться писать более
сложные командные файлы с использованиемлогических управляющих конструкций
и циклов.

# Задание
1. Написать командный файл, реализующий упрощённый механизм семафоров. Ко-
мандный файл должен втечение некоторого времени t1 дожидаться освобождения
ресурса,выдавая об этом сообщение,а дождавшись его освобождения,использовать
его в течение некоторого времени t2<>t1, также выдавая информацию о том, что
ресурс используется соответствующим командным файлом (процессом).Запустить
командный файл в одном виртуальномтерминале в фоновом режиме,перенаправив
его вывод в другой (> /dev/tty#,где # —номертерминала куда перенаправляется
вывод),в которомтакже запущен этотфайл,но не фоновом,а в привилегированном
режиме.Доработатьпрограммутак,чтобыимеласьвозможностьвзаимодействиятрёх
и более процессов.
2. Реализовать команду man с помощью командного файла.Изучите содержимое ката-
лога /usr/share/man/man1.В нем находятся архивытекстовых файлов,содержащих
справку по большинству установленных в системе программ и команд.Каждый архив
можнооткрытькомандойless сразужепросмотревсодержимоесправки.Командный
файлдолженполучатьввидеаргументакоманднойстрокиназваниекомандыиввиде
результата выдавать справку об этой команде или сообщение об отсутствии справки,
если соответствующего файла нет в каталоге man1.
3. Используя встроенную переменную $RANDOM,напишите командный файл,генерирую-
щий случайную последовательность букв латинского алфавита.Учтите,что $RANDOM
выдаёт псевдослучайные числа в диапазоне от 0 до 32767.



# Выполнение лабораторной работы

1. Задание 1. Написали скрипт, проверили работу (рис. [-@fig:001]) (рис. [-@fig:002])

![рис.1](/home/edstarikova/homework/study/2022/ОперационныеСистемы/os-intro/labs/lab12/report/image/9.jpg){ #fig:001 width=70% }
![рис.2](/home/edstarikova/homework/study/2022/ОперационныеСистемы/os-intro/labs/lab12/report/image/8.jpg){ #fig:002 width=70% }


2. Задание 2. Написали скрипт man (рис. [-@fig:003]) (рис. [-@fig:004]) (рис. [-@fig:005]) (рис. [-@fig:006]) (рис. [-@fig:007])
![рис.3](/home/edstarikova/homework/study/2022/ОперационныеСистемы/os-intro/labs/lab12/report/image/11.jpg){ #fig:003 width=70% }
![рис.4](/home/edstarikova/homework/study/2022/ОперационныеСистемы/os-intro/labs/lab12/report/image/5.jpg){ #fig:004 width=70% }
![рис.5](/home/edstarikova/homework/study/2022/ОперационныеСистемы/os-intro/labs/lab12/report/image/1.jpg){ #fig:005 width=70% }
![рис.6](/home/edstarikova/homework/study/2022/ОперационныеСистемы/os-intro/labs/lab12/report/image/2.jpg){ #fig:006 width=70% }
![рис.7](/home/edstarikova/homework/study/2022/ОперационныеСистемы/os-intro/labs/lab12/report/image/3.jpg){ #fig:007 width=70% }

3. Задание 3 (рис. [-@fig:008]) (рис. [-@fig:009])
![рис.8](/home/edstarikova/homework/study/2022/ОперационныеСистемы/os-intro/labs/lab12/report/image/6.jpg){ #fig:008 width=70% }
![рис.9](/home/edstarikova/homework/study/2022/ОперационныеСистемы/os-intro/labs/lab12/report/image/4.jpg){ #fig:009 width=70% }
# Выводы

Я изучила основы программирования в UNIX
