# Инструкция для работы с **Git**

## Что такое Git и зачем он нужен?
Git - это консольная утилита, для отслеживания и ведения истории изменения файлов, в вашем проекте. Чаще всего его используют для кода, но можно и для других файлов. Например, для картинок - полезно для дизайнеров.

С помощью **Git**-a вы можете откатить свой проект до более старой версии, сравнивать, анализировать или сливать свои изменения в репозиторий.

**Репозиторием** называют хранилище вашего кода и историю его изменений. Git работает локально и все ваши репозитории хранятся в определенных папках на жестком диске.

## Создание **репозитория**

Для начала нужно перейти в папку, которая не находится под версионным контролем Git. 

Для разных операционных систем это выглядит по-разному:

для Linux:

* $ cd /home/user/my_project
для macOS:

* $ cd /Users/user/my_project
для Windows:

* $ cd C:/Users/user/my_project

Затем выполните команду:

* $ git init

Эта команда создаёт в текущем каталоге новый подкаталог с именем **.git**, содержащий все необходимые файлы репозитория - структуру Git репозитория.

## Создание **коммитов** 

В первую очередь следует добавить под версионный контроль существующий файл, для этого в терминале нужно ввести:

* $ git add "file_name"

Где "file_name" это имя файла без кавычек.

Далее выполнить следующую команду:
* $ git commit -m "Коментарий" 

## Просмотр истории **коммитов**

Одним из основных инструментов для того, чтобы посмотреть что было сделано, является команда **git log**.
* $ git log

Команда **git log** перечисляет коммиты, сделанные в репозитории в обратном к хронологическому порядке — последние коммиты находятся вверху.  

## Ветвление

Во время разработки новой функциональности считается хорошей практикой работать с копией оригинального проекта, которую называют веткой. Ветви имеют свою собственную историю и изолированные друг от друга изменения до тех пор, пока вы не решаете слить изменения вместе.

### Создание новой ветки

Основная ветка в каждом репозитории называется master. Чтобы создать еще одну ветку, используем команду "branch 'name'":

* $ git branch amazing_new_feature

### Переключение между ветками

Для работы с новой веткой воспользуемся командой "**checkout**", она принимает один параметр — имя ветки, на которую необходимо переключиться.

* $ git checkout amazing_new_feature

### Слияние веток

Для слияния веток нужно воспользоваться командой "**merge**"

* $ git merge amazing_new_feature

### Удаление ветки в Git

Бывают ситуации, когда после слива каких-то изменений из рабочей ветки в исходную версию проекта, ее, по правилам хорошего тона, необходимо удалить, чтобы она более не мешалась в вашем коде. Но как это сделать?
Для локально расположенных веток существует команда:

* $ git branch -d local_branch_name 
