---
## Front matter
title: "Отчёт по лабораторной работе 4"
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

Размещение на Github pages заготовки для персонального сайта.

- Установить необходимое программное обеспечение.
- Скачать шаблон темы сайта.
- Разместить его на хостинге git.
- Установить параметр для URLs сайта.
- Разместить заготовку сайта на Github pages.

# Выполнение лабораторной работы

Копируем себе в гит шаблон wowchemy. Называем его hgo.

![Рис.1](image\picture1.png)  

Создаем новый репозиторий lisagaydamaka.github.io.

![Рис.2](image\picture2.png)  

Клонируем на компьютер оба репозитория.

![Рис.3](image\picture3.png) 

Создаем новую ветку, называем ее main.

![Рис.4](image\picture4.png)  

Как тест создаем и 'пушим' файл README.md.

![Рис.5](image\picture5.png)  

Создаем сабмодуль в папке public.

![Рис.6](image\picture6.png)  

Генерируем сайт с помощью команды hugo.

![Рис.7](image\picture7.png)  

Добавляем изменения на гитхаб.

![Рис.8](image\picture8.png)  

Переходим на github pages.

![Рис.9](image\picture9.png)

Открываем наш сайт.

![Рис.10](image\picture10.png)

# Выводы

Благодаря данной работе я разместила на Github pages заготовку для персонального сайта.
