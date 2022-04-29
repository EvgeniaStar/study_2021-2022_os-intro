---
## Front matter
title: "Отчет по лабораторной работе №4"
subtitle: "Операционная система"
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

Целью данной работы является приобретение практических навыков взаимодействия пользователя с системой по-
средством командной строки.



# Выполнение лабораторной работы

1. Определяем  полное имя нашего домашнего каталога. (рис. [-@fig:001])

![рис.1](/home/edstarikova/laboratory/лаба4/image4/1.png){ #fig:001 width=70% }

1. Переходим в каталог /tmp и выводим его содержимое c помощью ls различными опциями.
      1. ls (рис. [-@fig:002])
      2. ls -a (рис. [-@fig:003])
      3. ls -F (рис. [-@fig:004])
      4. ls -l (рис. [-@fig:005])
![рис.2](/home/edstarikova/laboratory/лаба4/image4/2.png){ #fig:002 width=70% }
![рис.3](/home/edstarikova/laboratory/лаба4/image4/3.png){ #fig:003 width=70% }
![рис.4](/home/edstarikova/laboratory/лаба4/image4/4.png){ #fig:004 width=70% }
![рис.5](/home/edstarikova/laboratory/лаба4/image4/5.png){ #fig:005 width=70% }

1. Определить, есть ли в каталоге /var/spool подкаталог с именем cron (такого подкаталога не было) (рис. [-@fig:006])
![рис.6](/home/edstarikova/laboratory/лаба4/image4/6.png){ #fig:006 width=70% }

1. Переходим в наш домашний каталог и выводим на экран его содержимое.(рис. [-@fig:007])
![рис.7](/home/edstarikova/laboratory/лаба4/image4/7.png){ #fig:007 width=70% }
1. Создаём новый каталог с именем newdir. (рис. [-@fig:008])
![рис.8](/home/edstarikova/laboratory/лаба4/image4/8.png){ #fig:008 width=70% }
1. В каталоге ~/newdir создаём новый каталог с именем morefun. (рис. [-@fig:009])
![рис.9](/home/edstarikova/laboratory/лаба4/image4/9.png){ #fig:009 width=70% }
1. В домашнем каталоге создайте одной командой три новых каталога с именами letters, memos, misk. Затем удалите эти каталоги одной командой.(рис. [-@fig:010])
![рис.10](/home/edstarikova/laboratory/лаба4/image4/10.png){ #fig:010 width=70% }
1. Удалем каталог ~/newdir/morefun из домашнего каталога. Проверяем, был ли каталог удалён. (рис. [-@fig:011])
![рис.11](/home/edstarikova/laboratory/лаба4/image4/11.png){ #fig:011 width=70% }
1. С помощью команды man определите, какую опцию команды ls нужно использовать для просмотра содержимое не только указанного каталога, но и подкаталогов, входящих в него. (рис. [-@fig:012]) (рис. [-@fig:013]) (рис. [-@fig:014]) (рис. [-@fig:015]) (рис. [-@fig:016])
![рис.12](/home/edstarikova/laboratory/лаба4/image4/12.png){ #fig:012 width=70% }
![рис.13](/home/edstarikova/laboratory/лаба4/image4/13.png){ #fig:013 width=70% }
![рис.14](/home/edstarikova/laboratory/лаба4/image4/14.png){ #fig:014 width=70% }
![рис.15](/home/edstarikova/laboratory/лаба4/image4/15.png){ #fig:015 width=70% }
![рис.16](/home/edstarikova/laboratory/лаба4/image4/16.png){ #fig:016 width=70% }
1. С помощью команды man определите набор опций команды ls, позволяющий отсортировать по времени последнего изменения выводимый список содержимого каталога с развёрнутым описанием файлов. (рис. [-@fig:017])
![рис.17](/home/edstarikova/laboratory/лаба4/image4/17.png){ #fig:017 width=70% }
1. Используйте команду man для просмотра описания следующих команд: cd, pwd, mkdir, rmdir, rm. Поясните основные опции этих команд. (рис. [-@fig:018])
![рис.18](/home/edstarikova/laboratory/лаба4/image4/18.png){ #fig:018 width=70% }
1. Используя информацию, полученную при помощи команды history, выполните модификацию и исполнение нескольких команд из буфера команд. (рис. [-@fig:019])
![рис.19](/home/edstarikova/laboratory/лаба4/image4/19.png){ #fig:019 width=70% }




# Выводы

Я приобрела практические навыков взаимодействия пользователя с системой посредством командной строки.


