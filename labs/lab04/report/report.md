---
## Front matter
title: "Отчет о лабораторной работе"
subtitle: "Лабораторная работа"
author: "Калашникова Дарья"

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
mainfont: IBM Plex Serif
romanfont: IBM Plex Serif
sansfont: IBM Plex Sans
monofont: IBM Plex Mono
mathfont: STIX Two Math
mainfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
romanfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
sansfontoptions: Ligatures=Common,Ligatures=TeX,Scale=MatchLowercase,Scale=0.94
monofontoptions: Scale=MatchLowercase,Scale=0.94,FakeStretch=0.9
mathfontoptions:
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

Получение практических навыков работы в консоли с расширенными атрибутами файлов

# Выполнение лабораторной работы


Для начала откроем терминал и перейдем в пользователя guest, затем проверим роасширенные атрибуты файла, затем попробуем утсановить права 600,
после чего попытаемся утсановить расширенный атрибут а от пользователя guest

![Открытие](image/1.png){#fig:001 width=70%}

Так как у нас не получилось установить расширенный атрибут а от имени пользователя guest, откроем второй терминал и перейдем в супер пользователя и попробуем снова установить расширенный атрибут а 

![Установка](image/2.png){#fig:002 width=70%}

Далле вернемся на пользователя guest и проверим что атрибут установлен  и  выполним дозапись в файл test и проверим 

![Дозапись](image/3.png){#fig:003 width=70%}

После чего  попробуем перезаписать файл, затем переименовать и попробовать изменить права доступа, и как мы увидим везде нам будет отказано 

![Перезапись](image/4.png){#fig:004 width=70%}

Затем вернемся в супер пользователя и снимем расширение а

![Расширение](image/5.png){#fig:005 width=70%}

И попробуем ранее запрещенные операции для проверки 

![Проверка](image/6.png){#fig:006 width=70%}

После чего перейдем в супер пользователя и установим расширенный атрибут i 

![Установка](image/7.png){#fig:007 width=70%}

Далее снова вернемся в пользователя guest и проверим атрибут i

![Возвращение](image/8.png){#fig:008 width=70%}


# Выводы

В результате выполнения лабораторной работы я получила  навыки работы в консоли с расширенными атрибутами файлов
