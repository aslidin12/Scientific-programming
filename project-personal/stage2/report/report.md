---
## Front matter
title: "Отчёт по 2 стадии персонального проекта"
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

Добавить к сайту данные о себе.

- Список добавляемых данных.
  - Разместить фотографию владельца сайта.
  - Разместить краткое описание владельца сайта (Biography).
  - Добавить информацию об интересах (Interests).
  - Добавить информацию от образовании (Education).
- Сделать пост по прошедшей неделе.
- Добавить пост на тему по выбору:
  - Управление версиями. Git.
  - Непрерывная интеграция и непрерывное развертывание (CI/CD).

# Выполнение работы

Сначала я поместила в папку admin ысвое фото и исправила информацию о роли и месте обучения в файле _index.md.

![Рис.1](image\picture1.png)  

Далее в том же файле я написала раздел Biography.

![Рис.2](image\picture2.png)  

Потом написала разделы Interests и Education.

![Рис.3](image\picture3.png) 

Далее я создавала пост про Git. Для этого загрузила подходящую картинку и в файле index.md написала текст поста.

![Рис.4](image\picture4.png)  

![Рис.5](image\picture5.png) 

Так же я исправила тэги, авторов и тд.

Теперь мой сайт выглядит так:

![Рис.6](image\picture6.png) 

![Рис.7](image\picture7.png) 

![Рис.8](image\picture8.png) 

![Рис.9](image\picture9.png) 

# Выводы

Благодаря данной работе я добавила информацию о себе на сайт и создала свой первый пост.
