luka@luka-VirtualBox:~$ export GITHUB_USERNAME=Joker762-rgb
luka@luka-VirtualBox:~$ export GIST_TOKEN=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
luka@luka-VirtualBox:~$ alias edit=nano
luka@luka-VirtualBox:~$ mkdir -p ${GITHUB_USERNAME}/workspace
luka@luka-VirtualBox:~$ cd ${GITHUB_USERNAME}/workspace
luka@luka-VirtualBox:~/Joker762-rgb/workspace$ pwd
/home/luka/Joker762-rgb/workspace
luka@luka-VirtualBox:~/Joker762-rgb/workspace$ cd . .
bash: cd: слишком много аргументов
luka@luka-VirtualBox:~/Joker762-rgb/workspace$ cd
luka@luka-VirtualBox:~$ cd ${GITHUB_USERNAME}/workspace
luka@luka-VirtualBox:~/Joker762-rgb/workspace$ pwd
/home/luka/Joker762-rgb/workspace
luka@luka-VirtualBox:~/Joker762-rgb/workspace$ cd ..
luka@luka-VirtualBox:~/Joker762-rgb$ pwd
/home/luka/Joker762-rgb
luka@luka-VirtualBox:~/Joker762-rgb$ mfdir -p workspace/tasks/
Команда «mfdir» не найдена. Возможно, вы имели в виду:
  команда 'mkdir' из deb-пакета coreutils (9.4-3.1ubuntu1)
  команда 'mdir' из deb-пакета mtools (4.0.43-1build1)
  команда 'mmdir' из deb-пакета simh (3.8.1-6.2)
Попробуйте: sudo apt install <имя_deb-пакета>
luka@luka-VirtualBox:~/Joker762-rgb$ mkdir -p workspace/tasks/
luka@luka-VirtualBox:~/Joker762-rgb$ mkdir -p workspace/projects/
luka@luka-VirtualBox:~/Joker762-rgb$ mkdir -p workspace/reports/
luka@luka-VirtualBox:~/Joker762-rgb$ cd workspace
luka@luka-VirtualBox:~/Joker762-rgb/workspace$ wget https://nodejs.org/dist/v6.11.5/node-v6.11.5-linux-x64.tar.xz
--2025-03-01 17:39:38--  https://nodejs.org/dist/v6.11.5/node-v6.11.5-linux-x64.tar.xz
Распознаётся nodejs.org (nodejs.org)… 104.20.23.46, 104.20.22.46, 2606:4700:10::6814:162e, ...
Подключение к nodejs.org (nodejs.org)|104.20.23.46|:443... соединение установлено.
HTTP-запрос отправлен. Ожидание ответа… 200 OK
Длина: 9356460 (8,9M) [application/x-xz]
Сохранение в: ‘node-v6.11.5-linux-x64.tar.xz’

node-v6.11.5-linux-x64.ta 100%[=====================================>]   8,92M  1,12MB/s    за 8,0s    

2025-03-01 17:39:46 (1,12 MB/s) - ‘node-v6.11.5-linux-x64.tar.xz’ сохранён [9356460/9356460]

luka@luka-VirtualBox:~/Joker762-rgb/workspace$ tar -xf node-v6.11.5-linux-x64.tar.xz
luka@luka-VirtualBox:~/Joker762-rgb/workspace$ rm -rf node-v6.11.5-linux-x64.tar.xz
luka@luka-VirtualBox:~/Joker762-rgb/workspace$ mv node-v6.11.5-linux-x64 node
luka@luka-VirtualBox:~/Joker762-rgb/workspace$ ls node/bin
node  npm
luka@luka-VirtualBox:~/Joker762-rgb/workspace$ echo ${PATH}
/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin:/snap/bin
luka@luka-VirtualBox:~/Joker762-rgb/workspace$ export PATH=${PATH}: `pwd`/node/bin
bash: export: «/home/luka/Joker762-rgb/workspace/node/bin»: это недопустимый идентификатор
luka@luka-VirtualBox:~/Joker762-rgb/workspace$ export PATH=${PATH}:`pwd`/node/bin
luka@luka-VirtualBox:~/Joker762-rgb/workspace$ echo ${PATH}
/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin:/snap/bin::/home/luka/Joker762-rgb/workspace/node/bin
luka@luka-VirtualBox:~/Joker762-rgb/workspace$ mkdir scripts
luka@luka-VirtualBox:~/Joker762-rgb/workspace$ cat > scripts/activate<<EOF
> export PATH=\${PATH}:`pwd`/node/bin
> EOF
luka@luka-VirtualBox:~/Joker762-rgb/workspace$ source scripts/activate
luka@luka-VirtualBox:~/Joker762-rgb/workspace$ gem install gist
Команда «gem» не найдена, но может быть установлена с помощью:
sudo snap install ruby           # version 3.4.2, or
sudo apt  install ruby-rubygems  # version 3.4.20-1
См. 'snap info ruby', чтобы посмотреть дополнительные версии.
luka@luka-VirtualBox:~/Joker762-rgb/workspace$ suda apt install gist
Команда «suda» не найдена. Возможно, вы имели в виду:
  команда 'sada' из deb-пакета plc-utils-extra (0.0.6+git20230504.1ba7d5a0-1)
  команда 'sudo' из deb-пакета sudo (1.9.15p5-3ubuntu5)
  команда 'sudo' из deb-пакета sudo-ldap (1.9.15p5-3ubuntu5)
Попробуйте: sudo apt install <имя_deb-пакета>
luka@luka-VirtualBox:~/Joker762-rgb/workspace$ sudo apt install gist
[sudo] пароль для luka: 
Попробуйте ещё раз.
[sudo] пароль для luka: 
К установке:                                                      
  gist

Зависимости к установке:
  fonts-lato         libruby     ruby             ruby-rubygems  ruby-xmlrpc
  javascript-common  libruby3.3  ruby-json        ruby-sdbm      ruby3.3
  libjs-jquery       rake        ruby-net-telnet  ruby-webrick   rubygems-integration

Предлагаемые пакеты:
  apache2  | lighttpd  | httpd  ri  ruby-dev  bundler

Сводка:
  К обновлению: 0, К установке: 16 К удалению: 0, Не обновляется: 133
  Размер загрузки: 9 487 kB
  Места необходимо: 44,8 MB / 14,5 GB доступно

Продолжить? [Д/н] Д
Пол:1 http://ru.archive.ubuntu.com/ubuntu oracular/main amd64 fonts-lato all 2.015-1 [2 781 kB]
Пол:2 http://ru.archive.ubuntu.com/ubuntu oracular/main amd64 rubygems-integration all 1.18ubuntu1 [5 528 B]
Пол:3 http://ru.archive.ubuntu.com/ubuntu oracular-updates/main amd64 ruby3.3 amd64 3.3.4-2ubuntu5.1 [49,1 kB]
Пол:4 http://ru.archive.ubuntu.com/ubuntu oracular/main amd64 libruby amd64 1:3.3~ubuntu3 [5 036 B]
Пол:5 http://ru.archive.ubuntu.com/ubuntu oracular/main amd64 ruby-rubygems all 3.4.20-1 [238 kB]
Пол:6 http://ru.archive.ubuntu.com/ubuntu oracular/main amd64 ruby amd64 1:3.3~ubuntu3 [3 618 B]
Пол:7 http://ru.archive.ubuntu.com/ubuntu oracular/main amd64 rake all 13.2.1-1 [45,8 kB]
Пол:8 http://ru.archive.ubuntu.com/ubuntu oracular/main amd64 ruby-net-telnet all 0.2.0-1 [13,3 kB]
Пол:9 http://ru.archive.ubuntu.com/ubuntu oracular/main amd64 ruby-webrick all 1.8.1-1ubuntu1 [52,6 kB]
Пол:10 http://ru.archive.ubuntu.com/ubuntu oracular/main amd64 ruby-xmlrpc all 0.3.3-2 [24,8 kB]
Пол:11 http://ru.archive.ubuntu.com/ubuntu oracular/main amd64 ruby-sdbm amd64 1.0.0-5build5 [16,1 kB]
Пол:12 http://ru.archive.ubuntu.com/ubuntu oracular-updates/main amd64 libruby3.3 amd64 3.3.4-2ubuntu5.1 [5 834 kB]
Пол:13 http://ru.archive.ubuntu.com/ubuntu oracular/universe amd64 ruby-json amd64 2.7.2+dfsg-1build1 [54,3 kB]
Пол:14 http://ru.archive.ubuntu.com/ubuntu oracular/universe amd64 gist all 6.0.0-3 [30,0 kB]          
Пол:15 http://ru.archive.ubuntu.com/ubuntu oracular/main amd64 javascript-common all 11+nmu1 [5 936 B] 
Пол:16 http://ru.archive.ubuntu.com/ubuntu oracular/main amd64 libjs-jquery all 3.6.1+dfsg+~3.5.14-1 [328 kB]
Получено 9 487 kB за 8с (1 158 kB/s)                                                                   
Выбор ранее не выбранного пакета fonts-lato.
(Чтение базы данных … на данный момент установлено 150028 файлов и каталогов.)
Подготовка к распаковке …/00-fonts-lato_2.015-1_all.deb …
Распаковывается fonts-lato (2.015-1) …
Выбор ранее не выбранного пакета rubygems-integration.
Подготовка к распаковке …/01-rubygems-integration_1.18ubuntu1_all.deb …
Распаковывается rubygems-integration (1.18ubuntu1) …
Выбор ранее не выбранного пакета ruby3.3.
Подготовка к распаковке …/02-ruby3.3_3.3.4-2ubuntu5.1_amd64.deb …
Распаковывается ruby3.3 (3.3.4-2ubuntu5.1) …
Выбор ранее не выбранного пакета libruby:amd64.
Подготовка к распаковке …/03-libruby_1%3a3.3~ubuntu3_amd64.deb …
Распаковывается libruby:amd64 (1:3.3~ubuntu3) …
Выбор ранее не выбранного пакета ruby-rubygems.
Подготовка к распаковке …/04-ruby-rubygems_3.4.20-1_all.deb …
Распаковывается ruby-rubygems (3.4.20-1) …
Выбор ранее не выбранного пакета ruby.
Подготовка к распаковке …/05-ruby_1%3a3.3~ubuntu3_amd64.deb …
Распаковывается ruby (1:3.3~ubuntu3) …
Выбор ранее не выбранного пакета rake.
Подготовка к распаковке …/06-rake_13.2.1-1_all.deb …
Распаковывается rake (13.2.1-1) …
Выбор ранее не выбранного пакета ruby-net-telnet.
Подготовка к распаковке …/07-ruby-net-telnet_0.2.0-1_all.deb …
Распаковывается ruby-net-telnet (0.2.0-1) …
Выбор ранее не выбранного пакета ruby-webrick.
Подготовка к распаковке …/08-ruby-webrick_1.8.1-1ubuntu1_all.deb …
Распаковывается ruby-webrick (1.8.1-1ubuntu1) …
Выбор ранее не выбранного пакета ruby-xmlrpc.
Подготовка к распаковке …/09-ruby-xmlrpc_0.3.3-2_all.deb …
Распаковывается ruby-xmlrpc (0.3.3-2) …
Выбор ранее не выбранного пакета ruby-sdbm:amd64.
Подготовка к распаковке …/10-ruby-sdbm_1.0.0-5build5_amd64.deb …
Распаковывается ruby-sdbm:amd64 (1.0.0-5build5) …
Выбор ранее не выбранного пакета libruby3.3:amd64.
Подготовка к распаковке …/11-libruby3.3_3.3.4-2ubuntu5.1_amd64.deb …
Распаковывается libruby3.3:amd64 (3.3.4-2ubuntu5.1) …
Выбор ранее не выбранного пакета ruby-json:amd64.
Подготовка к распаковке …/12-ruby-json_2.7.2+dfsg-1build1_amd64.deb …
Распаковывается ruby-json:amd64 (2.7.2+dfsg-1build1) …
Выбор ранее не выбранного пакета gist.
Подготовка к распаковке …/13-gist_6.0.0-3_all.deb …
Распаковывается gist (6.0.0-3) …
Выбор ранее не выбранного пакета javascript-common.
Подготовка к распаковке …/14-javascript-common_11+nmu1_all.deb …
Распаковывается javascript-common (11+nmu1) …
Выбор ранее не выбранного пакета libjs-jquery.
Подготовка к распаковке …/15-libjs-jquery_3.6.1+dfsg+~3.5.14-1_all.deb …
Распаковывается libjs-jquery (3.6.1+dfsg+~3.5.14-1) …
Настраивается пакет javascript-common (11+nmu1) …
Настраивается пакет fonts-lato (2.015-1) …
Настраивается пакет rubygems-integration (1.18ubuntu1) …
Настраивается пакет ruby-net-telnet (0.2.0-1) …
Настраивается пакет ruby-webrick (1.8.1-1ubuntu1) …
Настраивается пакет libjs-jquery (3.6.1+dfsg+~3.5.14-1) …
Настраивается пакет ruby-xmlrpc (0.3.3-2) …
Настраивается пакет ruby-rubygems (3.4.20-1) …
Настраивается пакет ruby3.3 (3.3.4-2ubuntu5.1) …
Настраивается пакет ruby (1:3.3~ubuntu3) …
Настраивается пакет rake (13.2.1-1) …
Настраивается пакет libruby3.3:amd64 (3.3.4-2ubuntu5.1) …
Настраивается пакет gist (6.0.0-3) …
Настраивается пакет libruby:amd64 (1:3.3~ubuntu3) …
Настраивается пакет ruby-json:amd64 (2.7.2+dfsg-1build1) …
Настраивается пакет ruby-sdbm:amd64 (1.0.0-5build5) …
Обрабатываются триггеры для fontconfig (2.15.0-1.1ubuntu2) …
Обрабатываются триггеры для libc-bin (2.40-1ubuntu3.1) …
Обрабатываются триггеры для man-db (2.12.1-3) …
luka@luka-VirtualBox:~/Joker762-rgb/workspace$ (umask 0077 && echo ${GIST_TOKEN} > ~/.gist)
luka@luka-VirtualBox:~/Joker762-rgb/workspace$ export LAB_NUMBER=01
luka@luka-VirtualBox:~/Joker762-rgb/workspace$ git clone https://github.com/tp-labs/lab${LAB_NUMBER} tasks/lab${LAB_NUMBER}
Команда «git» не найдена, но может быть установлена с помощью:
sudo apt install git
luka@luka-VirtualBox:~/Joker762-rgb/workspace$ sudo apt install git
К установке:                                                      
  git

Зависимости к установке:
  git-man  liberror-perl

Предлагаемые пакеты:
  git-daemon-run         git-doc    git-gui  gitweb   git-mediawiki
  | git-daemon-sysvinit  git-email  gitk     git-cvs  git-svn

Сводка:
  К обновлению: 0, К установке: 3 К удалению: 0, Не обновляется: 133
  Размер загрузки: 5 168 kB
  Места необходимо: 26,9 MB / 14,4 GB доступно

Продолжить? [Д/н] Д
Пол:1 http://ru.archive.ubuntu.com/ubuntu oracular/main amd64 liberror-perl all 0.17029-2 [25,6 kB]
Пол:2 http://ru.archive.ubuntu.com/ubuntu oracular-updates/main amd64 git-man all 1:2.45.2-1ubuntu1.1 [1 122 kB]
Пол:3 http://ru.archive.ubuntu.com/ubuntu oracular-updates/main amd64 git amd64 1:2.45.2-1ubuntu1.1 [4 020 kB]
Получено 5 168 kB за 4с (1 157 kB/s) 
Выбор ранее не выбранного пакета liberror-perl.
(Чтение базы данных … на данный момент установлено 153370 файлов и каталогов.)
Подготовка к распаковке …/liberror-perl_0.17029-2_all.deb …
Распаковывается liberror-perl (0.17029-2) …
Выбор ранее не выбранного пакета git-man.
Подготовка к распаковке …/git-man_1%3a2.45.2-1ubuntu1.1_all.deb …
Распаковывается git-man (1:2.45.2-1ubuntu1.1) …
Выбор ранее не выбранного пакета git.
Подготовка к распаковке …/git_1%3a2.45.2-1ubuntu1.1_amd64.deb …
Распаковывается git (1:2.45.2-1ubuntu1.1) …
Настраивается пакет liberror-perl (0.17029-2) …
Настраивается пакет git-man (1:2.45.2-1ubuntu1.1) …
Настраивается пакет git (1:2.45.2-1ubuntu1.1) …
Обрабатываются триггеры для man-db (2.12.1-3) …
luka@luka-VirtualBox:~/Joker762-rgb/workspace$ git clone https://github.com/tp-labs/lab${LAB_NUMBER} tasks/lab${LAB_NUMBER}
Клонирование в «tasks/lab01»...
remote: Enumerating objects: 74, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 74 (delta 0), reused 1 (delta 0), pack-reused 71 (from 1)
Получение объектов: 100% (74/74), 945.07 КиБ | 43.00 КиБ/с, готово.
Определение изменений: 100% (20/20), готово.
luka@luka-VirtualBox:~/Joker762-rgb/workspace$ mkdir reports/lab${LAB_NUMBER}
luka@luka-VirtualBox:~/Joker762-rgb/workspace$ cp tasks/lab${LAB_NUMBER}/README>md reports/lab${LAB_NUMBER}/REPORT.md
cp: не удалось выполнить stat для 'tasks/lab01/README': Нет такого файла или каталога
luka@luka-VirtualBox:~/Joker762-rgb/workspace$ cp tasks/lab${LAB_NUMBER}/README.md reports/lab${LAB_NUMBER}/REPORT.md
luka@luka-VirtualBox:~/Joker762-rgb/workspace$ cd reports/lab${LAB_NUMBER}
luka@luka-VirtualBox:~/Joker762-rgb/workspace/reports/lab01$ edit REPORT.md
luka@luka-VirtualBox:~/Joker762-rgb/workspace/reports/lab01$ gist REPORT.md
Команда «gist» не найдена, но может быть установлена с помощью:
sudo apt install yorick
luka@luka-VirtualBox:~/Joker762-rgb/workspace/reports/lab01$ sudo apt install yorick
К установке:                                                      
  yorick

Зависимости к установке:
  rlwrap  yorick-data  yorick-z

Предлагаемые пакеты:
  yorick-full  yorick-mpy-openmpi  | yorick-mpy-mpich2  emacsen  curl

Сводка:
  К обновлению: 0, К установке: 4 К удалению: 0, Не обновляется: 133
  Размер загрузки: 1 457 kB
  Места необходимо: 4 588 kB / 14,4 GB доступно

Продолжить? [Д/н] Д
Пол:1 http://ru.archive.ubuntu.com/ubuntu oracular/universe amd64 rlwrap amd64 0.46.1-1build2 [107 kB]
Пол:2 http://ru.archive.ubuntu.com/ubuntu oracular/universe amd64 yorick-data all 2.2.04+dfsg1-13 [505 kB]
Пол:3 http://ru.archive.ubuntu.com/ubuntu oracular/universe amd64 yorick amd64 2.2.04+dfsg1-13 [809 kB]
Пол:4 http://ru.archive.ubuntu.com/ubuntu oracular/universe amd64 yorick-z amd64 1.2.0+cvs20080115-5.1build2 [36,7 kB]
Получено 1 457 kB за 1с (1 043 kB/s)       
Выбор ранее не выбранного пакета rlwrap.
(Чтение базы данных … на данный момент установлено 154472 файла и каталога.)
Подготовка к распаковке …/rlwrap_0.46.1-1build2_amd64.deb …
Распаковывается rlwrap (0.46.1-1build2) …
Выбор ранее не выбранного пакета yorick-data.
Подготовка к распаковке …/yorick-data_2.2.04+dfsg1-13_all.deb …
Распаковывается yorick-data (2.2.04+dfsg1-13) …
Выбор ранее не выбранного пакета yorick.
Подготовка к распаковке …/yorick_2.2.04+dfsg1-13_amd64.deb …
Распаковывается yorick (2.2.04+dfsg1-13) …
Выбор ранее не выбранного пакета yorick-z.
Подготовка к распаковке …/yorick-z_1.2.0+cvs20080115-5.1build2_amd64.deb …
Распаковывается yorick-z (1.2.0+cvs20080115-5.1build2) …
Настраивается пакет yorick-data (2.2.04+dfsg1-13) …
Настраивается пакет rlwrap (0.46.1-1build2) …
update-alternatives: используется /usr/bin/rlwrap для предоставления /usr/bin/readline-editor (readline-ed
itor) в автоматическом режиме
/usr/share/rlwrap/filters/ftp_filter.py:57: SyntaxWarning: invalid escape sequence '\s'
  results = [re.split('\s+', l)[dir_filename_column[where]] for l in lines]
/usr/share/rlwrap/filters/ftp_filter.py:100: SyntaxWarning: invalid escape sequence '\s'
  nwords = len(re.split('\s+', line))
/usr/share/rlwrap/filters/ftp_filter.py:108: SyntaxWarning: invalid escape sequence '\s'
  command = re.search('\s*(\S+)', line).group(1)
/usr/share/rlwrap/filters/rlwrapfilter.py:4: SyntaxWarning: invalid escape sequence '\s'
  """
/usr/share/rlwrap/filters/rlwrapfilter.py:211: SyntaxWarning: invalid escape sequence '\S'
  m = re.match("(\S+) (.*?)\r?\n", sys.stdin.readline())
Настраивается пакет yorick (2.2.04+dfsg1-13) …
Настраивается пакет yorick-z (1.2.0+cvs20080115-5.1build2) …
Обрабатываются триггеры для man-db (2.12.1-3) …
Обрабатываются триггеры для install-info (7.1-3build2) …
luka@luka-VirtualBox:~/Joker762-rgb/workspace/reports/lab01$ gist REPORT.md
gist: (WARNING) fread failed (command) on CGM file REPORT.md
gist: (WARNING) BEGIN METAFILE element missing
gist: (WARNING) REPORT.md is not a binary CGM, cannot open

