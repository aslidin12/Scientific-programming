---
## Front matter
title: "Отчёт по лабораторной работе 6"
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

Целью данной работы является ознакомление с инструментами поиска файлов и фильтрации текстовых данных.
Приобретение практических навыков по управлению процессами (и заданиями), по
проверке использования диска и обслуживанию файловых систем.


# Задание

1. Осуществите вход в систему, используя соответствующее имя пользователя.
2. Запишите в файл file.txt названия файлов, содержащихся в каталоге /etc. Допишите в этот же файл названия файлов, содержащихся в вашем домашнем каталоге.
3. Выведите имена всех файлов из file.txt, имеющих расширение .conf, после чего запишите их в новый текстовой файл conf.txt.
4. Определите, какие файлы в вашем домашнем каталоге имеют имена, начинавшиеся
с символа c? Предложите несколько вариантов, как это сделать.
5. Выведите на экран (по странично) имена файлов из каталога /etc, начинающиеся
с символа h.
6. Запустите в фоновом режиме процесс, который будет записывать в файл ~/logfile файлы, имена которых начинаются с log.
7. Удалите файл ~/logfile.
8. Запустите из консоли в фоновом режиме редактор gedit.
9. Определите идентификатор процесса gedit, используя команду ps, конвейер и фильтр grep. Как ещё можно определить идентификатор процесса?
10. Прочтите справку (man) команды kill, после чего используйте её для завершения процесса gedit.
11. Выполните команды df и du, предварительно получив более подробную информацию об этих командах, с помощью команды man.
12. Воспользовавшись справкой команды find, выведите имена всех директорий, имеющихся в вашем домашнем каталоге.

# Теоретическое введение

1. Какие потоки ввода вывода вы знаете?

В системе по умолчанию открыто три специальных потока:
- stdin — стандартный поток ввода (по умолчанию: клавиатура), файловый дескриптор
0;
- stdout — стандартный поток вывода (по умолчанию: консоль), файловый дескриптор
1;
- stderr — стандартный поток вывод сообщений об ошибках (по умолчанию: консоль),
файловый дескриптор 2.

2. Объясните разницу между операцией > и >>.

Операция ">" полностью перезаписывает файл, а ">>" - только дописывает в него информацию.

3. Что такое конвейер?

Конвейер - это множество объединенных процессов. Выход одного процесса направляется на вход другого.

4. Что такое процесс? Чем это понятие отличается от программы?

Компьютерная программа — пассивная последовательность инструкций. А процесс — непосредственное выполнение этих инструкций.

5. Что такое PID и GID?

PID - аббревиатура от Process ID.

GID - аббревиатура от Group ID.

6. Что такое задачи и какая команда позволяет ими управлять?

Задачи (jobs) - фоновые процессы в линукс. Управлять ими можно с помощью команды jobs.

7. Найдите информацию об утилитах top и htop. Каковы их функции?

top (table of processes) — консольная команда, которая выводит список работающих в системе процессов и информацию о них.

htop — продвинутый монитор процессов, написанный для Linux. Он был задуман заменить стандартную программу top. Htop показывает динамический список системных процессов, список обычно выравнивается по использованию ЦПУ. В отличие от top, htop показывает все процессы в системе.

8. Назовите и дайте характеристику команде поиска файлов. Приведите примеры использования этой команды.

Для поиска файлов используется команда find.  
Формат команды:
```
find путь [-опции]  
```
Путь определяет каталог, начиная с которого по всем подкаталогам будет вестись
поиск.

Например, вывести на экран имена файлов из вашего домашнего каталога и его подкаталогов, начинающихся на f:
```
find ~ -name "f*" -print
```
9. Можно ли по контексту (содержанию) найти файл? Если да, то как?

Команда grep способна обрабатывать стандартный вывод других команд
(любой текст). Для этого следует использовать конвейер, связав вывод команды с вводом grep.

Например, показать строки во всех файлах в вашем домашнем каталоге с именами, начинающимися на f, в которых есть слово begin:
```
grep begin f*
```
10. Как определить объем свободной памяти на жёстком диске?

df -h — данная команда отобразит информацию об объеме свободной памяти на диске в удобном формате. При использовании этой команды, дисковое пространство будет показано в Гб.

11. Как определить объем вашего домашнего каталога?

Определить объем домашнего каталога можно с помощью команды du ~.

12. Как удалить зависший процесс?

С помощью kill xxx, где xxx - код процесса.

# Выполнение лабораторной работы

Записываем в file.txt имена всех файлов в папке /etc/.

![Рис.1](image\picture1.png)  

Дозаписываем в тот же файл имена файлов домашней папки.

![Рис.2](image\picture2.png)  

Записываем в файл conf.txt те файлы из file.txt, которые оканчиваются на .conf.

![Рис.3](image\picture3.png) 

Выводим несколькими способами имена файлов домашней папки, начинающихся на с.

![Рис.4](image\picture4.png)  

Выводим файлы папки /etc/, начинающиеся на h.

![Рис.5](image\picture5.png)

Запускаем в фоновом режиме процесс записи в файл logfile всех файлов домашней папки, начинающихся на log.

![Рис.6](image\picture6.png)  

Удаляем logfile.

![Рис.7](image\picture7.png)  

Запускаем в фоновом режиме gedit.

![Рис.8](image\picture8.png)  

Находим номер процесса gedit с помощью ps и grep.

![Рис.9](image\picture9.png)

Завершаем процесс gedit.

![Рис.10](image\picture10.png)

Читаем справку по командам.

![Рис.11](image\picture11.png)

Используем команды.

![Рис.12](image\picture12.png)  

Выводим все репозитории домашней папки.

![Рис.13](image\picture13.png)  

# Выводы

Благодаря данной работе я ознакомилась с инструментами поиска файлов и фильтрации текстовых данных.
Приобрела практические навыков по управлению процессами (и заданиями), по
проверке использования диска и обслуживанию файловых систем.
