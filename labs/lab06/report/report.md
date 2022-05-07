---
## Front matter
title: "Отчет по лабораторной работе №6"
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

Ознакомление с инструментами поиска файлов и фильтрации текстовых данных.
Приобретение практических навыков: по управлению процессами (и заданиями), по
проверке использования диска и обслуживанию файловых систем.


# Выполнение лабораторной работы

1. Выполниои вход в сиситему Linux. 
1. Записываем в файл file.txt названия файлов,содержащихся в каталоге /etc. Дописываем в этот же файл названия файлов,содержащихся в моём домашнем каталоге. (рис. [-@fig:001]) 

![рис.1](/home/edstarikova/Изображения/1.jpg){ #fig:001 width=70% }

1. Выведите имена всех файлов из file.txt,имеющих расширение .conf,после чего
запишите их в новыйтекстовой файл conf.txt (рис. [-@fig:002])
![рис.2](/home/edstarikova/%D0%98%D0%B7%D0%BE%D0%B1%D1%80%D0%B0%D0%B6%D0%B5%D0%BD%D0%B8%D1%8F/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20%D0%BE%D1%82%202022-05-05%2006-53-33.png){ #fig:002 width=70% }

1. Определите,какие файлы в вашем домашнем каталоге имеют имена,начинавшиеся
с символа c? Предложите несколько вариантов,как это сделать.(рис. [-@fig:003])
![рис.3](home/edstarikova/%D0%98%D0%B7%D0%BE%D0%B1%D1%80%D0%B0%D0%B6%D0%B5%D0%BD%D0%B8%D1%8F/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20%D0%BE%D1%82%202022-05-05%2006-53-13.png){ #fig:003 width=70% }
1. Выведите на экран (по странично) имена файлов из каталога /etc,начинающиеся
с символа h.(рис. [-@fig:004])
![рис.4](/home/edstarikova/%D0%98%D0%B7%D0%BE%D0%B1%D1%80%D0%B0%D0%B6%D0%B5%D0%BD%D0%B8%D1%8F/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20%D0%BE%D1%82%202022-05-05%2006-49-11.png){ #fig:004 width=70% }
1. Запустите в фоновом режиме процесс,который будетзаписывать в файл ~/logfile
файлы,имена которых начинаются с log. (рис. [-@fig:005])
![рис.5](/home/edstarikova/%D0%98%D0%B7%D0%BE%D0%B1%D1%80%D0%B0%D0%B6%D0%B5%D0%BD%D0%B8%D1%8F/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20%D0%BE%D1%82%202022-05-05%2006-54-00.png){ #fig:005 width=70% }
1. Удалите файл ~/logfile. (рис. [-@fig:006])
![рис.6](/home/edstarikova/%D0%98%D0%B7%D0%BE%D0%B1%D1%80%D0%B0%D0%B6%D0%B5%D0%BD%D0%B8%D1%8F/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20%D0%BE%D1%82%202022-05-05%2006-55-32.png){ #fig:006 width=70% }
1. Запустите из консоли в фоновом режиме редактор gedit.(рис. [-@fig:007])
![рис.7]( /home/edstarikova/%D0%98%D0%B7%D0%BE%D0%B1%D1%80%D0%B0%D0%B6%D0%B5%D0%BD%D0%B8%D1%8F/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20%D0%BE%D1%82%202022-05-05%2006-57-07.png){ #fig:007 width=70% }
1. Определите идентификатор процесса gedit,используякомандуps,конвейерифильтр
grep.Как ещё можно определить идентификатор процесса?(рис. [-@fig:008])
![рис.8](/home/edstarikova/Изображения/5.png){ #fig:008 width=70% }
1. Прочтите справку (man) команды kill, после чего используйте её для завершения
процесса gedit.(рис. [-@fig:009])
![рис.9](/home/edstarikova/%D0%98%D0%B7%D0%BE%D0%B1%D1%80%D0%B0%D0%B6%D0%B5%D0%BD%D0%B8%D1%8F/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20%D0%BE%D1%82%202022-05-05%2006-58-55.png){ #fig:009 width=70% }
1. Выполните команды df и du,предварительно получив более подробную информацию
об этих командах,с помощью команды man.(рис. [-@fig:010])
![рис.10](/home/edstarikova/%D0%98%D0%B7%D0%BE%D0%B1%D1%80%D0%B0%D0%B6%D0%B5%D0%BD%D0%B8%D1%8F/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20%D0%BE%D1%82%202022-05-05%2007-02-31.png){ #fig:010 width=70% }
1. Воспользовавшись справкой команды find,выведите имена всех директорий,имею-
щихся в вашем домашнем каталоге (рис. [-@fig:011])

![рис.11](/home/edstarikova/%D0%98%D0%B7%D0%BE%D0%B1%D1%80%D0%B0%D0%B6%D0%B5%D0%BD%D0%B8%D1%8F/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%20%D0%BE%D1%82%202022-05-05%2007-05-55.png){ #fig:011 width=70% }
# Выводы

Я ознакомилась с инструментами поиска файлов и фильтрации текстовых данных. Также приобрела практические навыки: по управлению процессами, по проверке использования диска и обслуживанию файлов.


