## Что такое git

Система контроля версий

*Cистема контроля версий (VCS)* — программное обеспечение для облегчения работы с изменяющейся информацией.

* Полная история изменений каждого файла за длительный период. Это касается всех изменений, внесенных огромным количеством людей за долгие годы. Изменением считается создание и удаление файлов, а также редактирование их содержимого. Различные инструменты VCS отличаются тем, насколько хорошо они обрабатывают операции переименования и перемещения файлов. В историю также должны входить сведения об авторе, дата и комментарий с описанием цели каждого изменения. Наличие полной истории позволяет возвращаться к предыдущим версиям, чтобы проводить анализ основных причин возникновения ошибок и устранять проблемы в старых версиях программного обеспечения. 
* Ветвление и слияние. Создание «веток» позволяет иметь несколько независимых друг от друга направлений разработки, а также выполнять их слияние, чтобы разработчики могли проверить, что изменения, внесенные в каждую из веток, не конфликтуют друг с другом. Многие команды разработчиков программного обеспечения создают отдельные ветки для каждой функциональной возможности, для каждого релиза либо и для того, и для другого. 
* Отслеживаемость. Возможность отслеживать каждое изменение, внесенное в программное обеспечение, и связывать его с ПО для управления проектами и отслеживания ошибок. История с комментариями во время чтения кода помогает понять, что этот код делает и почему действие реализовано именно таким образом. Благодаря этому разработчики могут вносить корректные и совместимые изменения в соответствии с долгосрочным планом разработки системы. 

# Подготовка репозитория

создаем заново или выбираем папку, открываем ее в VS и создаем там файлик. Файл создаем с именем и расширением .md
Далее, обязательно используем команду git init.

Все, после выполнения этой команды и создания папки и файла у нас создан репозиторий и он инициализирован Git. 

добавлено то, что из файла (то есть не отсебятина): 
Подготовка к работе
1.	Скачать и установить VS Code https://code.visualstudio.com/docs/?dv=win
2.	Скачать и установить Git https://git-scm.com/download/win
3.	Проверить, работает ли git  с помощью команды 
git --version
4.	Добавить имя и email пользователя с помощью команд
  git config --global user.email "email@mail.com"
  git config --global user.name "User Name"


# Создание "сохранений"


Такого я еще не писала!! ***а вот этот текст исключительно для конфликта***

Такого я еще не писала!! 
# а тут вот тут сделаю подставу
Сохранение и восстановление незавершённых изменений

$ git stash

Временно сохраняет все незафиксированные изменения отслеживаемых файлов

$ git stash pop

Восстанавливает состояние ранее сохранённых версий файлов

$ git stash list

Выводит список всех временных сохранений

$ git stash drop

Сбрасывает последние временно сохранённыe изменения

# Перемещение между сохранениями

Для того, чтобы перемещаться между сохранениями, а точнее коммитами ( мы же помним, что к каждому сохранению мы пишем свой коммит), необходимо сначала ввести команду **git log**. На экарне мы увидим всю историю сохранений, а точнее всю сохранений, которые закоммичены. выбираем необходимый нам коммит, к нему привязан уникальный код или беспорядочный набор (только для нас беспорядочный) цифр. Копируем как минимум первые 4 цифры нужного нам коммита. Вводим команду **git checkout 4 цифры скопированные** и переходим на выбранный коммит. вводим необходимые изменения и вуаля, что мы имеем, измененный коммит и мы профи)

# Журнал изменений

Название говорит само за себя. 

И так, чтобы посмотреть журнал изменений, необходимо воспользоваться комнадой *git log*.  **исключительно для конфликта, пркатика же**

# Ветки в Git
# Слияние веток и решение конфликтов
# Удаление веток
