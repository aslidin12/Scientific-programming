---
## Front matter
title: "Отчёт по 5 стадии персонального проекта"
author: "Елизавета Александровна Гайдамака"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
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

Конечной целью работы является создание персонального сайта научного работника с помощью hugo на основе шаблона wowchemy academic.

# Задание

Добавить с сайту все остальные элементы.

- Сделать записи для персональных проектов.
- Сделать пост по прошедшей неделе.
- Добавить пост на тему по выбору.
  - Языки научного программирования.

# Выполнение работы

Добавила проект и изменила содержание в `\content\project\example\index.md`.

![Рис.1](image\picture1.png)  

Вот так он выглядит на сайте.

![Рис.2](image\picture2.png)  

Добавила новый пост на тему "языки научного программирования".

![Рис.3](image\picture3.png) 

Вот так он выглядит на сайте.

![Рис.4](image\picture4.png)  

Так же добавила пост о прошедшей неделе.

![Рис.5](image\picture5.png) 

# Выводы

Благодаря данной работе я добавила на сайт свои проекты.
