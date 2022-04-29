---
## Front matter
title: "Отчет по лабораторной работе №3"
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

Целью данной работы является изучение идеологии и применение средств контроля версий.


# Задание

– Сделайте отчёт по предыдущей лабораторной работе в формате Markdown.
– Вкачествеотчётапросьбапредоставитьотчётыв3форматах:pdf,docx иmd (вархиве,
поскольку он должен содержать скриншоты,Makefile ит.д.)


# Выполнение лабораторной работы

1. Создайте учётную запись на https://github.com (рис. [-@fig:001])

![рис.1](/home/edstarikova/laboratory/лаба2/1.jpg){ #fig:001 width=70% }

2. Настраиваем систему контроля версий git.
Синхронизируем учётную запись github с компьютером 
git config --global user.name "EvgeniaStarikova"
git config --global user.email “jenya.stari960687@gmail.com"
Затем создаём новый ключ на github ssh-keygen -C "jenya.stari960687@gmail.com"  и привязываем его к компьютеру через консоль (рис. [-@fig:002])
![рис.2](/home/edstarikova/laboratory/лаба2/2.jpg){ #fig:002 width=70% }
3. Устанавливаю git-flow в Fedora Linux (рис. -@fig:003)
![рис.3](/home/edstarikova/laboratory/лаба2/3.jpd.png){ #fig:003 width=70% }

4. Устанавливаю gh в Fedora Linux. Также задаю базовые настройки Git (имя и почта пользователя) (рис. [-@fig:004])
![рис.4](/home/edstarikova/laboratory/лаба2/4.png){ #fig:004 width=70%}

5. Настроим utf-8 в выводе сообщений git, Настройте верификацию и подписание коммитов git. Зададим имя начальной ветки (будем называть её master), Параметр autocrlf: Параметр safecrlf. (рис. [-@fig:005])
![рис.5](/home/edstarikova/laboratory/лаба2/5.png){ #fig:005 width=70%}

6. Создаём ключи ssh – по алгоритму rsa с ключём размером 4096 бит – по алгоритму ed25519 (рис. [-@fig:006]) (рис. [-@fig:006,1])
![рис.6](/home/edstarikova/laboratory/лаба2/6.png){ #fig:006 width=70%}
![рис.6,1](/home/edstarikova/laboratory/лаба2/6,1.png){ #fig:006,1 width=70%}

7. Создаём ключи pgp. Генерируем ключ с параметрами: Из предложенных опций выбираем: – тип RSA and RSA; – размер 4096; – выберите срок действия; значение по умолчанию— 0 (срок действия не истекает никогда) (рис. [-@fig:007]) (рис. [-@fig:008]) (рис. [-@fig:009])
![рис.7](/home/edstarikova/laboratory/лаба2/7.png){ #fig:007 width=70%}
![рис.8](/home/edstarikova/laboratory/лаба2/8.png){ #fig:008 width=70%}
![рис.9](/home/edstarikova/laboratory/лаба2/9.png){ #fig:009 width=70%}

8. Добавляем ключ в Github. Копируем отпечаток ключа (рис. [-@fig:0010])
![рис.10](/home/edstarikova/laboratory/лаба2/10.png){ #fig:0010 width=70%}

9. Сознание репозитория курса на основе шаблона. (рис. [-@fig:0011])
![рис.11](/home/edstarikova/laboratory/лаба2/11.png){ #fig:0011 width=70%}


# Выводы

Я изучил идеологию и применение контроля версий.


