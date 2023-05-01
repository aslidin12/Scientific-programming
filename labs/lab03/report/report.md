---
## Front matter
title: "Отчёт по лабораторной работе 3"
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

Целью данной работы является изучение идеологии и применения средств контроля версий и получение умений работы с git.

# Задание

Создать базовую конфигурацию для работы с git.
- Создать ключ SSH.
- Создать ключ PGP.
- Настроить подписи git.
- Зарегистрироваться на Github.
- Создать локальный каталог для выполнения заданий по предмету

# Теоретическое введение

Система управления версиями позволяет хранить несколько версий одного и того же документа, при необходимости возвращаться к более ранним версиям, определять, кто и когда сделал то или иное изменение

Хранилище версий - то, где хранятся все документы вместе с историей их изменения и другой служебной информацией.
Коммит - зафиксированный набор изменений, который показывает, какие файлы изменились и что именно в них изменилось.
История - список всех изменений.
Рабочая копия - снимок одной версии проекта

Централизованные VCS: одно основное хранилище всего проекта; каждый пользователь копирует себе необходимые ему файлы из этого репозитория, изменяет и, затем, добавляет свои изменения обратно. Примеры: Subversion, CVS, TFS, VAULT, AccuRev.
Децентрализованные VCS: у каждого пользователя свой вариант (возможно не один) репозитория, присутствует возможность добавлять и забирать изменения из любого репозитория. Пример: Git, Mercurial, Bazaar.

Порядок работы с общим хранилищем VCS:

- Клонировать репозиторий себе в гитхаб
- Клонировать репозиторий себе на устройство
- Внести изменения
- Добавить новую версию файлов на сервер

Git решает две задачи: хранить информацию о всех изменениях в коде, начиная с самой первой строчки, а вторая — обеспечение удобства командной работы над кодом.

Краткая характеристика команд git:

- git config - настройки
- git init - создание репозитория
- git add - добавление файлов в индекс
- git commit - коммит изменений
- git status -  список измененных файлов
- git push - перенос изменений в главную ветку
- git rm - удаление файлов из индекса

Локальный репозиторий можно загрузить на гитхаб и работать с ним с помощью VCS, т.е. загружать новые версии, не теряя старые.

Ветка в Git это подвижный указатель на один из коммитов. Обычно ветка указывает на последний коммит в цепочке коммитов. Ветки нужны для того, чтобы программисты могли вести совместную работу над проектом и не мешать друг другу при этом.

Чтобы проигнорировать файлы при коммит, надо просто не добавлять их в коммит. Игнорируют те файлы, которые пользователь не хочет отправлять в репозиторий.

# Выполнение лабораторной работы

Cкачиваем и устанавливаем git flow и gh.

![Рис.1](image\picture1.png)  

![Рис.2](image\picture2.png)  

Настраиваем git: задаем имя владельца, настраиваем utf-8 в выводе сообщений git, зададим имя начальной ветки, параметры autpcrlf и safecrlf.

![Рис.3](image\picture3.png) 

Создаем ключ SSH с помощью команды ssh-keygen

![Рис.4](image\picture4.png)  

Генерируем pgp ключ и вводим свои данные.

![Рис.5](image\picture5.png)  

![Рис.6](image\picture6.png)  

Добавляем ключ в github.

![Рис.7](image\picture7.png)  

Настраиваем подписи git.

![Рис.8](image\picture8.png)  

Авторизируемся в гитхабе на устройстве.

![Рис.9](image\picture9.png)

![Рис.10](image\picture10.png)

![Рис.11](image\picture11.png)

Создаем репозиторий на гитхабе с помощью template. Потом клонируем его себе на компьютер.


![Рис.12](image\picture12.png)  

Вносим поправки в репозиторий на компьютере.

![Рис.13](image\picture13.png)  

Добавляем файлы с поправками в коммит и отправляем на сервер.

![Рис.14](image\picture14.png)  

Проверяем, что новая версия загрузилась.

# Выводы

Благодаря данной работе я изучила идеологию и применение средств контроля версий и получила умения работы с git.
