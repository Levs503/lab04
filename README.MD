levs503@levs503-MSI:~$ echo ${PATH}
/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin
levs503@levs503-MSI:~$ echo ${GITHUB_USER}

levs503@levs503-MSI:~$ export GITHUB_USERNAME=LevS503
levs503@levs503-MSI:~$ export GITHUB_EMAIL=semkov01@mail.ru
levs503@levs503-MSI:~$ export GITHUB_TOKEN=a94d89fcbe79b3f6ed76cc993fcac740e95d5f6c
levs503@levs503-MSI:~$ alias edit=nano
levs503@levs503-MSI:~$ cd LevS503/workspace/
levs503@levs503-MSI:~/LevS503/workspace$ source scripts/activate 
levs503@levs503-MSI:~/LevS503/workspace$ mkdir ~/.config
mkdir: невозможно создать каталог «/home/levs503/.config»: Файл существует
levs503@levs503-MSI:~/LevS503/workspace$ cat > ~/.config/hub <<EOF
> github.com:
> - user: $:{GITHUB_USERNAME}
> oauth_token: ${GITHUB_TOKEN}
> protocol: https
> EOF
levs503@levs503-MSI:~/LevS503/workspace$ git config --global hub.protocol https

Command 'git' not found, but can be installed with:

sudo apt install git

levs503@levs503-MSI:~/LevS503/workspace$ sudo apt install git
[sudo] пароль для levs503: 
Чтение списков пакетов… Готово
Построение дерева зависимостей       
Чтение информации о состоянии… Готово
Следующие пакеты устанавливались автоматически и больше не требуются:
  libfwup1 libwayland-egl1-mesa
Для их удаления используйте «sudo apt autoremove».
Будут установлены следующие дополнительные пакеты:
  git-man liberror-perl
Предлагаемые пакеты:
  git-daemon-run | git-daemon-sysvinit git-doc git-el git-email git-gui gitk
  gitweb git-cvs git-mediawiki git-svn
Следующие НОВЫЕ пакеты будут установлены:
  git git-man liberror-perl
Обновлено 0 пакетов, установлено 3 новых пакетов, для удаления отмечено 0 пакетов, и 24 пакетов не обновлено.
Необходимо скачать 4 738 kB архивов.
После данной операции объём занятого дискового пространства возрастёт на 33,9 MB.
Хотите продолжить? [Д/н] Д    
Пол:1 http://ru.archive.ubuntu.com/ubuntu bionic/main amd64 liberror-perl all 0.17025-1 [22,8 kB]
Пол:2 http://ru.archive.ubuntu.com/ubuntu bionic-updates/main amd64 git-man all 1:2.17.1-1ubuntu0.5 [803 kB]
Пол:3 http://ru.archive.ubuntu.com/ubuntu bionic-updates/main amd64 git amd64 1:2.17.1-1ubuntu0.5 [3 912 kB]
Получено 4 738 kB за 1с (3 967 kB/s)       
Выбор ранее не выбранного пакета liberror-perl.
(Чтение базы данных … на данный момент установлен 174191 файл и каталог.)
Подготовка к распаковке …/liberror-perl_0.17025-1_all.deb …
Распаковывается liberror-perl (0.17025-1) …
Выбор ранее не выбранного пакета git-man.
Подготовка к распаковке …/git-man_1%3a2.17.1-1ubuntu0.5_all.deb …
Распаковывается git-man (1:2.17.1-1ubuntu0.5) …
Выбор ранее не выбранного пакета git.
Подготовка к распаковке …/git_1%3a2.17.1-1ubuntu0.5_amd64.deb …
Распаковывается git (1:2.17.1-1ubuntu0.5) …
Настраивается пакет git-man (1:2.17.1-1ubuntu0.5) …
Настраивается пакет liberror-perl (0.17025-1) …
Настраивается пакет git (1:2.17.1-1ubuntu0.5) …
Обрабатываются триггеры для man-db (2.8.3-2ubuntu0.1) …
levs503@levs503-MSI:~/LevS503/workspace$ git --help
использование: git [--version] [--help] [-C <path>] [-c <name>=<value>]
           [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]
           [-p | --paginate | --no-pager] [--no-replace-objects] [--bare]
           [--git-dir=<path>] [--work-tree=<path>] [--namespace=<name>]
           <command> [<args>]

Стандартные команды Git используемые в различных ситуациях:

создание рабочей области (смотрите также: git help tutorial)
   clone      Клонирование репозитория в новый каталог
   init       Создание пустого репозитория Git или переинициализация существующего

работа с текущими изменениями (смотрите также: git help everyday)
   add        Добавление содержимого файла в индекс
   mv         Перемещение или переименование файла, каталога или символьной ссылки
   reset      Сброс текущего состояния HEAD на указанное состояние
   rm         Удаление файлов из рабочего каталога и индекса

просмотр истории и текущего состояния (смотрите также: git help revisions)
   bisect     Выполнить двоичный поиск изменения, которое вносит ошибку
   grep       Вывод строк, соответствующих шаблону
   log        Вывод истории коммитов
   show       Вывод различных типов объектов
   status     Вывод состояния рабочего каталога

выращивание, отметка и настройка вашей общей истории
   branch     Вывод списка веток,  их создание или удаление
   checkout   Переключение веток или восстановление файлов в рабочем каталоге
   commit     Запись изменений в репозиторий
   diff       Вывод разницы между коммитами, коммитом и рабочим каталогом и т.д.
   merge      Объединение одной или нескольких историй разработки вместе
   rebase     Повторно применить коммиты над верхушкой другой ветки
   tag        Создание метки, вывод списка, удаление или проверка метки, подписанной с помощью GPG

совместная работа (смотрите также: git help workflows)
   fetch      Загрузка объектов и ссылок из другого репозитория
   pull       Извлечение изменений и объединение с другим репозиторием или локальной веткой
   push       Обновление внешних ссылок и связанных объектов

«git help -а» и «git help -g» выводит список доступных подкоманд и
некоторые руководства по темам. Запустите «git help <команда>» или
«git help <термин>», чтобы прочесть о конкретных подкоманде или теме.
levs503@levs503-MSI:~/LevS503/workspace$ git help --global
error: unknown option `global'
использование: git help [--all] [--guides] [--man | --web | --info] [<команда>]

    -a, --all             вывести список всех доступных команд
    -g, --guides          вывести список полезных руководств
    -m, --man             открыть руководство в формате man
    -w, --web             открыть руководство в веб-браузере
    -i, --info            открыть руководство в формате info

levs503@levs503-MSI:~/LevS503/workspace$ git config --global hub.protocol https
levs503@levs503-MSI:~/LevS503/workspace$ echo ${hub.protocol}
bash: ${hub.protocol}: неверная подстановка
levs503@levs503-MSI:~/LevS503/workspace$ git config --global --get hub.protocol
https
levs503@levs503-MSI:~/LevS503/workspace$ ды
ды: команда не найдена
levs503@levs503-MSI:~/LevS503/workspace$ ls
node  projects  reports  scripts  tasks
levs503@levs503-MSI:~/LevS503/workspace$ mkdir projects/lab02 && cd projects/lab02
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ git --help
использование: git [--version] [--help] [-C <path>] [-c <name>=<value>]
           [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]
           [-p | --paginate | --no-pager] [--no-replace-objects] [--bare]
           [--git-dir=<path>] [--work-tree=<path>] [--namespace=<name>]
           <command> [<args>]

Стандартные команды Git используемые в различных ситуациях:

создание рабочей области (смотрите также: git help tutorial)
   clone      Клонирование репозитория в новый каталог
   init       Создание пустого репозитория Git или переинициализация существующего

работа с текущими изменениями (смотрите также: git help everyday)
   add        Добавление содержимого файла в индекс
   mv         Перемещение или переименование файла, каталога или символьной ссылки
   reset      Сброс текущего состояния HEAD на указанное состояние
   rm         Удаление файлов из рабочего каталога и индекса

просмотр истории и текущего состояния (смотрите также: git help revisions)
   bisect     Выполнить двоичный поиск изменения, которое вносит ошибку
   grep       Вывод строк, соответствующих шаблону
   log        Вывод истории коммитов
   show       Вывод различных типов объектов
   status     Вывод состояния рабочего каталога

выращивание, отметка и настройка вашей общей истории
   branch     Вывод списка веток,  их создание или удаление
   checkout   Переключение веток или восстановление файлов в рабочем каталоге
   commit     Запись изменений в репозиторий
   diff       Вывод разницы между коммитами, коммитом и рабочим каталогом и т.д.
   merge      Объединение одной или нескольких историй разработки вместе
   rebase     Повторно применить коммиты над верхушкой другой ветки
   tag        Создание метки, вывод списка, удаление или проверка метки, подписанной с помощью GPG

совместная работа (смотрите также: git help workflows)
   fetch      Загрузка объектов и ссылок из другого репозитория
   pull       Извлечение изменений и объединение с другим репозиторием или локальной веткой
   push       Обновление внешних ссылок и связанных объектов

«git help -а» и «git help -g» выводит список доступных подкоманд и
некоторые руководства по темам. Запустите «git help <команда>» или
«git help <термин>», чтобы прочесть о конкретных подкоманде или теме.
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ ^C
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ git init
Инициализирован пустой репозиторий Git в /home/levs503/LevS503/workspace/projects/lab02/.git/
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ git config --global user.name ${GITHUB_USERNAME}
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ git config --global user.email ${GITHUB_EMAIL}
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ git config --global --get user.name
LevS503
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ git config -e --global
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ git remote add origin https://github.com/${GITHUB_USERNAME}/lab02.git
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ git remote --help
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ git pull origin master
Username for 'https://github.com': LevS503
Password for 'https://LevS503@github.com': 
remote: Invalid username or password.
fatal: Authentication failed for 'https://github.com/LevS503/lab02.git/'
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ git pull origin master
Username for 'https://github.com': LevS503
Password for 'https://LevS503@github.com': 
remote: Repository not found.
fatal: repository 'https://github.com/LevS503/lab02.git/' not found
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ git pull origin master
Username for 'https://github.com': ovKonovalSemko123
Password for 'https://ovKonovalSemko123@github.com': 
remote: Invalid username or password.
fatal: Authentication failed for 'https://github.com/LevS503/lab02.git/'
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ git pull origin master
Username for 'https://github.com': LevS503
Password for 'https://LevS503@github.com': 
remote: Repository not found.
fatal: repository 'https://github.com/LevS503/lab02.git/' not found
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ git init
Переинициализирован существующий репозиторий Git в /home/levs503/LevS503/workspace/projects/lab02/.git/
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ git pull origin master
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Распаковка объектов: 100% (3/3), готово.
Из https://github.com/LevS503/lab02
 * branch            master     -> FETCH_HEAD
 * [новая ветка]     master     -> origin/master
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ touch --help
Использование: touch [КЛЮЧ]… ФАЙЛ…
Устанавливает временные метки доступа и изменения каждого ФАЙЛА в текущее
время.

Если ФАЙЛ не существует, то создаётся пустой, если не указаны ключи -c или -h.

Если строка аргумента ФАЙЛ равна -, то это обрабатывается специальным образом
и вызывает изменение временных меток файла, связанного со стандартным выводом.

Аргументы, обязательные для длинных ключей, обязательны и для коротких.
  -a                     изменить только время доступа
  -c, --no-create        не создавать файлов
  -d, --date=СТРОКА      проанализировать СТРОКУ и использовать вместо
                         текущего времени
  -f                     (игнорируется)
  -h, --no-dereference   изменяет символьные ссылки, а не файлы, на которые
                         они ссылаются (имеет смысл только на системах, где
                         можно изменять владельца символьной ссылки)
  -m                     изменять только время изменения
  -r, --reference=ФАЙЛ   использовать время ФАЙЛА вместо текущего времени
  -t ВРЕМЯ               использовать [[ВВ]ГГ]ММДДччмм[.сс] вместо
                         текущего времени
  --time=СЛОВО           изменить указанное время:
                         значения access, atime, use эквивалентны -a
                         значения modify, mtime эквивалентны -m
      --help     показать эту справку и выйти
      --version  показать информацию о версии и выйти

Заметьте, что ключи -d и -t используют разные форматы даты и времени.

Оперативная справка GNU coreutils: <http://www.gnu.org/software/coreutils/>
Об ошибках в переводе сообщений «touch» сообщайте по адресу <gnu@mx.ru>
Полная документация: <http://www.gnu.org/software/coreutils/touch>
или доступная локально: info '(coreutils) touch invocation'
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ touch README.md
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ git status 
На ветке master
Неотслеживаемые файлы:
  (используйте «git add <файл>…», чтобы добавить в то, что будет включено в коммит)

	README.md

ничего не добавлено в коммит, но есть неотслеживаемые файлы (используйте «git add», чтобы отслеживать их)
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ git add README.md
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ gir commit -m"added README.md"

Command 'gir' not found, did you mean:

  command 'gpr' from deb gpr
  command 'gri' from deb gri
  command 'gio' from deb libglib2.0-bin
  command 'gid' from deb id-utils
  command 'gip' from deb gip
  command 'dir' from deb coreutils
  command 'git' from deb git

Try: sudo apt install <deb name>

levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ git commit -m"added README.md"
[master cceaa8d] added README.md
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 README.md
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ git push origin master
Username for 'https://github.com': LevS503
Password for 'https://LevS503@github.com': 
Подсчет объектов: 3, готово.
Delta compression using up to 12 threads.
Сжатие объектов: 100% (2/2), готово.
Запись объектов: 100% (3/3), 278 bytes | 278.00 KiB/s, готово.
Total 3 (delta 0), reused 0 (delta 0)
remote: This repository moved. Please use the new location:
remote:   https://github.com/Levs503/lab02.git
To https://github.com/LevS503/lab02.git
   5910cab..cceaa8d  master -> master
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ touch .gitignore
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ cat > .gitignore
*build*/
*install*/
*.swp
.idea/
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ git add .gitignore
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ find --gelp
find: неизвестный предикат «--gelp»
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ find --help
Usage: find [-H] [-L] [-P] [-Olevel] [-D debugopts] [path...] [expression]

путём по умолчанию является текущий подкаталог; выражение по умолчанию: -print
выражение может состоять из операторов, параметров, тестов и действий:
операторы (в порядке уменьшения приоритета; -and берется по умолчанию, если не дано других):
      ( EXPR ) ! EXPR -not EXPR EXPR1 -a EXPR2 EXPR1 -and EXPR2
      EXPR1 -o EXPR2 EXPR1 -or EXPR2 EXPR1 , EXPR2
позиционные параметры (всегда): -daystart -follow -regextype

обычные параметры (всегда указываются раньше остальных выражений):
      -depth --help -maxdepth LEVELS -mindepth LEVELS -mount -noleaf
      --version -xdev -ignore_readdir_race -noignore_readdir_race
tests (N могут быть +N или -N или N): -amin N -anewer ФАЙЛ -atime N -cmin N
      -cnewer ФАЙЛ -ctime N -empty -false -fstype ТИП -gid N -group ИМЯ
      -ilname ШАБЛОН -iname ШАБЛОН -inum N -ipath ШАБЛОН -iregex ШАБЛОН
      -links N -lname ШАБЛОН -mmin N -mtime N -name ШАБЛОН -newer ФАЙЛ
      -nouser -nogroup -path PATTERN -perm [-/]MODE -regex PATTERN
      -readable -writable -executable
      -wholename PATTERN -size N[bcwkMG] -true -type [bcdpflsD] -uid N
      -used N -user NAME -xtype [bcdpfls]      -context КОНТЕКСТ

actions: -delete -print0 -printf FORMAT -fprintf FILE FORMAT -print 
      -fprint0 FILE -fprint FILE -ls -fls FILE -prune -quit
      -exec COMMAND ; -exec COMMAND {} + -ok COMMAND ;
      -execdir COMMAND ; -execdir COMMAND {} + -okdir COMMAND ;

Valid arguments for -D:
exec, help, opt, rates, search, stat, time, tree
Use '-D help' for a description of the options, or see find(1)

Please see also the documentation at http://www.gnu.org/software/findutils/.
You can report (and track progress on fixing) bugs in the "find"
program via the GNU findutils bug-reporting page at
https://savannah.gnu.org/bugs/?group=findutils or, if
you have no web access, by sending email to <bug-findutils@gnu.org>.
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ tree --help
usage: tree [-acdfghilnpqrstuvxACDFJQNSUX] [-H baseHREF] [-T title ]
	[-L level [-R]] [-P pattern] [-I pattern] [-o filename] [--version]
	[--help] [--inodes] [--device] [--noreport] [--nolinks] [--dirsfirst]
	[--charset charset] [--filelimit[=]#] [--si] [--timefmt[=]<f>]
	[--sort[=]<name>] [--matchdirs] [--ignore-case] [--] [<directory list>]
  ------- Listing options -------
  -a            All files are listed.
  -d            List directories only.
  -l            Follow symbolic links like directories.
  -f            Print the full path prefix for each file.
  -x            Stay on current filesystem only.
  -L level      Descend only level directories deep.
  -R            Rerun tree when max dir level reached.
  -P pattern    List only those files that match the pattern given.
  -I pattern    Do not list files that match the given pattern.
  --ignore-case Ignore case when pattern matching.
  --matchdirs   Include directory names in -P pattern matching.
  --noreport    Turn off file/directory count at end of tree listing.
  --charset X   Use charset X for terminal/HTML and indentation line output.
  --filelimit # Do not descend dirs with more than # files in them.
  --timefmt <f> Print and format time according to the format <f>.
  -o filename   Output to file instead of stdout.
  -------- File options ---------
  -q            Print non-printable characters as '?'.
  -N            Print non-printable characters as is.
  -Q            Quote filenames with double quotes.
  -p            Print the protections for each file.
  -u            Displays file owner or UID number.
  -g            Displays file group owner or GID number.
  -s            Print the size in bytes of each file.
  -h            Print the size in a more human readable way.
  --si          Like -h, but use in SI units (powers of 1000).
  -D            Print the date of last modification or (-c) status change.
  -F            Appends '/', '=', '*', '@', '|' or '>' as per ls -F.
  --inodes      Print inode number of each file.
  --device      Print device ID number to which each file belongs.
  ------- Sorting options -------
  -v            Sort files alphanumerically by version.
  -t            Sort files by last modification time.
  -c            Sort files by last status change time.
  -U            Leave files unsorted.
  -r            Reverse the order of the sort.
  --dirsfirst   List directories before files (-U disables).
  --sort X      Select sort: name,version,size,mtime,ctime.
  ------- Graphics options ------
  -i            Don't print indentation lines.
  -A            Print ANSI lines graphic indentation lines.
  -S            Print with CP437 (console) graphics indentation lines.
  -n            Turn colorization off always (-C overrides).
  -C            Turn colorization on always.
  ------- XML/HTML/JSON options -------
  -X            Prints out an XML representation of the tree.
  -J            Prints out an JSON representation of the tree.
  -H baseHREF   Prints out HTML format with baseHREF as top directory.
  -T string     Replace the default HTML title and H1 header with string.
  --nolinks     Turn off hyperlinks in HTML output.
  ---- Miscellaneous options ----
  --version     Print version and exit.
  --help        Print usage and this help message and exit.
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ git commit -m"added .gitignore"
[master ebb60b5] added .gitignore
 1 file changed, 4 insertions(+)
 create mode 100644 .gitignore
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ git push origin master 
Username for 'https://github.com': LevS503      
Password for 'https://LevS503@github.com': 
Подсчет объектов: 3, готово.
Delta compression using up to 12 threads.
Сжатие объектов: 100% (2/2), готово.
Запись объектов: 100% (3/3), 339 bytes | 339.00 KiB/s, готово.
Total 3 (delta 0), reused 0 (delta 0)
remote: This repository moved. Please use the new location:
remote:   https://github.com/Levs503/lab02.git
To https://github.com/LevS503/lab02.git
   cceaa8d..ebb60b5  master -> master
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ git --help
использование: git [--version] [--help] [-C <path>] [-c <name>=<value>]
           [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]
           [-p | --paginate | --no-pager] [--no-replace-objects] [--bare]
           [--git-dir=<path>] [--work-tree=<path>] [--namespace=<name>]
           <command> [<args>]

Стандартные команды Git используемые в различных ситуациях:

создание рабочей области (смотрите также: git help tutorial)
   clone      Клонирование репозитория в новый каталог
   init       Создание пустого репозитория Git или переинициализация существующего

работа с текущими изменениями (смотрите также: git help everyday)
   add        Добавление содержимого файла в индекс
   mv         Перемещение или переименование файла, каталога или символьной ссылки
   reset      Сброс текущего состояния HEAD на указанное состояние
   rm         Удаление файлов из рабочего каталога и индекса

просмотр истории и текущего состояния (смотрите также: git help revisions)
   bisect     Выполнить двоичный поиск изменения, которое вносит ошибку
   grep       Вывод строк, соответствующих шаблону
   log        Вывод истории коммитов
   show       Вывод различных типов объектов
   status     Вывод состояния рабочего каталога

выращивание, отметка и настройка вашей общей истории
   branch     Вывод списка веток,  их создание или удаление
   checkout   Переключение веток или восстановление файлов в рабочем каталоге
   commit     Запись изменений в репозиторий
   diff       Вывод разницы между коммитами, коммитом и рабочим каталогом и т.д.
   merge      Объединение одной или нескольких историй разработки вместе
   rebase     Повторно применить коммиты над верхушкой другой ветки
   tag        Создание метки, вывод списка, удаление или проверка метки, подписанной с помощью GPG

совместная работа (смотрите также: git help workflows)
   fetch      Загрузка объектов и ссылок из другого репозитория
   pull       Извлечение изменений и объединение с другим репозиторием или локальной веткой
   push       Обновление внешних ссылок и связанных объектов

«git help -а» и «git help -g» выводит список доступных подкоманд и
некоторые руководства по темам. Запустите «git help <команда>» или
«git help <термин>», чтобы прочесть о конкретных подкоманде или теме.
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ $ git pull origin master
$: команда не найдена
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$  git pull origin master
Из https://github.com/LevS503/lab02
 * branch            master     -> FETCH_HEAD
Уже обновлено.
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ git log
commit ebb60b54a3b1c1f0bd8b2b4409b70aa1bbfa50b3 (HEAD -> master, origin/master)
Author: LevS503 <semkov01@mail.ru>
Date:   Thu Apr 9 21:47:23 2020 +0500

    added .gitignore

commit cceaa8d9613d450a2c56f936c0e60ea031d473c0
Author: LevS503 <semkov01@mail.ru>
Date:   Thu Apr 9 21:25:24 2020 +0500

    added README.md

commit 5910cab382089c148f61a75ca104e6f76e8f7cf4
Author: Levs503 <39101014+Levs503@users.noreply.github.com>
Date:   Thu Apr 9 21:19:25 2020 +0500

    Initial commit
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ mkdir sources
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ mkdir include
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ mkdir examples
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ ls
examples  include  LICENSE  README.md  sources
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ $ mkdir sources
$: команда не найдена
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ $ mkdir include
$: команда не найдена
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ $ mkdir examples
$: команда не найдена
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ 
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ cat>sources/print.cpp <<EOF
> #include <print.hpp>
> 
> void print(const std::string& text, std::ostream& out)
> {
>   out << text;
> }
> 
> void print(const std::string& text, std::ofstream& out)
> {
>   out << text;
> }
> EOF
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ cat > include/print.hpp << EOF
> #include <fstream>
> #include <iostream>
> #include <string>
> 
> void print(const std::string& text, std::ofstream& out);
> void print(const std::string& text, std::ostream& out = std::cout);
> EOF
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ cat > examples/example1.cpp <<EOF
> #include <print.hpp>
> 
> int main(int argc, char** argv)
> {
>   print("hello");
> }
> EOF
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ cat > examples/example2.cpp <<EOF
> #include <print.hpp>
> 
> #include <fstream>
> 
> int main(int argc, char** argv)
> {
>   std::ofstream file("log.txt");
>   print(std::string("hello"), file);
> }
> EOF
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ edit --help
Использование: nano [ОПЦИИ] [[+СТРОКА[,СТОЛБЕЦ]] ФАЙЛ]...

Чтобы поместить курсор в нужную строку файла, укажите номер строки с
'+' перед именем файла. Можно добавить номер столбца после запятой.
Если вместо имени файла указано '-', nano читает данные из стандартного потока ввода.

Опция		Длинная форма		Значение
 -A		--smarthome		Включить умную кнопку home
 -B		--backup		Сохранять резервные копии существующих файлов
 -C <дир>	--backupdir=<дир>	Каталог для хранения уникальных резервных копий
 -D		--boldtext		Использовать жирный шрифт вместо обычного
 -E		--tabstospaces		Преобразовать табуляции в пробелы
 -F		--multibuffer		Читать файл в новый буфер по умолчанию
 -G		--locking		Использовать файлы блокировки (vim-стиль)
 -H		--historylog		Сохранять и читать историю поиска/замены строк
 -I		--ignorercfiles		Не использовать на файлы nanorc
 -K		--rebindkeypad		Исправлять проблему малой клавиатуры
 -L		--nonewlines		Не добавлять пустые строки в конце файла
 -M		--trimblanks		Trim tail spaces when hard-wrapping
 -N		--noconvert		Не преобразовывать из DOS/Mac формата
 -O		--morespace		Использование дополнительной строки для редактирования
 -P		--positionlog		Сохранять и загружать позицию курсора
 -Q <стр>	--quotestr=<стр>	Строка цитирования
 -R		--restricted		Ограниченный режим
 -S		--smooth		Построчная прокрутка вместо полу-экранной
 -T <#чис>	--tabsize=<#чис>	Установить ширину табуляции в #чис столбцов
 -U		--quickblank		Использовать быструю очистку строки состояния
 -V		--version		Показать версию и выйти
 -W		--wordbounds		Использовать более точное определение границ слов
 -X <str>	--wordchars=<str>	Which other characters are word parts
 -Y <name>	--syntax=<name>		Использовать описание синтаксиса для подсветки
 -a		--atblanks		When soft-wrapping, do it at whitespace
 -c		--constantshow		Постоянно показывать позицию курсора
 -d		--rebinddelete		Исправить проблему Backspace/Delete
 -g		--showcursor		Show cursor in file browser
 -h		--help			Показать эту справку и выйти
 -i		--autoindent		Автоматический отступ на новых строках
 -k		--cutfromcursor		Вырезаь от курсора до конца строки
 -l		--linenumbers		Показывать номера строк перед текстом
 -m		--mouse			Разрешить использование мыши
 -n		--noread		Не читать файл (только писать его)
 -o <дир>	--operatingdir=<дир>	Установить рабочий каталог
 -p		--preserve		Зарезервировать кнопки XON (^Q) и XOFF (^S)
 -r <#столбцы>	--fill=<#столбцы>	Установить точку жесткого переноса строки на #столбцы
 -s <программа>	--speller=<программа>	Использовать альтернативную программу проверки орфографии
 -t		--tempfile		Автозапись при выходе, без лишних вопросов
 -u		--unix			Сохранить файл в формате Unix по умолчанию
 -v		--view			Режим просмотра (только чтение)
 -w		--nowrap		Не делать жесткий перенос длинных строк
 -x		--nohelp		Не показывать две строки помощи внизу
 -z		--suspend		Разрешить приостановку
 -$		--softwrap		Включить мягкий перенос строк
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ edit README.md
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ git add .
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ git commit -m"addeed sources"
[master a26b48b] addeed sources
 5 files changed, 33 insertions(+)
 create mode 100644 examples/example1.cpp
 create mode 100644 examples/example2.cpp
 create mode 100644 include/print.hpp
 create mode 100644 sources/print.cpp
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ git push origin master
Username for 'https://github.com': LevS503
Password for 'https://LevS503@github.com': 
Подсчет объектов: 10, готово.
Delta compression using up to 12 threads.
Сжатие объектов: 100% (7/7), готово.
Запись объектов: 100% (10/10), 988 bytes | 329.00 KiB/s, готово.
Total 10 (delta 0), reused 0 (delta 0)
remote: This repository moved. Please use the new location:
remote:   https://github.com/Levs503/lab02.git
To https://github.com/LevS503/lab02.git
   ebb60b5..a26b48b  master -> master
levs503@levs503-MSI:~/LevS503/workspace/projects/lab02$ 

