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
Чтобы посмотреть журнал изменений, необходимо воспользоваться комнадой *git log*. По итогам выполнения этой команды в окне терминала нам будет предосталвен полный перечень выполненных ранее нами изменений. О том, как между ними перемещаться - см. выше. 
также, есть такая команда как *git diff* и *git show* , которые смогут отразить в терминале разницу или отличия между сделаннами в разное время изменениями.

# Ветки в Git

 Для создания ветки нам необходимо понять, какие вообще ветки у нас есть и на какой находимся мы. Вдруг уже кто-то что-то создал?
 *git branch*  - та самая волшебная команда, которая покажет нам все существующие ветки и отметит звездочкой, на какой же находимся мы.
 Для создания новой ветки необходимо выполнить команду *git branch name_of_the_branch*. После выполнения не заубдь переключиться на новую ветку, если ты хочешь в ней сразу работать.
 
# Слияние веток и решение конфликтов
Поработав на одной из созданных веток ( то есть она уже отличается от оригинала), есть необходимость переноса информации или слияния всех веток. 
Для слияния двух веток необходимо применить команду *git merge hame_of_branch* , но, следует обратить особое внимание, что выполняем слияние на той ветке, к которой хотим применить слияние. После слияния двух веток возможно возникновение конфликта - когда на одних и тех же строках присуствует текст и git спросить, какой вариант оставить, текущую версию, версию из той ветки или оба изменения оставить. 
После выбора одного из трех вариантов необходимо создать коммит.

# Удаление веток
После внесения изменений и последующего слияния веток возникает необходимость в удалении всех ненужных веток. *git branch -d name_of_branch* прекрасно справится с этой задачей. По итогам выполнения этой комнады указанная ветка будет успешно удалена.

# Работа с удаленным репозиторием (GitHub)
Сущесвтует такая возможность совместной работы над документом или просто возникла необходимость предоставить свое "творение" на обозрение миру. Чтобы осуществить такие возможности или пожелания необходимо воспользоваться сайтом GitHub. регистрация на сайте обязательна, создается свой профиль, в котором как раз и ***будут хранится ваши наивеличайшие мылсли***. 
После регистрация на сайте вы уже можете пробовать что-то свое создавать или воспользоваться чужими мыслями ( то есть ссылками), внести туда свою лепту, например, и загрузить обратно, то есть предложить что-то свое автору, еоторый сможет увидеть внесенный изменения и принять решение , оставлять данное изменение или нет. также будет и с вашими файлами, вынесенными на всеобщее обозрение. Вы делитесь, кто-то комментирует и отправляет обратно измененный файл со своими идеями, предложениями, замечаниями или просто свое "фи".
Далее расскажу здесь (попробую даже вставить картинки с сайта), как поэтапно создать свой репозиторий на GitHub:
1. заходим на сайт GitHub  *(вернусь в прошлые лекции, забыла как картинки вставлять...) и потом продолжу заходить на сайт и писать...*
![стартовая страница сайта](StartPageGitHub.png)   Получилось)))
2. Слева в верхнем углу страницы есть кнопка NEW (зеленая), на картинке выше обведена красной линией. Нажимаем на эту кнопку и создаем новый репозиторий вот так ![создание нового репозитория](Pic1CreatRep.png)
справа от наименования Вашего профиля придумываем имя для Вашего репозитория, спускаемся вниз (пока самовольно ничего не жмем), и нажимаем опять зеленую кнопочку (вообще зеленая кнопка - это тема).
Поздравляю, репозиторий создался (чудом, сам) ![выглядит вот так](Pic2CreatRep.png)
3. Для привязки репозитория к нужному файлу ( в VScode) необходимо выполнить комнады (Гит дает подсказки и можно просто скопировать эти команды в терминал и все будет ок, но я сделаю снимок экрана ![вот такой](Pic3CreatRep.png), но и пропишу тут комнады для вставки (себе на память и на случай, если Гит окажется не расположен ко мне и уберет эти подсказки:
* git remote add origin https://github.com/ZauYana/DocForWrittingHW3.git
* git branch -M main
* git push -u origin main
или еще вариант 
* echo "# DocForWrittingHW3" >> README.md
* git init
* git add README.md
* git commit -m "first commit"
* git branch -M main
* git remote add origin https://github.com/ZauYana/DocForWrittingHW3.git
* git push -u origin main  )
Вставляем в терминал (я тоже это сделала и о чудо!) и забыла добавить - на сайте GitHub надо обновить страницу и отобразится тот файл, который вы привязали из VSCode. 
4. Далее мы можем вносить изменения как на сайте ГитХаб, так и в файле в VSCode, но надо соображать , что внося изменения на одном из ресурсов и не обновляя с помощью команд сопряженный друг с другом репозиторий не стоит ожидать автоматического изменения на противоположном конце. рассмотрим два варианта:

___Изменения вносятся на GitHub___

 Здесь, на сайте открываем доступ к редактированию этого файла (значок карандашека в правом углу). После чего вносим все что нашей душе угодно и внизу страницы видим предложение ГитХаба добавить коммит к внесенным изменениям, мы конечно же вносим данный коммит (коммит придумывать каждый раз надо самому, какая прекрасная тренировка креативности, развивай, энджой). После того, как добавили текст и сделали коммит, жмем опять на зеленую кнопку, мы помним, что _зеленая кнопка - это тема_?   Работа с изменениями на GitHub окончена, мы переходим в VSCode и там необходимо в терминале отработать команду  __git pull__ после нее все изменения из ГитХаба перетянутся в VSC. (Сейчас я все это проделаю, изменения вносила на сайте).  

___Изменения вносим в VSC___

Внесенные изменения в VSC также добавляются и коммитится, а далее просто через конмаду в терминале _git push_ передаются на ГитХаб. На сайте не забываем обновлять страницу! 