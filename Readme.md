# Инструкция по работе с Git и с GitHub


## Что такое *Git*?
*Git* - одна из реализаций распределённых систем контроля версий, позволяющая организовать версионность, как локально, так и на удалённом серевере. Самая популярная платформа, реализующая *Git*,- [GitHub](https://github.com)

## Подготовка репозитория
Для создания в папке репозитория необходимо открыть эту папку в терминале и написать команду *git init*, после чего в этой папке создасться скрытая папка *.git*, и таким образом папка станет репозиторием


## Создание коммитов

### Просмотр состояния репозитория
Для просмотра состояния репозитория используется команда *git status*. В терминале с открытой папкой-репозиторием необходимо написать команду *git status*. В результате можно увидеть следующие выводы:
1. On branch *** nothing to commit - это означает нет активных изменений
2. Untracked file - это означает, что имеются файлы, не отслеживаемые системой контроля версий
...

### Добавление файла к коммиту
Для того, чтобы добавить файл к "сохранению", необходимо использовать команду *git add*. В терминале с открытой папкой-репозиторием необходимо написать *git add <название файла>*, и этот файл добавится к "сохранению"


### Создание фиксации
Для создания фиксации используется команда *git commit*. Для этого в терминале с папкой-репозиторием необходимо написать команду *git commit -m <сообщение к коммиту>*. Сообщение к коммиту писать **ОБЯЗАТЕЛЬНО**.


## Журнал изменений
Для просмотра истории изменений используется команда *git log*. Для этого в терминале с папкой-репозиторием необходимо написать *git log*, и Вы увидите список всех коммитов в этой ветке с описанием: имени, электронной почты, сообщением к коммиту и номер коммита.

## Перемещение между коммитами
Для перемещения между коммитами испозуется команда *git checkout*. Для этого в терминале с папкой-репозиторием необходимо написать *git checkout <номер коммита>*. Номер коммита берётся из журнала изменений ветки.

## Ветки в git
### Создание ветки
Для того, чтобы создать новую ветку используется команда *git branch*. Для этого терминале с папкой-репозиторием необходимо написать *git branch <название вертки>* и таким образом создасться новая ветка, но вы останетесь в исходной.

## Просмотр списка веток
Для того, чтобы просмотреть список веток в локальном репозитории, используется команда *git branch*. Для этого в терминале с папкой-репозиторием, напишите *git branch*, и тогда Вы увидите список всех Ваших локальных веток. Зелёным цветом и звёздочкой будет выделена ветка, на которой Вы сейчас стоите. Фалг *-a* позволяет посмотреть все ветки в том числе и в удалённом репозитории.

### Переключение между ветками
Для того, чтобы переключиться на другую ветку, используется команда *git checkout*. Для этого в терминале с папкой-репозиторием необходимо написать *git checkout <название ветки>*, и тогда Вы перейдёте в указанную ветку. Для переключения между ветками, ветка должна **СУЩЕСТВОВАТЬ**, и в текущий ветке **НЕ ДОЛЖНО** быть активных изменений


## Слияние веток и решение конфликтов
 Для того чтобы совместить (реализовать слияние) ветки можно использовать команду *git merge <название ветки>*. Это можно делать как с основной так и остальных ветках, однако если у вас есть разные данные в одном и том же разделе разных веток, то может произойти конфликт. При слиянии появиться сообщение и для решения конфликта можно редактировать информацию как вам нужно и сохранить коммит далее.
 
## Удаление веток
Для удаления веток используетя команда *git branch -d <название ветки>*.

## Работа с GitHub
Работа с удаленными репозиториями. Копировать внешний репозиторий на свой ПК можно командой git clone и ссылка на репо.
git pull - Эта команда позволяет скачать все из текущего репозитория и автоматически сделать merge с нашей версией
git push - Эта команда позволяет отправить нашу версию репозитория на внешний репозиторий. ТРЕБУЕТ АВТОРИЗАЦИИ на внешнем репозитории.

### Отправка данных на GitHub с локального репозитория
Для того чтобы отправить ваши файлы на удаленный репозитории на вам нужно авторизоваться на GitHub. После чего написать команду git push origin master, в ходе отправки возникнит конфликт его можно решить за счет команды. Однако данный алгоритм подходит для небольших совметсных проектов. Если у вас будут работать над проектом много людей одновременно то ваши файлы не возможно будет отправить. Чтобы решить эту проблему необходимо подрузить свежие данные, произвести изменения и затем совершить команду обратно.

### Загрузка данных на локальный репозитории
Загружить файлы на удаленный репозитория можно с помощью команды git remote add origin и ссылки на эту репозиторию. 

### Работа репозиториями на GitHUb
На платформе есть большое количество репозитории и прочих проектов с которыми вы могли поработать. Для этого есть функция *fork* на панеле которая создает копию интересующей репо и после чего вы можете делать изменения на копии. Когда вы закончите работу над файлом мы можете отправить ваши предложения через функция *pull request* и у автора есть возможность дать коментарии (Comment), одобрить (Approve) либо отправить на доработку (Request changes) ваши предложения.
