---
## Front matter
title: "Отчет по лабороторной работе №11"
subtitle: "Дисциплина: Операционные системы"
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

Изучить основы программирования в оболочке ОС UNIX. Научится писать более
сложные командные файлы с использованиемлогических управляющих конструкций
и циклов.

# Задание

1. Используя команды getopts grep,написать командный файл,который анализирует
командную строку с ключами:
– -iinputfile —прочитатьданные из указанного файла;
– -ooutputfile —вывести данные в указанный файл;
– -pшаблон —указать шаблон для поиска;
– -C —различать большие и малые буквы;
– -n —выдавать номера строк.
а затем ищет в указанном файле нужные строки,определяемые ключом -p.
2. Написатьна языке Си программу,которая вводитчисло и определяет,являетсяли оно
больше нуля,меньше нуля или равно нулю.Затем программа завершается с помощью
функции exit(n),передавая информацию в о коде завершения в оболочку.Команд-
ный файл должен вызывать эту программу и,проанализировав с помощью команды
$?,выдать сообщение отом,какое число было введено.
3. Написать командный файл,создающий указанное число файлов,пронумерованных
последовательноот1до𝑁(например1.tmp,2.tmp,3.tmp,4.tmp ит.д.).Числофайлов,
которые необходимо создать,передаётся в аргументы командной строки.Этот же ко-
мандный файл должен уметь удалять все созданные им файлы (если они существуют).
4. Написать командный файл,который с помощью команды tar запаковываетв архив
все файлы в указанной директории.Модифицировать еготак,чтобы запаковывались
только те файлы,которые были изменены менее недели тому назад (использовать
команду find).



# Выполнение лабораторной работы


   1. Используя команды getopts grep, написала командный файл, который анализирует командную строку с ключами:

    -iinputfile — прочитать данные из указанного файла;
    -ooutputfile — вывести данные в указанный файл;
    -pшаблон — указать шаблон для поиска;
    -C — различать большие и малые буквы;
    -n — выдавать номера строк,
    а затем ищет в указанном файле нужные строки, определяемые ключом –p.
    Для данной задачи я создала файл prog1.sh и написала соответствующие скрипты (рис. [-@fig:001]) (рис. [-@fig:002])  (рис. [-@fig:003])

![рис.1](/home/edstarikova/homework/study/2022/ОперационныеСистемы/os-intro/labs/lab11/report/image/1.jpg){ #fig:001 width=70% }
![рис.2](/home/edstarikova/homework/study/2022/ОперационныеСистемы/os-intro/labs/lab11/report/image/7.jpg){ #fig:002 width=70% }
![рис.3](/home/edstarikova/homework/study/2022/ОперационныеСистемы/os-intro/labs/lab11/report/image/7.jpg){ #fig:003 width=70% }
Проверяем работу скрипта. Всё работает. (рис. [-@fig:004])
![рис.4](/home/edstarikova/homework/study/2022/ОперационныеСистемы/os-intro/labs/lab11/report/image/1.jpg){ #fig:004 width=70% }
 2. Написала на языке Си программу, которая вводит число и определяет, является ли оно больше нуля, меньше нуля или равно нулю. Затем программа завершается с помощью функции exit(n), передавая информацию в о коде завершения в оболочку. Командный файл должен вызывать эту программу и, проанализировав с помощью команды $?, выдать сообщение о том, какое число было введено. Для данной задачи я создал 2 файла: prog2.c и prog2.sh и написал соответствующие скрипты
(рис. [-@fig:005]) (рис. [-@fig:006]) (рис. [-@fig:007])
![рис.5](/home/edstarikova/homework/study/2022/ОперационныеСистемы/os-intro/labs/lab11/report/image/3.jpg){ #fig:001 width=70% }
![рис.6](/home/edstarikova/homework/study/2022/ОперационныеСистемы/os-intro/labs/lab11/report/image/8.jpg){ #fig:001 width=70% }
![рис.7](/home/edstarikova/homework/study/2022/ОперационныеСистемы/os-intro/labs/lab11/report/image/9.jpg){ #fig:001 width=70% }
Проверила работу. Всё работает. (рис. [-@fig:008])
![рис.8](/home/edstarikova/homework/study/2022/ОперационныеСистемы/os-intro/labs/lab11/report/image/3.jpg){ #fig:001 width=70% }

3. Написала командный файл, создающий указанное число файлов, пронумерованных последовательно от 1 до N (например 1.tmp, 2.tmp, 3.tmp, 4.tmp и т.д.). Число файлов, которые необходимо создать, передаётся в аргументы командной строки. Этот же командный файл должен уметь удалять все созданные им файлы (если они существуют). Для данной задачи я создал файл: prog3.sh (рис. [-@fig:009]) (рис. [-@fig:010])
![рис.9](/home/edstarikova/homework/study/2022/ОперационныеСистемы/os-intro/labs/lab11/report/image/4.jpg){ #fig:001 width=70% }
![рис.10](/home/edstarikova/homework/study/2022/ОперационныеСистемы/os-intro/labs/lab11/report/image/10.jpg){ #fig:001 width=70% }
Проверила работу. (рис. [-@fig:011])
![рис.11](/home/edstarikova/homework/study/2022/ОперационныеСистемы/os-intro/labs/lab11/report/image/4.jpg){ #fig:001 width=70% }
4. Написала командный файл, который с помощью команды tar запаковывает в архив все файлы в указанной директории. Модифицировала его так, чтобы запаковывались только те файлы, которые были изменены менее недели тому назад (использовать команду find). Для данной задачи я создала файл: prog4.sh (рис. [-@fig:012]) (рис. [-@fig:013])
![рис.12](/home/edstarikova/homework/study/2022/ОперационныеСистемы/os-intro/labs/lab11/report/image/5.jpg){ #fig:001 width=70% }
![рис.13](/home/edstarikova/homework/study/2022/ОперационныеСистемы/os-intro/labs/lab11/report/image/11.jpg){ #fig:001 width=70% }
Скрипт работает коректно. (рис. [-@fig:014]) (рис. [-@fig:015])
![рис.14](/home/edstarikova/homework/study/2022/ОперационныеСистемы/os-intro/labs/lab11/report/image/5.jpg){ #fig:001 width=70% }
![рис.15](/home/edstarikova/homework/study/2022/ОперационныеСистемы/os-intro/labs/lab11/report/image/6.jpg){ #fig:001 width=70% }





# Выводы

В ходе выполнения данной лабораторной работы я изучила основы программирования в оболочке ОС UNIX и научилась писать более сложные командные файлы с использованием логических управляющих конструкций и циклов.

