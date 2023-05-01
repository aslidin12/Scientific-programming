---
## Front matter
title: "Отчёт по 4 стадии персонального проекта"
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

Добавить к сайту ссылки на научные и библиометрические ресурсы.

- Зарегистрироваться на соответствующих ресурсах и разместить на них ссылки на сайте:
  - eLibrary : https://elibrary.ru/;
  - Google Scholar : https://scholar.google.com/;
  - ORCID : https://orcid.org/;
  - Mendeley : https://www.mendeley.com/;
  - ResearchGate : https://www.researchgate.net/;
  - Academia.edu : https://www.academia.edu/;
  - arXiv : https://arxiv.org/;
  - github : https://github.com/.
- Сделать пост по прошедшей неделе.
- Добавить пост на тему по выбору:
  - Оформление отчёта.
  - Создание презентаций.
  - Работа с библиографией.

# Выполнение работы

Добавляем ссылки в файл `\content\authors\admin\_index.md` и ставим подходящие иконки. Вот так это теперь выглядит на сайте.

![Рис.1](image\picture1.png)  

Добавляем пост о прошедшей недели.

![Рис.2](image\picture2.png)  

Вот так выглядит пост.

![Рис.3](image\picture3.png) 

Добавляем пост по выбору. Я взяла тему "создание презентаций".

![Рис.4](image\picture4.png)  

Вот так выглядит пост.

![Рис.5](image\picture5.png) 

# Выводы

Благодаря данной работе я добавила на сайт ссылки на электронные ресурсы и сделала 2 поста.
