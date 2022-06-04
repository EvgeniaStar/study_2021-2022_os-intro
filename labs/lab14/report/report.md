---
## Front matter
title: "Отчет по лабораторной работе №14"
subtitle: "Дисциплина: оперативные системы"
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

Приобретение практических навыков работы с именованными каналами.

# Задание

1. Работает не 1 клиент,а несколько (например,два).
2. Клиенты передаюттекущее время с некоторой периодичностью (например,раз в пять
секунд).Используйте функцию sleep() для приостановки работы клиента.
3. Сервер работаетне бесконечно,а прекращаетработу через некоторое время (напри-
мер,30 сек).Используйте функцию clock() для определения времени работы сервера.

# Выполнение лабораторной работы

1. (рис. [-@fig:001])

![рис.1](/home/edstarikova/homework/study/2022/ОперационныеСистемы/os-intro/labs/lab14/report/image/1.jpg){ #fig:001 width=70% }
2. (рис. [-@fig:002])
![рис.2](/home/edstarikova/homework/study/2022/ОперационныеСистемы/os-intro/labs/lab14/report/image/6.jpg){ #fig:002 width=70% }
3. (рис. [-@fig:003])
![рис.3](/home/edstarikova/homework/study/2022/ОперационныеСистемы/os-intro/labs/lab14/report/image/5.jpg){ #fig:003 width=70% }
4. (рис. [-@fig:004])
![рис.4](/home/edstarikova/homework/study/2022/ОперационныеСистемы/os-intro/labs/lab14/report/image/4.jpg){ #fig:004 width=70% }
5. (рис. [-@fig:005])
![рис.5](/home/edstarikova/homework/study/2022/ОперационныеСистемы/os-intro/labs/lab14/report/image/3.jpg){ #fig:005 width=70% }
6. (рис. [-@fig:006])
![рис.6](/home/edstarikova/homework/study/2022/ОперационныеСистемы/os-intro/labs/lab14/report/image/2.jpg){ #fig:006 width=70% }


# Выводы

Преобрела практические навыки с именными каналами
