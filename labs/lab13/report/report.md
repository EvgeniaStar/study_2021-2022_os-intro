---
## Front matter
title: "Отчет по лабораторной работе №13"
subtitle: "Дисциплина операционные системы"
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

Приобрести простейшие навыки разработки,анализа,тестирования и отладки при-
ложений в ОС типа UNIX/Linux на примере создания на языке программирования
С калькулятора с простейшими функциями.

# Задание


   1. В домашнем каталоге создайте подкаталог ~/work/os/lab_prog.
   2. Создайте в нём файлы: calculate.h, calculate.c, main.c. Это будет примитивнейший калькулятор, способный складывать, вычитать, умножать и делить, возводить число в степень, брать квадратный корень, вычислять sin, cos, tan. При запуске он будет запрашивать первое число, операцию, второе число. После этого программа выведет результат и остановится.
   3. Выполните компиляцию программы посредством gcc:
   * gcc -c calculate.c
   * gcc -c main.c
   * gcc calculate.o main.o -o calcul -lm
   * При необходимости исправьте синтаксические ошибки.
   * Создайте Makefile. Поясните в отчёте его содержание.
   * С помощью gdb выполните отладку программы calcul (перед использованием gdb исправьте Makefile ):

   4. Запустите отладчик GDB, загрузив в него программу для отладки
   5. Для запуска программы внутри отладчика введите команду run
   6. Для постраничного (по 10 строк) просмотра исходного код используйте команду list
   * Для просмотра строк с 12 по 15 основного файла используйте list с параметрами
   * Для просмотра определённых строк не основного файла используйте list с параметрами
   * Установите точку останова в файле calculate.c на строке номер 21
   * Выведите информацию об имеющихся в проекте точка останова
   * Запустите программу внутри отладчика и убедитесь, что программа остановится в момент прохождения точки останова
   * Отладчик выдаст информацию, а команда backtrace покажет весь стек вызываемых функций от начала программы до текущего места
   * Посмотрите, чему равно на этом этапе значение переменной Numeral. На экран должно быть выведено число 5
   * Сравните с результатом вывода на экран после использования команды
   * Уберите точки останова

   7. С помощью утилиты splint попробуйте проанализировать коды файлов calculate.c и main.c.



# Выполнение лабораторной работы

1. Создаём необходимые каталоги, в нем нужные файлы. (рис. [-@fig:001])

![рис.1](/home/edstarikova/homework/study/2022/ОперационныеСистемы/os-intro/labs/lab13/report/image/1.jpg){ #fig:001 width=70% }
2. Это будет примитивнейший калькулятор, способный складывать, вычитать, умножать и делить, возводить число в степень, брать квадратный корень, вычислять sin, cos, tan. При запуске он будет запрашивать первое число, операцию, второе число. После этого программа выведет результат и остановится.
Открыв редактор Emacs, приступил к редактированию созданных файлов.
Реализация функций калькулятора в файле calculate.с (рис. [-@fig:002])
![рис.2](/home/edstarikova/homework/study/2022/ОперационныеСистемы/os-intro/labs/lab13/report/image/14.jpg){ #fig:002 width=70% }
Интерфейсный файл calculate.h, описывающий формат вызова функции калькулятора (рис. [-@fig:003])
![рис.3](/home/edstarikova/homework/study/2022/ОперационныеСистемы/os-intro/labs/lab13/report/image/15.jpg){ #fig:003 width=70% }
Основной файл main.c, реализующий интерфейс пользователя к калькулятору(рис. [-@fig:004])
![рис.4](/home/edstarikova/homework/study/2022/ОперационныеСистемы/os-intro/labs/lab13/report/image/16.jpg){ #fig:004 width=70% }

3. Выполнил компиляцию программы посредством gcc, используя команды «gcc -c calculate.c», «gcc -c main.c» и «gcc calculate.o main.o -o calcul -lm»(рис. [-@fig:005])
![рис.5](/home/edstarikova/homework/study/2022/ОперационныеСистемы/os-intro/labs/lab13/report/image/2.jpg){ #fig:005 width=70% }
Редактируем файл Маке(рис. [-@fig:006])
![рис.6](/home/edstarikova/homework/study/2022/ОперационныеСистемы/os-intro/labs/lab13/report/image/17.jpg){ #fig:006 width=70% }
4. После этого я удалила исполняемые и объектные файлы из каталога с помощью команды «make clean». Выполнила компиляцию файлов, используя команды «make calculate.o», «make main.o», «male calcul» (рис. [-@fig:007])
![рис.7](/home/edstarikova/homework/study/2022/ОперационныеСистемы/os-intro/labs/lab13/report/image/3.jpg){ #fig:007 width=70% }
5. Далее с помощью gdb выполнил отладку программы calcul. Запустил отладчик GDB, загрузив в него программу для отладки, используя команду: «gdb ./calcul»(рис. [-@fig:008])
![рис.8](/home/edstarikova/homework/study/2022/ОперационныеСистемы/os-intro/labs/lab13/report/image/4.jpg){ #fig:008 width=70% }
Для запуска программы внутри отладчика ввёл команду «run» (рис. [-@fig:009])
![рис.9](/home/edstarikova/homework/study/2022/ОперационныеСистемы/os-intro/labs/lab13/report/image/5.jpg){ #fig:009 width=70% }
Для запуска программы внутри отладчика ввёл команду «run» (рис. [-@fig:010])
![рис.10](/home/edstarikova/homework/study/2022/ОперационныеСистемы/os-intro/labs/lab13/report/image/6.jpg){ #fig:010 width=70% }
Для просмотра строк с 12 по 15 основного файла использовал команду «list 12,15» (рис. [-@fig:011])
![рис.11](/home/edstarikova/homework/study/2022/ОперационныеСистемы/os-intro/labs/lab13/report/image/7.jpg){ #fig:011 width=70% }
Для просмотра определённых строк не основного файла использовал команду «list calculate.c:20,29» (рис. [-@fig:012])
![рис.12](/home/edstarikova/homework/study/2022/ОперационныеСистемы/os-intro/labs/lab13/report/image/8.jpg){ #fig:012 width=70% }
Для просмотра определённых строк не основного файла использовал команду «list calculate.c:15,22» (рис. [-@fig:013])
![рис.13](/home/edstarikova/homework/study/2022/ОперационныеСистемы/os-intro/labs/lab13/report/image/9.jpg){ #fig:013 width=70% }



# Выводы

В ходе выполнения данной лабораторной работы я приобрёла простейшие навыки разработки, анализа, тестирования и отладки приложений в ОС типа UNIX/Linux на примере создания на языке программирования С калькулятора с простейшими функциями.
