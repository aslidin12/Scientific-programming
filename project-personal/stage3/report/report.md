---
## Front matter
title: "Отчёт по 3 стадии персонального проекта"
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

Добавить к сайту достижения.

- Список достижений.
  - Добавить информацию о навыках (Skills).
  - Добавить информацию об опыте (Experience).
  - Добавить информацию о достижениях (Accomplishments).
- Сделать пост по прошедшей неделе.
- Добавить пост на тему по выбору:
  - Легковесные языки разметки.
  - Языки разметки. LaTeX.
  - Язык разметки Markdown.

# Выполнение работы

Изменила раздел Skills в `\content\home\skills.md`.

![Рис.1](image\picture1.png)  

Вот так он теперь выглядит на сайте.

![Рис.2](image\picture2.png)  

Изменила раздел Experience в `\content\home\experience.md`.

![Рис.3](image\picture3.png) 

Вот так он теперь выглядит на сайте.

![Рис.4](image\picture4.png)  

Изменила раздел Accomplishments в `\content\home\accomplishments.md`.

![Рис.5](image\picture5.png) 

Вот так он теперь выглядит на сайте.

![Рис.6](image\picture6.png) 

Создала новый пост с помощью `hugo new post\week2` и посместила в `\content\post\week2\index.md` отчет по прошедшей неделе.

![Рис.7](image\picture7.png) 

![Рис.8](image\picture8.png) 

Создала новый пост с помощью `hugo new post\markdown` и посместила в `\content\post\markdown\index.md` текст нового поста на тему "Язык разметки Markdown".

![Рис.9](image\picture9.png) 

![Рис.10](image\picture10.png) 

# Выводы

Благодаря данной работе я добавила на сайт свои достижения.
