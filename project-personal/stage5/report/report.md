---
## Front matter
title: "Работа с burpsuite"
subtitle: "Часть 5"
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

Использовать Burp Suite

# Выполнение индивидуального проекта 

Для начала откроем терминал и запустим Burp Suite

![Открытие](image/1.png){#fig:001 width=70%}

После чего настроим его 

![Настройка](image/2.png){#fig:002 width=70%}

Затем проверим запустился ли burp suite или нет 

![Проверка](image/3.png){#fig:003 width=70%}

Далее настроим Proxy включив перехват запросов 

![Настройка](image/4.png){#fig:004 width=70%}

После чего запустим браузер с прокси  burp

![Запуск](image/5.png){#fig:005 width=70%}

Затем проверим работу прокси и убедимся что запрос перехвотили 

![Проверка](image/6.png){#fig:006 width=70%}

![Провекра](image/7.png){#fig:007 width=70%}


# Выводи 

В результате выполнения индивидуального проекта часть 5, я получила навыки работы с burp suite

