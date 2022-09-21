# Инструкция для работы с Git и удалёнными репозиториями

## Что такое Git? 
Git - это одна из реализаций распределённых систем контроля версий, имеющая как и локальные, так и удалённые репозитории. Является самой популярной реализацией систем контроля версий в мире.

Итак, рассмотрим принцип работы Git и базовые понятия подробнее.

## Репозиторий
### ***Git innit***

Репозиторий Git - это папка, в которой Git отслеживает изменения (дополнения/удаления и т.д.), вносимые в разрабатываемый проект. 

## Подготовка репозитория
Создать репозиторий можно несколькими способами: 
+ **создание репозитория в существующем каталоге** - для этого необходимо выполнить команду *git init*  в папке с репозиторием и у Вас создаться репозиторий (появится скрытая папка .git)
+ **клонирование существующего репозитория** - для получения копии существующего Git-репозитория используйте команду git clone.

## Коммиты 
## Git commit -m "message"

Коммит - одно из базовых понятий Git, которое представляет снимок текущего состояния изменений, добавленных в раздел проиндексированных файлов. 

Для создания коммита необходимо выполнить следующие шаги: 
1. Добавтить изменения с помощью команды  __*git add <имя файла>*__
2. Просмотреть состояние репозитория и убедиться, что изменения отображаются - для этого используйте команду __*git status*__.
3. Создайте коммит и тем самым зафиксируйте в системе Git все необходимые изменения. Для создания коммита используйте команду __*git commit -m "<сообщение к коммиту>*__, где *"сообщение к коммиту"* - **обязательное** название Вашего изменения, например: *git commit -m "First Edition"*

Обратите внимание, что все файлы для коммита должны быть ***ДОБАВЛЕНЫ***, как указано выше в пункте 1, иначе система не увидит изменений, доступных для добавления в коммит. 

## Перемещение между коммитами
## Git checkout <commit name>

Для того, чтобы перемещаться между коммитами, используется команда __*git checkout*__. Используется она в папке с репозиторием следующим образом: *git checkout <номер коммита>*.
Для того, чтобы вернуться из просматриваемого коммита в текущий - необходимо выполнить команду __*git checkout master*__.

## Журнал изменений
## Git log

Все сохраненные изменения в репозитории можно просмотреть в журнале изменений - для просмотра журнала используйте команду __*git log*__ в папке с репозиторием. 

## Ветвления в Git

Ветвления реализуют возможность отклонения от основной линии разработки (т.н. "чистовика") для продолжения внесения изменений в проект, но без вмешательства в основную линию. Иначе говоря, прежде чем писать в чистовик, Вы решаете задачу в черновике. 

### Создание ветки

Для того, чтобы создать ветку, используется команда __*git branch*__, т.е. для создания ветки Вы должны в папке с репозиторием ввести команду и придумать название новой ветви: *git branch <название новой ветки>*

## Слияние веток

Когда закончены черновые работы и Вам необходимо объединить основную ветку и ту ветку, в которой Вы работали, необходимо выполнить следующие команды: 
+ вернуться на основную ветку, используя команду __*git checkout master*__ 
+ на основной ветви ввести команду __*git merge*__ и указать имя ветви, которую необходимо добавить к основной - *git merge <название ветки>*

## Удаление веток
Когда все необходимые слияния выполнены и дополнительные ветви больше не нужны, их можно удалить.
Для удаления ветки необходимо ввести команду __*"git branch -d*__ с указанием имени ответвления - *git branch -d 'name branch'"*.

# Enjoy your work with Git ! 
![Git!](Git.png)