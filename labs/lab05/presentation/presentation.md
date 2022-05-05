---
## Front matter
lang: ru-RU
title: Structural approach to the deep learning method
author: |

	Starikova Evgenia\inst{1}

institute: |
	\inst{1}RUDN University, Moscow, Russian Federation
	
	
date: NEC--2022, 3 May

## Formatting
toc: false
slide_level: 2
theme: metropolis
header-includes: 
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'
aspectratio: 43
section-titles: true
---


# Цель работы

Ознакомление с файловой системой Linux, её структурой, именами и содержанием
каталогов. Приобретение практических навыков по применению команд для работы
с файлами и каталогами,по управлению процессами (и работами),по проверке исполь-
зования диска и обслуживанию файловой системы

# Выполнение заданий из первой части лабораторной работы

## Выполняю примеры из первой части 
- изучаем команды для работы с файлами и каталогами (touch, cat, less, head, tail ) (рис.1 [-@fig:001]) 

![рис. 1](/home/edstarikova/image/123.jpg){ #fig:001 width=70% }




# Копируем файл /usr/include/sys/io.h в домашний каталоги назовите его equipment. 
(рис.2 [-@fig:002]) 
![рис. 2](/home/edstarikova/image/3.jpg){ #fig:002 width=70% }

## В домашнем каталоге создаём директорию ~/ski.plases. Перемещаем файл equipment в каталог ~/ski.plases. Переименновываем файл ~/ski.plases/equipment в ~/ski.plases/equiplist. 
(рис.3 [-@fig:003]) 
![рис. 3](/home/edstarikova/image/2.jpg){ #fig:003 width=70% }


## Создаём в домашнем каталоге файл abc1 и скопируем его в каталог ~/ski.plases,называем его equiplist2 
(рис.4 [-@fig:004]) 
![рис. 4](/home/edstarikova/image/11.jpg){ #fig:004 width=70% }

## Создаём каталог с именем equipment в каталоге ~/ski.plases Переместим файлы ~/ski.plases/equiplist и equiplist2 в каталог ~/ski.plases/equipment. 
(рис.5 [-@fig:005]) 
![рис. 5](/home/edstarikova/image/11.jpg){ #fig:005 width=70% }

## Создаём и переместим каталог ~/newdir в каталог ~/ski.plases и назовите его plans. 
(рис.6 [-@fig:006]) 
![рис. 6](/home/edstarikova/image/6.jpg){ #fig:006 width=70% }

# Определяем опции команды chmod,необходимые длятого,чтобы присвоить перечисленным ниже файлам выделенные права доступа, считая, что в начале таких прав нет:
## - drwxr--r-- ... australia (рис.7 [-@fig:007]) 
 ![рис. 7](/home/edstarikova/image/7.jpg){ #fig:007 width=70% }
## - drwx--x--x ... play (рис.8 [-@fig:008]) 
  ![рис. 8](/home/edstarikova/image/56.jpg){ #fig:008 width=70% }
## - -r-xr--r-- ... my_os (рис.9 [-@fig:009]) 
  ![рис. 9](/home/edstarikova/image/12.jpg){ #fig:009 width=70% }
##  - -rw-rw-r-- ... feathers (рис.10 [-@fig:010]) 
  ![рис. 10](/home/edstarikova/image/8.jpg){ #fig:010 width=70% }
# Чтобы просмотреть содержимое файла /etc/password используе  команду cat (рис.11 [-@fig:011]) 
![рис. 11](/home/edstarikova/image/66.jpg){ #fig:011 width=70% }
# Чтобы скопировать файл ~/feathers в файл ~/file.old используем команду ср (рис.12 [-@fig:012]) 
![рис. 12](/home/edstarikova/image/77.jpg){ #fig:011 width=70% }
# Чтобы переместить файл ~/file.old в каталог ~/play используем команду mv (рис.13 [-@fig:013]) 
![рис. 13](/home/edstarikova/image/77.jpg){ #fig:011 width=70% }

# Чтобы скопировать каталог ~/play в каталог ~/fun mvdir (рис.14 [-@fig:014]) 
![рис. 14](/home/edstarikova/image/99.jpg){ #fig:014 width=70% }
# Чтобы переместить каталог ~/fun в каталог ~/play и назовите его games используем команду mv (рис.15 [-@fig:015]) 
![рис. 15](/home/edstarikova/image/99.jpg){ #fig:015 width=70% } 
# Чтобы лишить владельца файла ~/feathers права на чтение используем u-r (рис.16 [-@fig:016])
![рис.16](/home/edstarikova/image/68.jpg){ #fig:016 width=70% } 
# Что произойдёт,если вы попытаетесь просмотреть файл ~/feathers командой cat? (рис.17 [-@fig:017])
![рис.17](/home/edstarikova/image/68.jpg) { #fig:017 width=70% } 
# Чтобы дать владельцу файла ~/feathers право на чтение используем u+r (рис.18 [-@fig:018])
![рис.18](/home/edstarikova/image/68.jpg) { #fig:018 width=70% } 
# Чтобы лишить владельца каталога ~/play права на выполнение используем u-x (рис.19 [-@fig:019])
![рис.19](/home/edstarikova/image/67.jpg) { #fig:019 width=70% } 
# Чтобы дать владельцу каталога ~/play право на выполнение используем u+x (рис.20 [-@fig:020])
![рис.20](/home/edstarikova/image/67.jpg) { #fig:020 width=70% } 
# Прочитайте man по командам mount,fsck,mkfs,kill и кратко их охарактеризуйте, приведя примеры.
## MUONT
![рис.21](/home/edstarikova/image/9.jpg) { #fig:021 width=70% } 
## FSCK
![рис.22](/home/edstarikova/image/0.jpg) { #fig:022 width=70% } 
## MKFS
![рис.23](/home/edstarikova/image/22.jpg) { #fig:023 width=70% }
## KILL
![рис.24](/home/edstarikova/image/89.jpg) { #fig:024 width=70% } 

# Выводы

Я ознакомилась с файловой системой, её структурой, именами и соделжанием каталогов. Приобрела навыки по выполнению команд.


## {.standout}

Спасибо за внимание!!!
