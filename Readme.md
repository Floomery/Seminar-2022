# Инструкция по работе с git

## Что такое git
**Git** — система управления версиями с распределенной архитектурой. В отличие от некогда популярных систем вроде CVS и Subversion (SVN), где полная история версий проекта доступна лишь в одном месте, в Git каждая рабочая копия кода сама по себе является репозиторием. Это позволяет всем разработчикам хранить историю изменений в полном объеме. Самой распространенной реализацией ***Git*** является (GitHub)[https://github.com]

## Подготовка репозитория 
Для создания нового репозитория используется команда **git init**. Команду **git init** выполняют только один раз для первоначальной настройки нового репозитория. Выполнение команды приведет к созданию нового подкаталога (.git) в вашем рабочем каталоге. Кроме того, будет создана новая главная ветка.

## Создание коммитов
Для создания новой фиксации коммита используется команда git commit. Для этого в терминале в папке-репозитория пишем git commit -m "сообщение к коммиту". Сообщение к коммиту ***Обязательно!***

### Дабовление файлов к комитту
Для добавления файла к новому коммиту используется команда **git add** используется она следующим образом: в терминале с папкой-репозиторием пишем git add <название файла>

## Перемещение между комиттами
Для перемещения на другую фиксацию(коммит) используется команда **git checkout**. Для этого необходимо как показано в прошлом пункте в журнале изменений найти необходимый хэш(номер) после чего в папке надо написать **git checkout**, после выполнения этой команды мы попадаем в состояние *detached head*, в котором никакие следующие коммиты сораняться не будут. Для выхода из этого состояния необходимо ввести **git checkout master**. 

## Журнал сохранений
После того, как вы создали несколько коммитов или же клонировали репозиторий с уже существующей историей коммитов, вероятно вам понадобится возможность посмотреть что было сделано — историю коммитов. Одним из основных и наиболее мощных инструментов для этого является команда **git log**.

## Ветки в git
Ветки в Git — это простой перемещаемый указатель на один из таких коммитов. По умолчанию, имя основной ветки в Git — **master**. Как только вы начнёте создавать коммиты, ветка master будет всегда указывать на последний коммит. Каждый раз при создании коммита указатель ветки master будет передвигаться на следующий коммит автоматически.

## Создание веток 
Что же на самом деле происходит при создании ветки? Всего лишь создаётся новый указатель для дальнейшего перемещения. Допустим вы хотите создать новую ветку с именем testing. Вы можете это сделать командой **git branch**

## Разрешение конфликтов
Самый простой способ разрешить конфликт — отредактировать конфликтующий файл. 

## Стирание веток
Чтобы удалить локальную ветку GIT, вы можете выполнить одну из следующих команд:

*git branch -d branch_name*

*git branch -D branch_name*

Как вы можете заметить, эти команды, в разных вариациях использования, имеют 2 разных аргумента, d и D.

Параметр **d** означает **delete**, который удалит локальную ветвь, только в случае, если вы смерджили её с какой-то из веток.

Опция **D** обозначает **delete force**, которая удаляет ветку независимо от ее статуса push или merge, так что будьте осторожны при её использовании!

## Решение конфликта
