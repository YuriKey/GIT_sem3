# Инструкция для работы с Git и удалёнными репозиториями

## Что такое Git?
------------------
> Git - это одна из реализаций распределённых систем контроля версий, имеющая как и локальные, так и удалённые репозитории. Является самой популярной реализацией систем контроля версий в мире.

## Подготовка репозитория
--------------------
Для создание репозитория необходимо выполнить команду **git init**  в папке с репозиторием и у Вас создатся репозиторий (появится скрытая папка .git)

## Коммиты
----------

> Коммит - контрольная точка, сохранение изменений.
    
### Git add
Для добавления измений в коммит используется команда **git add**. Чтобы использовать команду *git add* напишите **git add <имя файла>**. Для добавления изменений во всех файлах репозитория необходимо ввести команду **git add .** .

### Просмотр состояния репозитория
Для того, чтобы посмотреть состояние репозитория используется команда **git status**. Вы увидите были ли измения в файлах, или их не было.

### Создание коммитов
Для того, чтобы создать коммит(сохранение) необходимо выполнить команду **git commit**. Выполняется она так: **git commit -m "<сообщение к коммиту>**. Все файлы для коммита должны быть ***ДОБАВЛЕНЫ*** и сообщение к коммиту писать ***ОБЯЗАТЕЛЬНО***.

### Перемещение между сохранениями
Для того, чтобы перемещаться между коммитами, используется команда **git checkout**. Используется она в папке с репозиторием следующим образом: **git checkout <номер коммита>**

## Журнал изменений
--------------------
Для того, чтобы посмтреть все сделанные изменения в репозитории, используется команда **git log**. Для этого достаточно выполнить команду **git log** в папке с репозиторием

## Ветки в Git
----------------

### Создание ветки

Для того, чтобы создать ветку, используется команда **git branch**. Делается это следующим образом в папке с репозиторием: **git branch <new_branch_name>** Второй способ создания ветки - ввести команду **git checkout -b <new_branch_name>**. В этом случае после создания ветки git автоматически перейдет в эту ветку.

## Слияние веток

Для того чтобы дабавить ветку в текущую ветку используется команда **git merge <branch_name>**

## Удаление веток
Для удаления ветки ввести команду **git branch -d <branch_name>**

## Работа с удаленными репозиториями
-------------------------------------
>Для совместной работы над *open source* и прочими проектами используют сервисы удаленной работы с репозиториями: GitLab, GitHub и т.д.

### Начало работы с GitHub

* Для того, чтобы данные работы в VSC принимались и отправлялись на GitHub, необходимо авторизваться на GH через VSC.
* Для того, чтобы соотнести репозитории на ПК и GH, надо создать на обоих ресурсах новые репозитории и либо

    а) ввести предлагаемый на GB код в терминал, либо

    б) сопоставить их через source control.

### Команда clone

Команда **git clone <ссылка на репозиторий>** выполняет копирование файлов удаленного репозитория на локуальный ПК.

### Команда push

Команда **git push** выполняет отправку коммита в удаленный репозиторий.

### git pull
Команда **git pull** выполняет скачивание информацию с удаленного репозитория. ***ВНИМАНИЕ!*** В случае введения **pull** git пытается слить ветки. Соответственно, в случае конфликта версий предлагается этот кофлит решить.

### Алгоритм работы с _open source_ проектами
Иногда возникает необходимость или желание поучаствовать в каком-либо проекте, выложенном на GH, и предложить своё видение какой-либо фичи, указать на какую-либо ошибку и т.д. Чтобы это сделать, необходимо

* скопировать чужой репозиторий в свой с помощью кнопки "fork" 

* скачать репозиторий на ПК из VSC с помощью команды **clone**

* создать новую ветку, произвести в ней изменения

* отправить на GH с помощью команды **push**

* отправить на рассмотрение создателю проекта с помощью кнопки "Compare & pull request" на GH
