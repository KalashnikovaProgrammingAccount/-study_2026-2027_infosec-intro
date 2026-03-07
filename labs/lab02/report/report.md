---
## Front matter
title: "Отчет о лабораторной работе"
subtitle: "Лабораторная работа №2"
author: "Калашникова Дарья Викторовна"

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

Получение практических навыков работы в консоли с атрибутами файлов, закрепление теоретических основ дискреционного раграничения доступа в современных системах с открытым кодом на базе OC Linux

# Выполнение лабораторной работы

Для начала откроем терминал и создадим пользователя  guest (рис. [-@fig:001]).

![Создание](image/1.png){#fig:001 width=70%}

После чего зайдем от нового пользователя guest, проверим в какой мы находимся директории, затем уточним имя, после чего id и группу (рис. [-@fig:002]).

![Вход под пользователем](image/2.png){#fig:002 width=70%}

Далее просмотрим файл  /etc/passwd (рис. [-@fig:003]).

![Просмотр](image/3.png){#fig:003 width=70%}

Теперь проверяем какие  атрибуты установлены на поддиректориях находящихся в директории home  (рис. [-@fig:004]). 

![Атрибуты](image/4.png){#fig:004 width=70%}

Затем создаем домашнюю директорию dir1 и проверяем  права данной директории (рис. [-@fig:005]).

![Создание](image/5.png){#fig:005 width=70%}

После чего снимаем с директории dir1 все атрибуты и проверяем,далее пытаемся создать в директории dir1 файл file1 (рис. [-@fig:006]).

![Снятие](image/6.png){#fig:006 width=70%}

Заполним таблицу «Установленные права и разрешённые действия».

| Права директории | Права файла | Создание файла | Удаление файла | Переименование файла | Смена атрибутов файла | Просмотр файлов в директории | Смена директории | Чтение файла | Запись в файл |
|------------------|-------------|----------------|----------------|----------------------|------------------------|-------------------------------|-------------------|---------------|---------------|
| d(000) | (000) | - | - | - | - | - | - | - | - |
| d--x (100) | (000) | + | - | - | - | - | + | - | - |
| d--x (100) | (700) | + | - | - | + | - | + | + | + |
| d-wx (300) | (000) | + | + | + | - | - | + | - | - |
| d-wx (300) | (700) | + | + | + | + | - | + | + | + |
| dr-x (500) | (000) | - | - | - | - | + | + | - | - |
| dr-x (500) | (700) | - | - | - | + | + | + | + | + |
| drwx (700) | (000) | + | + | + | - | + | + | - | - |
| drwx (700) | (700) | + | + | + | + | + | + | + | + |

Заполним таблицу «Минимальные права для совершения операций».

| Операция | Минимальные права на директорию | Минимальные права на файл |
|----------|----------------------------------|---------------------------|
| Создание файла | `-wx` (300) | не требуются |
| Удаление файла | `-wx` (300) | не требуются |
| Переименование файла | `-wx` (300) | не требуются |
| Смена атрибутов файла | `--x` (100) | `rwx` (700) или владение файлом |
| Просмотр файлов в директории | `r-x` (500) | не требуются |
| Смена директории (cd) | `--x` (100) | не требуются |
| Чтение файла | `--x` (100) | `r--` (400) |
| Запись в файл | `--x` (100) | `-w-` (200) |

# Выводы

В результате выполнения лабораторной работы я получила навыки работы в консоли с атрибутами файлов закрепление теоретических основ дискреционного разграничения доступа в современных системах с открытым кодом на базе OC Linux

# Список литературы{.unnumbered}

::: {#refs}
:::
