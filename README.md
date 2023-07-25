# linux_basic

## Basic comand 

## Content


 [Help](#help)

 [Keyboard shortcuts](#keyboard-shortcuts)

 [Piping](#piping)

 [About System](#about-system)

 [History](#history)
 
 [Work with directories](#work-with-directories)
 
 [Work with files](#work-with-files)
  
 [Work with links](#create-links)
 
 [Search](#search)
  
 [Redirecting IO](#redirecting-io)

 [Zip](#zip)

 [Memory and Processes](#memory-and-processes)
 
 [Logs](#logs)
 
 [Accounts](#accounts)
  
 [Network](#network)
   
 [Install programms](#install-programms)

 [Environment variables](#environment-variables)
    
 [Bash](#bash)
 
 [HDD](#hdd)
 
 [Schedule](#schedule)
   
 [SDK](#sdk)

 [Solving problem](#solving-problem)
  


### Help

[Content](#content)


`man` – помощь - help

`man -k time` -find all avaible commands wich contains word "time"

`man uptime`  - show manual info about command "uptime" . When we in text redactor we can find word `/word` - show all "word" in this manual(to move between "word" use `n`). To exit `q`

`info` – помощь - help documentation 

`info uptime`  - show manual info about command "uptime" . When we in text redactor we can find word `/word` - show all "word" in this manual. To exit `q`

`whatis` – показывает что делает комманда - show short description command

`whatis uptime` – показывает что делает комманда - show short description command "uptime"

`apropos`  -  command searches the man page descriptions for a specified string

`apropos -a graph editor` -  outputs man pages that contain both the words “graph" and "editor” in their descriptions


### Keyboard shortcuts

[Content](#content)

    • `CTRL + C` Terminates a command that is currently running; from the instructions portion of Qwiklabs, you can use CTRL + C to copy, but within the terminal, it will only terminate a command and if one isn't running, it will display ^C at the prompt

    • `CTRL + V` Pastes text

    • `clear`  Clears the terminal screen; this can also be done by entering `CTRL + L`

    • `CTRL + A` Sets your cursor at the beginning of a command

    • `CTRL + E` Sets your cursor at the end of a command

    • `Left arrow` key: Moves left within a command

    • `Right arrow` key: Moves right within a command

    • `Up arrow` key: Provides the last command you entered into the command line; can be entered multiple times to go through multiple commands from the command history

    • `Down arrow` key: Provides the next command in the command history; must be after using the up arrow key

    • `Tab` key: Provides available suggestions for completing your text 


### Piping

`|`  -  Piping sends the standard output of one command as standard input to another command for further processing. 

`ls /home/analyst/reports | grep users` - returns the file and directory names in the reports directory that contain users


### About System 

[Content](#content)

`ps` - show processes

`Ctrl+Z`  - отправить процесс на background -  process to background mode

`fg` - return process from background mode

`Ctrl+C`– прекратить процесс вообще - stop process

`uptime`  - время с последнего включения - time from last turn on

`uname` - version Linux 

`user -a` - more info about Linux

`lscpu` – данные процессора - info about processor

`clear` - clean terminal

`ls` - show directory - показать что в этой директории

`ls -l` - more info about directory(with rights)

`ls –la –R  / `   - показать все на компутере - show all files in pc

`head import.txt `*show 10 lines first

`tail import.txt` **show 10 lines last

`exho $PATH` - show directories from wich we use commands

`echo` -show text

`echo Hello!` - show "Hello!"

`ctrl(left) + F3` -switch to linux wihout grafic interface

`ctrl(left) + F4` -switch to linux wihout grafic interface add new session and you can next session ctrl(left) + F5

`alt(left) + F3 or F4` - switch between sessions(tty)

`ctrl(left) + alt + F2` - exit from mode without grafic interface


`whereis`– показывает где файл -show place of file where command

`whereis uptime` - show file where command

`locate` – показывает где файл - need to install

`locate uptime` - show directory where file or test.txt

`sudo reboot now` - reboot system

`sudo shutdown now` - power off

`uname -r `-show version of kurl

`sudo apt full -upgrade -y`
  
### History

[Content](#content)


`!77 `  -run command from history

`!! - run` previos command

`$HISTSIZE `- quantity saved commands

search `ctrl+r`


### Work with directories

[Content](#content)

`/` - root directory - коренная директория Linux

`/home`- Each user in the system gets their own home directory.

`/bin` -  This directory stands for “binary” and contains binary files and other executables. Executables are files that contain a series of commands a computer needs to follow to run programs and perform other functions.

`/etc` -  This directory stores the system’s configuration files.

`/tmp` - This directory stores many temporary files. The /tmp directory is commonly used by attackers because anyone in the system can modify data in these files.

`/mnt` - This directory stands for “mount” and stores media, such as USB drives and hard drives.

`/home` - directory where users

`/media` - diks directory

`pwd` – вывести путь где мы сейчас - path to current place where we are

`~ `  - сокращение нашей Home директории - short name home dirrectory when you are in `/home/username`

`..`    - директория которая выше - directory which above current

`. `    - директория где мы сейчас - current directory

`cd`  - сменить директорию - change directory

`cd` or `cd ~` - move to home directory `/home/username`

`cd ~/test/` - move to `/home/username/test/`

`cd /` - move to root directory "/" we can `cd /home`

`cd ..` - move to directory above

`cd ../..` - move to 2 directory above

`ls` – вывести содержимое директории - show all in directory

`ls –la –R  / `   - показать все на компутере - show all files in pc

`ls -a` Displays hidden files. Hidden files start with a period (.) at the beginning.

`ls -l` Displays permissions to files and directories. Also displays other additional information, including owner name, group, file size, and the time of last modification.

`ls -la` Displays permissions to files and directories, including hidden files. This is a combination of the other two options.

`less` -  returns the content of a file one page at a time

    • Space bar: Move forward one page
    • b: Move back one page
    • Down arrow: Move forward one line
    • Up arrow: Move back one line
    • q: Quit and return to the previous terminal window

`less 1.txt`

`mkdir` – создать директорию -create directory

`mkdir dir1` -create directory dir1

`mkdir dir1/dir2` - create dir2 in dir1

`mkdir -p dir3/dir4` - create dir3 and dir4 in dir3

`mkdir my\ cool\ folder` ***name with spaces

`mkdir 'my directory'`  ***name with spaces

`ls -R dir3` -show name dir3: and dir4

`ls -Rla dir3` -show name dir3: and dir4 with hidden

`mv`  - переименовать или перенести директорию

`mv my_doc.txt your_doc.txt`  **rename doc

`mv your_doc.txt ~/Documents` **move doc

`mv *_doc.txt ~/Desktop`

`mv dir1 dirr` - rename dir1 to dirr

`rmdir` – стереть пустую директорию

`rmdir dirr` - remove if dirr empty

`rm –R`   – стереть не пустую директорию со всем что внутри - delete not empty directory

`rm -R  dir*` - remove all directories started "dir"

`rm doc1.txt `

`rm -rf important_syst_file` **force remove

`rm -r my_folder` **recursively

`cp`     - копировать директорию - copy directory

`cp -R dir2 dir4` - copy directory dir2 to dir4 with all files

`cp my.txt ~/Desktop`

`cp *.txt ~/Desktop`

`cp -r photo ~/Desktop` ***copy directory photo to Desktop recursively

`DONT DO IT DANGER!!!`  `sudo rm –R  / --no-preserve-root`   - замочить систему Linux - kill system



### Work with files

[Content](#content)

`cat` - show file

`cat text.txt` - show file use `Tab` when in directory to autofilling for example `cat t`+Tab == `cat text.txt`

`more text.txt` - show file by pages, to read next use `Enter` to exit `q`.

`less text.txt` - show file  When we in text redactor we can find word `/word` - show all "word" in this manual(to move between "word" use `n`). To exit `q`

`touch` – создать файл или обновить время

`toch test.txt` -create file test.txt if you again use `touch test.txt` will be updated date creation

`cp`  - скопировать файл - copy file

`cp test.txt /home/user/data/` - cp fileName then directory where we want to copy(copy test.txt to /home/user/data/)

`cp t*.* dir` - copy all files started "t" to directory dir

`cp file?.txt -v dir` - file?.txt it mean that any symbol can be instead ? , copy all files according pattern to dir; `-v` mean show what we do 

`cp -R dir newdir` - copy directory dir into directory newdir

`rm` – стереть файл - delete file

`rm *` -delete all files in directory

`rm dir/*` - delete all files in dir

`mv` – перенести файл или переименовать - move or rename file

`mv secret.txt .secret.txt` - make file hidden to show it use `ls -la`

`mv .secret.txt ~/Desktop/` - move secret.txt to desktop directory

#### Redacting files

`vi` или `vim`  - самы старый и дурацкий редактор - oldest redactor `i` -to redact file `Esc` - out from redact. `:q`-exit, `:wq` -write and quit `:wq text.txt` -save to new file text.txt and quit

`pico`  - новый редактов - the same as nano but less older

`nano` – самый новый редактор - newest redactor `^`(ctrl)-for commands. `ctrl+o` -save `ctrl+x` -exit 

`nano file.txt` - create and redact if not exist, else if present redact file

`gedit` – как и Notepad в Windows, работает только  если есть графический интерфейс - only with graphic interface

### Create Links

[Content](#content)

`ln`   - создать дубликат файла 

`ln –s `  - создать symbolic линк на файл или директорию типа Shortcut

`ln -s /home/user/dir MyLinkToDir` - create link to directory dir (always use absolute path) with name link MyLinkToDir

`cd MyLinkToDir` - go to dir by link

`mv MyLinkToDir ~/Desktop/` - move link to desktop directory

`ln -s file.txt MyFile` - link to file file.txt (we can create a few links to one file, if we remove file links will be read)

`toch MyFile` - change data creating file.txt

`rm MyFile` - remove link

`ln file.txt fileduplicate` - !!!only for file!!! create duplicate(clone) file.txt with name fileduplicate (if we change file.txt duplicate also change in back order too)

`ls -l file `-show info about file after permissions quantity of links

`ln -s file file_softlink `-create softlink(refer to file)

`ln file file_hardlink `-create hardlink(refer to point on disk)

`ls -l file `-we will see 2


### Search

[Content](#content)

`find` - найти файл - find file

`find /home -name "*.txt"` - find all files .txt in home directory

`find /home -name "file*.txt"` - find all files name starts from file .txt in home directory

`find / \( -path '/bin/*' search1 \) -o \( -path '/usr/bin/*' search2 \)`

`wc`  - вывести количество строк, слов, байт - count quantity of strings(lines), words, bytes

`wc linux.txt` - show quantity in file linux.txt

`wc -l linux.txt` - show quantity only strings in file linux.txt

`wc -w linux.txt` - show quantity words in file linux.txt

`cut` – вывести определенное поле из текста - show field by delimeter

`cut -d ">" -f 3 filedata.txt` - show fild by delimeter ">" 3d column from file filedata.txt

`cut -d ">" -f 3 filedata.txt | sort` - show fild by delimeter ">" 3d column from file filedata.txt then sort them



`sort` – вывести отсортированный текст - show sorted file do not change file

`sort numbers.txt` - show sorted numbers.txt(by char)

`sort -n numbers.txt` - show sorted numbers.txt(by numbers)



teamA.txt
1,Petya, PM, 45
2,Tanya, QA, 37
3,Sergey,Boss,36
4,Alina, FrontendDev, 23

`cut -d "," -f2 teamA.txt `  ***show 2 column

`cut -d "," -f2-3 teamA.txt `  ***show 2,3 column

`cut -d "," -f2 teamA.txt | sort ` ***show 2 column sorted by alphabet

`cut -d "," -f2 teamA.txt | sort -r `  ***show 2 column sorted by alphabet in opposite order

sort is sorting all as strings if we want sort numbers we should use `sort -n``sort -n -r` and | uniq `unic -c` **show uniq and quantity of duplicates

#### Grep

`grep`  - поиск определонного слова в файле и вывод строк с этим словом -find words in file and show strings with it

`grep error ./*` - find error in current directory in all files

`grep -i error ./*` - find error in current directory in all files ignore case sensitive

`grep -i error ./* | less` - find error in current directory in all files ignore case sensitive in editor

`grep .com logs.txt` - find ".com" in file logs.txt

`grep -E "[A-Za-z]*@[A-Za-z]*.com" logs.txt` - find by regexp in file logs.txt

`grep -E "(dev.gov|dev.com)" logs.txt` - find by regexp "dev.gov" or "dev.com" in file logs.txt

1. Make the search case-insensitive with the "-i" option:
`grep -i 'searched-word' filename`

 
2. Search recursively in all files in a given directory with the "-r" option:
`grep -ir 'searched-word' '/directory'`

 
3. Search whole words only with the "-w" option:
`grep -irw 'searched-word' '/directory'`

 
4. Print the line numbers in which the searched word was found with the "-n" option:
`grep -irwn 'searched-word' '/directory'`

 
5. Search for multiple words syntax:
`grep -ir 'word1|word2|word3' '/directory'`


`sudo apt install searchmonkey` GUI app for search

`grep -rl "string" /path`
where

`-r `(or --recursive) option is used to traverse also all sub-directories of /path, whereas
`-l `(or --files-with-matches) option is used to only print filenames of matching files, and not the matching lines (this could also improve the speed, given that grep stop reading a file at first match with this option).

`grep -Hrn 'search term' path/to/files`

`-H `causes the filename to be printed (implied when multiple files are searched)
`-r `does a recursive search
`-n `causes the line number to be printed
path/to/files can be . to search in the current directory

Further options that I find very useful:

`-I `ignore binary files (complement: -a treat all files as text)
`-F `treat search term as a literal, not a regular expression
`-i `do a case-insensitive search
`--color`=always to force colors even when piping through less. To make less support colors, you need to use the -r option:

`grep -Hrn search . | less -r`

`--exclude-dir=dir` useful for excluding directories like .svn and .git.

##### Time

-mtime

`find /home/analyst/projects -mtime -3` - returns all files and directories in the projects directory that have been modified within the past three days

The `-mtime` option search is based on days, so entering 

`-mtime +1` indicates all files or directories last modified more than one day ago, and entering

`-mtime -1` indicates all files or directories last modified less than one day ago. 

Note: The option `-mmin` can be used instead of `-mtime` if you want to base the search on minutes rather than days.


##### Regular expression / Регулярные Выражения:

`[A-Z]*`  - любое слово из больших букв - any word upper case

`[a-z]*`  - любое слово из строчная букв - any word lower case

`[0-9]*`   - сколько угодно подряд стоящих цифр - any numbers

`\.` - "."

`[A-Za-z]*@[A-Za-z]*.com`   – простое выражение емайлов с окончанием .com  - simple expression with ".com"

`www\.[a-z]*\.com`  - любой вэб адресс  с окончанием .com - any web address with ".com"

### Redirecting IO

[Content](#content)


output linux

`1` -standart

`2` -errors

redirecting

`>`    write(add file or recreate file)

`>>`   append(add to file if present or create file)

`ls 1>out.txt`

`ls 1>>out.txt`

#also we can dont specify 1
`ls >out.txt`


`daslklfa 2>err.txt`

`daslklfa 2>>err.txt`

`ls 1>out.txt 2>err.txt`

`ls 1&2>out.txt   === ls &>out.txt `


`sort names.txt > sorted_names.txt` - sort file names.txt and record to new file sorted_names.txt

`sort -n numbers.txt > sorted_names.txt` - sort by number numbers.txt and rewrite(will be deleted info wich was in file) to sorted_names.txt 

`sort names.txt >> sorted_names.txt` - sort names.txt and add to sorted_names.txt (not rewrite)

`sort names.txt > names.txt` - firstly create file then sort(!!! will be empty )

`sort -n numbers.txt >> numbers.txt` - sort by number numbers.txt and add sorted to numbers.txt

`grep sv /etc/* 2> errors.txt` - find sv in directory /etc/ and subdirectories  if error write to file errors.txt (2> - mean redirect bad responses)

`grep sv /etc/* 2> /dev/null` - find sv in directory /etc/ and subdirectories  if error write to no present device(2> - mean redirect bad responses)

`/dev/null`   - устройство находящиеся - no present device

`grep sv /etc/* > good.txt 2> errors.txt` - find sv in directory /etc/ and subdirectories good response write to good.txt if error write to file errors.txt (2> - mean redirect bad responses)

`grep sv /etc/* > good.txt` - find sv in directory /etc/ and subdirectories good response write to good.txt

`grep sv /etc/* &> results.txt` - find sv in directory /etc/ and subdirectories good and bad response write to results.txt

`2>> errors.txt` - add errors to errors.txt


### Zip

[Content](#content)

`tar cf  mytar.tar  Folder1`   - заархивировать Folder1 - create tar from folder Folder1(f always last)

`tar cvf mytar.tar Folder1` - create tar from Folder1 (v - verbbose - show what do)

`tar xf mytar.tar`  - разархивировать архив - unzip mytar.tar

`tar xvf mytar.tar`  - разархивировать архив - unzip mytar.tar and show what do

`tar tf mytar.tar` - show what contains mytar.tar

`tar cvzf myBZIP2.bz2  Folder1`    – сжать Folder1 - compress folder

`tar xvf  myBZIP2.bz2`   - распаковать архив - uncompress folder

`tar tf myBZIP2.bz2`    - посмотреть что внутри архива - show what inside 

`tar cvzf myGzip.gz Folder1` - create myGzip.gz from Folder1 and show what do

`tar cjf myBzip.bz2 Folder1` - create myBzip.bz2 from Folder1

`tar cJf myXz.xz Folder1` - create m myXz.xz from Folder1

`gzip     / bzip2     / xz`      – скомпрессировать файл -compress file

`gunzip /  bunzip2 / unxz`  – раскомпресировать файл - uncompress file

`gzip mytar.tar` - compress mytar.tar

`gunzip mytar.tar.gz` - decompress mytar.tar

`bzip2 mytar.tar` - compress mytar.tar compress more than gzip

`bunzip2 mytar.tar.bz2` - decompress mytar.tar

`xz mytar.tar` - compress mytar.tar also compress more than gzip but less than bzip2

`unxz mytar.tar.xz` - decompress mytar.tar

`zip –r myZIP.zip Folder1`- Запаковать Folder1 в ZIP - zip Folder1 to zip to compatible with windows

`unzip myZIP.zip`         - Распаковать файл myZIP.zip - unzip file myZIP.zip


### Memory and Processes

[Content](#content)

`top` – как Task Manager в Windows - taskmanager Linux then (`shift+p`-show max by processor)(`shift+m` - show max by memory) to exit `q`

`free`  - показать состояние памяти в байтах - state memory bytes

`free –h`  - показать состояние памяти в MB, GB - state memory MB, GB

`ps`          -  показать мои процессы - show current user processes

`ps -u name` -show processes for user "name"

`ps aux`  - показать все процессы от всех пользователей - show processes all users

`ps aux | grep bash`  - найти все процессы bash от всех пользователей - show all processes for all users where bash

`ps aux | grep -i “name of your desired program”`

`sudo kill -9 $(sudo lsof -t -i:8000)` - kill process on 8000 port

`sudo kill -9 process_id`

init the first process when run and has ID=1


Each process has parent

`less /etc/my_file | grep Hello `-less(parent) grep(child)

`ps -x `-showsnapshot of the current processes

status: R-running, T-stopped, S-interruptible sleep
Time -total CPU time that process has taken up

`ps -ef `-e(all processes from all users)f(full info)

it shows pid(id) ppid(parent id) c(number of children) tty(terminal)
cmd(comand line) 

`ps -ef | grep Chrome `-find Chrome process

`ls -l /proc  `-files that correspond to processes

`cat /proc/1805/status `-show about process number 1805 status

sigint `ctrl+c`

`kill 10234 `-kill prrocess number 10234

`kill -KILL 10234 `-kill prrocess number 10234 last resort

`kill -TSTP 10234 `-suspend(pause) prrocess number 10234 

`ctrl+z` equals TSTP(suspend)

`kill -CONT 10234 `-resume prrocess number 10234 

`top` -show resources
`Q `  -quit

`uptime` -time, user, load average

`lsof` -list processes to find holding open files



#### Logs

[Content](#content)

`cd /var` - root directory with logs

`cd log` - log directory

`dmesg` - log Linux kernel

logs `/var/log`

`ls /var/log `-show logs

most important file

`less /var/log/syslog`

`less /var/log/syslog | grep error`

`tail -f /var/log/syslog `-show last and then we can monitor




### Accounts

[Content](#content)

Type:

-root

-administrator(can use sudo)

-standart(cannot use sudo)

`cat /etc/group ` -show users

sudo:x:27:username - x(cripted password), 27(group №), username(login)

`cat /etc/passwd `-show passw

root:x:0:0:root:/root:/bin/bash - root(username), x(password which stored in other file),
:0:0(uid),

`/home` - directory with user's  folders

`sudo`  - запустить комманду используя Super User права - run comands from super user

`sudo ` means superuser do

`su` substitute user

`sudo su`

`su`- сменить текушего пользователя - change current user

`su petya` - change user to petya

`/etc/passwd`    - тут хранятся все аккаунты - here saved all accounts

`/etc/shadow`   - тут хранятся все пароли аккаунтов - here all passwords for accounts

`/etc/group`    - тут хранятся все группы - here all groups

`whoami`  - показать имя текущего пользователя - show name current user

`id`   - показать к каким группам принадлежит пользователь - show groups for user. For other user `id name` - show groups for name(user)

`who` – показать кто сейчас в системе - show users in system

`w`   - показать кто сейчас в системе и что делает - show who in system and what doing

`last` – показать последние логины - show lst logins

#### Work with users

`sudo useradd  -m vasya`   - создать юзера vasya с домашней  директорией - add user vasya

`sudo userdel –r vasya`     - стереть юзера vasya с его домашней  директорией - delete user vasya

`/etc/skel`    -  это шаблон домашней директории -template for home directory. When we create new user files from here copy to user directory

`sudo passwd vasya`   - изменить пароль для юзера vasya - change password for vasya

`passwd username `-change password for username

`sudo passwd -e username ` - expire password for username

`/etc/shadow ` -dir with passwords



#### Work with groups

`sudo groupadd Programmers`  - создать группу Programmers - create group Programmers

`sudo groupdel Programmers`  - стереть группу Programmers - delete group Programmers

`sudo usermod –aG Programmers vasya`  - добавить юзера vasya в группу Programmers -add user vasya to group Programmers

`sudo deluser vasya Programmers`  - удалить юзера vasya  из групы Programmers - remove user vasya from group Programmers


#### Access rights

`-rw-rw-r--1 user user date user.txt`

`drw-rw-r--1 user user date user.txt`

1st `-` -mean file if `d` -mean directory if `l` -mean link

2d `rwx` if no one `-`(rw-)

3d `rwx`(rw-)

4th `rwx`(r--)  - permissions to other who not user and not in group

5th `1` -mean links to file(based on 1st parameter) if directory -mean quantity of files inside directory

6th `user` - user to this user `2d` permissions

7th `user` -group to this group `3d` permissions

`rwx` - rights: `r`-read and visible for directory; `w` -write,delete,create; `x` - run for script and enter for directory

`ls -l /usr/bin/passwd` `-rwsr-xr-x`

s means substituted (we can work as an owner)

`sudo chmod u+s myfile `-enable s

`sudo chmod 4755  myfile `-enable s

SetUID - work as an owner

SetGID - run a file as a group member

`ls -l /usr/bin/wall`  `-rwxr-sr-x`

`sudo chmod g+s myfile `-enable s

`sudo chmod 2755  myfile `-enable s

Sticky bit - sticks file or folder down
anyone can write to file or folder but only owner can delete

`ls -ld /tmp` `drwxrwxrwt`  

t- all can add and modify files in /tmp

`sudo chmod +t myfolder `-enable t

`sudo chmod 1755  myfolder `-enable t



`chown` – изменить владельца файла / директории -change owner file / directory

`sudo chown joe user.txt` – change owner file(user.txt) to joe

`chgrp`– изменить группу файла / директории - change group file /directory

`sudo chgrp Programmers user.txt` - change group file (user.txt) to Programmers

`сhmod` – изменить права доступа на файл / директорию - change rights for file or directory

`sudo chmod  o+x  myfile.txt`   довавить X всем - add all(other user) right to execute(run) file myfile.txt

`sudo chmod  ugo+x  myfile.txt`   довавить X всем - add all(other user) right to execute(run) file myfile.txt

`sudo сhmod  g-rw   myfile.txt`   убрать RW у группы - delete permission to read and write for group myfile.txt

`sudo chmod  o=rw   myfile.txt` -  установить RW всем остальным -add all(other user) right to read and write file myfile.txt

 `u`= user;  `g` = group;  `o` = other; `a`= ugo -all

`sudo chmod  777   myfile.txt` -  установить RWX всем - add for all rights rwx for file myfile.txt

`sudo chmod  741   myfile.txt` - установить:   RWX   владельцу, R - -    группе,  - - X   всем остальным - owner all rights, read for group, execute for others

```
777 
rwx=7=4+2+1
r = 4
w = 2
x = 1
rw- =6=4+2+0
r-x=5=4+0+1
r--=4=4+0+0
-wx=3=0+2+1
-w-=2=0+2+0
--x=1=0+0+1
---=0=0+0+0
```
`sudo chmod  o+t myDir/`  -  включить StickyBit - turn on StickyBit mean others cannot remove files if they no have permission to file but have all permissions for directory

`sudo chmod  o-t myDir/`  -  выключить StickyBit - turn off StickyBit mean others can remove files if they no have permission to file but have all permissions for directory

`sudo chmod  1777 myDir`  -  включить StickyBit - turn on StickyBit `1` -mean add

`sudo chmod 0777 myDir`   - выключить StickyBit - turn off StickyBit `0` -mean delete


### Network

[Content](#content)

`ifconfig `     - показать мой IP адресс -show IP 

`ip addr show`- показать мой IP адресс - show IP

`route`      - показать адресс раутера Gateway - show adress gateway from wich you send packages to internet

`ping`        - протестировать коннекшен к адрессу - test connection

`ping 8.8.8.8` - google dns 

`ping -c 4 8.8.8.8` - ping 4 times google dns then exit

`traceroute www.google.com` - show 

`host`- дать IP адресс вэб сайта - show ip by domen

`host www.ebay.com`

`dig `        - дать IP адресс вэб сайта - show ip by domen

`netstat`– выдать сетевые подключения компьютера -show connection pc

`sudo ufw allow 22` - open your port

`sudo apt-get install openssh-server` - install server for connection from your server to others

`ssh MyLinux` - connect to own linux(name pc)

`sudo lsof -i -P -n | grep LISTEN` - check ports

`sudo lsof -t -i:8000` - check 8000 port

`telnet localhost 4222` - check

`sudo lsof -i -P -n | grep LISTEN `  **check ports

`ps aux  `                                  **check process

`ps aux | grep -i “name of your desired program”`

`sudo lsof -t -i:8000`

#### Change IP

`hostname`    - вывести название компа -current name PC

`sudo hostname MyLinux` - переименовать в MyLinux -rename PC to MyLinux

`/etc/hostname`  - тут прописано название компа - here file `sudo nano /etc/hostname`

`/etc/hosts`   - тут прописываем новое название напротив IP адресса - here change name `sudo nano /etc/hosts`

`ifconfig`   - вывести текущий IP адресс - show current IP

Временно меняем IP адресс так: / temporary change IP
`sudo  ifconfig  enp0s3  10.10.10.10  netmask  255.0.0.0`

`/etc/network/interfaces`  - тут прописываем постоянный IP - here write static IP 

`sudo nano /etc/network/interfaces` and add enp0s3(name network card from command `ifconfig`)

```
auto enp0s3
iface enpp0s3 inet static
address 20.20.20.20
netmask 255.0.0.0
gateway 20.20.20.1
dns-namesrvers 8.8.8.8
```

`sudo ifdown enp0s3`    - отключить сетевуху eth0 - turn off network card

`sudo ifup   enp0s3`      - включить сетевуху eth0 - turn on network card

#### Connect to remote Linux

`ifconfig` - get inet 192.168.10.130

`ping 192.168.10.130` -check connection

`service ssh status`   - статус SSH сервиса -ssh status

`service ssh start`- запустить SSH сервис - run ssh

`sudo apt-get install openssh-server`   - установить SSH - install ssh

`ssh vasya@192.168.10.130`   - подключится к компу (192.168.10.130) как пользователь (vasya) if user don't have need to create or use known(by default when connect it use your current user)


`ssh -p 2022 ivan@localhost`

we can use predefinet file
https://www.ssh.com/academy/ssh/config


#### From windows

##### Putty

1) download `putty`

2)enter Ip remote port 22

3) connect

##### mobaXterm

1) download

2) session ssh enter ip port and user

3)connect(you can save password)  and you can split

### Install programms

[Content](#content)

`wget adress`    - скачать файл из интернета - download file from internet adress

#### Ubuntu/Debian/Kali/Mint Linux:

`sudo apt-get install name`     - скачать и установить программу -download and install programm name

`sudo apt-get remove name`   - удалить программу - remove programm name

`sudo dpkg –i name.deb`                - установить программу из файла .deb - install programm from file name.deb

`sudo dpkg –r name`                - удалить программу -delete programm name

`sudo name` - run programm name


`sudo apt install gimp`

`sudo apt remove gimp`

`/etc/apt/sources.list -repos apt`

`sudo apt update`

`sudo apt upgrade`

`man apt-get`

`sudo apt update -y`


#### RedHat/CentOS/Amazon Linux:

`sudo yum install name`          - скачать и установить программу -download and install programm name

`sudo yum remove name`         - удалить программу - remove programm name

`sudo rpm –i name.rpm`                  - установить программу из файла .rpm -install programm from file name.rpm

`sudo rpm –e name`                 - удалить программу -delete programm name.rpm


### Environment variables

[Content](#content)


``/.bashrc` - это файл скрипта, который выполняется при входе пользователя в систему

`cat .bashrc | grep JAVA_HOME` find variable JAVA_HOME


`VALUE=25` - local variable

`echo $VALUE` - show variable

!!!! difference between '' and "" we can use $VALUE

`TEST='HEllo'`

`TEST1="HELLP $VALUE"`


`export VAL=27`- global variable

`printenv` - print variables

`echo VAL` - show variable

`printenv VAL` - show variable


`PATH` where our commands if we want create own we should add our to these directories or change path var

`PATH=$PATH:/path_to_our_directory`



`tail -4 .bashrc` - 4 last variables

`export VAL=7` - add variable

`tail -4 .bashrc` - 4 last variables

`echo $VAL` - show variable

`echo 'export VAL=7'>> .bashrc` - add variable

`tail -4 .bashrc ` - 4 last variables

#### to reread .bashrc and see updates

`source .bashrc `

`. ./.bashrc`

`. .bashrc`



### Bash

[Content](#content)

https://google.github.io/styleguide/shellguide.html

https://www.gnu.org/software/bash/manual/bash.html

#### how works bash and zsh

has 2 file

`.bash_profile`  or `.zprofile`   - profile

`.bashrc`        or `.zshrc`      - run command



`myscript.sh` - name script always end .sh

##### myscript.sh

```
#!/bin/bash        # comment: always start script

echo "Hello script"  # we can use commands
echo "Let`s show files in this folder"
ls
xterm &             # run terminal, & - mean don't want
ls -l 
<<COMMENT
    This is a multiple line comment
    In Bash Scripting, print Done
COMMENT
echo "Done"

```

##### run script

`bash myscript.sh` - run script using bash

To run without `bash` we need in rights add `x`

`sudo chmod a+x myscript.sh` - add rights to run script

`./myscript.sh` - run script

`export PATH=$PATH:$PWD` - if we want to run often script we can add to PATH AND then we can run `start-app`


##### Script result

after each work of script or utils they return status code

`test` - util that work with file, dir, strings and numbers

`test 10 -lt 5 ` - check if 10 less than 5

`echo $?` -return status code

`0 `- true
`1` - false


`[ 10 -lt 5 ]` -  syntax sugar on test legacy

`[[ -d .idea ]]` -  syntax sugar on test modern for file or strings


`(( 10 -lt 5 ))` syntax sugar on test modern for numbers
`(( 10 > 5 ))`


##### run a few comands

`cd my_dir ; ls`  - if first fall second work normally


`cd my_dir && ls` - if first fall second don't run


`cd my_dir || ls` - if first fall second work normally, if first run second don't run



##### my2.sh

```
#!/bin/bash       

myPC="sv"  # variable (!don't use whitespaces)
myOS=`uname –u` # record to variable name system
echo "Name of script is $0"

echo "Hello $1" # myPC
echo "Hello $2" #myOS

num1=10
num2=20
sum=$((num1+num2))
echo "$num1 + $num2 = $sum"
myhost=`hostname` #`` -for system variables
mygtw="8.8.8.8"

ping -c 4 $myhost
ping -c 4 $mygtw

echo -n "is done..." # -n -means no new line
echo "all done"
```

`./my2.sh  Vasya  Petya  Kolya`

`$0` -  при этом равен  ./myscript.sh  -always name script

`$1` - при этом равен Vasya - first argument

`$2` -при этом равен Petya - second argument

`$3`- при этом равен Kolya - third argument

myOS=`uname –u`   - запускает uname –u и сохраняет  результат в переменную myOS - save I argument
```
# Сохранить ввод пользователя в переменную name:
# Save Input to variable name
read –p “Please enter your name: “ name
```

##### my3.sh if and switch

```
#!/bin/bash       
# start
if["$1"=="Vasya"]; then
echo "Hi $1"
elif["$1"=="Joe"]; then
echo "Hello $1" 
else
echo "Welcome $1"
fi 
# end
# start switch
x=$2
echo "Start CASE"
case $x in
  1) echo "One";;
[2-9]) echo "two to nine";;
"Petya") echo "Hello $x";;
*) echo "Unknown parameter" # other case
esac
#end switch

```
`bash ./my3.sh Vasya 3333` - run script

##### my4.sh while and for

```
#!/bin/bash       
# start
COUNTER=0 # variable
while [$COUNTER -lt 10]; do
echo "Current counter is $COUNTER"
COUNTER=$(($COUNTER+1))
done
# end
<<COMMENT
Other variants
    let COUNTER=COUNTER+1
    let COUNTER+=1
COMMENT

# start
# this loop read all files "*.txt" and show to console
for myfile in `ls *.txt`; do
cat $myfile
done
$ end

# start

for ((i=1; i<=10; i++)); do
echo "number i = $i"
done
# end

# start

for x in {1..10}; do
echo "x = $x"
done
# end

```
`bash ./my43.sh` - run script

##### my5.sh  function

```
#!/bin/bash       
sum=0

myFunc()
{
echo "text from func"
echo "first param is $1"
echo "second parameter is $2"
}

myFunc1()
{
echo "text from func"
echo "first param is $1"
echo "second parameter is $2"
sum=$(($1+$2))
}
# start
myFunc
myFunc1 50 10
echo "sum is $sum"
# end

```
`bash ./my43.sh` - run script


### HDD

[Content](#content)

`sudo fdisk -l` - show disks

`/dev/sda`    - первый SATA диск - first disk

`/dev/sdb`    - второй SATA диск -second disk

`/dev/sdc`    - третий SATA диск -third disk

`fdisk –l`    -  показать какие есть диски show disks

`lsblk`        -  показать какие есть диски - show tree disk

`sudo cfdisk   /dev/sdb`  - редактировать разделы sdb диска - change disk's partitions 

`mkfs.ntfs  –f  /dev/sdb1`   - форматировать  раздел первый второго диска - format disk

`/etc/fstab`   - тут прописываем новые диски чтобы они присоединялись автоматически при загрузки Линукса - add to table for visible

```
create dir hdd2 /media/hdd2(by default own new disk add to /media/user)
then redact file
/etc/fstab:
/dev/sdb1 //media/hdd2 ntfs default 0 0
```


`du -h `-show disk usage show all without specification

`df -h `-free space

`sudo fsck /dev/sda `-auto repair file system


`sudo mount /media/hdd2`   - присоединяет диск прописанный в файле fstab с именем hdd2 без перезагрузки Линукса - connect second disk

`sudo parted -l `-show mounted disks

`sudo parted /dev/sdb  `-connecto to usb flesh (name sdb if you have only one disk on pc)

`print `-print info about disk

`mklabel gpt ` -add lebel to disk gpt

`mkpart primary ext4 1MiB 5GiB ` -create partition name=primary, fs=ext4, start=1, size=5Gb
quit

`sudo mkfs -t ext4 /dev/sdb1 `-format partition

`sudo arted -l`

`mount usb`

first we should create directory

`cd ~/Desktop`

`mkdir my_usb`

`sudo mount /dev/sdb1 /my_usb/ `-mount usb to directory my_usb

`cd /my_usb/`

`sudo umount /dev/sdb1 `-unmount usb

`sudo umount /my_usb `-unmount usb

clone using dd connect usb then 
`sudo parted -l `-here find name_disk

`u`mount /dev/name_disk `-paste name_disk

`sudo dd if=/dev/sdd of=~/Desktop/my_image.img bs=100M `-copy image from desktop


`cat etc/fstab`

after restart we lose our usb and need to mount again
make it auto

`sudo blkid`


`swap`

`sudo parted /dev/sdb`

`mkpart primary linux_swap 5GiB 100% `-100%=rest space
quit

`sudo mkswap /dev/sdb2`

`sudo swap /dev/sdb2`

if you want auto mount swap add to `etc/fstab`



### Schedule

[Content](#content)

`crontab - l`    - показать расписание -show schedule

`crontab -e`   - редактировать расписание - redact schedule

```
*     *     *    *       *
min   hour  day  month   day of week

0-59  0-23  1-31  1-12   0-6(0=sunday)

* -every minute
*/2 -every 2 minutes
*/3 - every 3 minute

6,18 -on 6 and 18 minute
```

```
* * * * 5 echo "Hello!" >> /home/user/scripts/mylog.log # every friday every minute write to mylog.log "Hello!"
50 12 * * *  echo "Hi!" >> /home/user/scripts/mylog.log # every day 12:50 write to mylog.log "Hi!"

*/2 * * * * /home/user/scripts/mylog.sh # every 2 minute run script
```

`sudo cat /var/spool/cron//crontabs/user` - path to file(each user have its file)

`/etc/crontab`  - файл расписания на системном уровне -file with schedule system

`sudo nano /etc/crontab`  - edit file with schedule system

`sudo cat /var/log/syslog | grep CRON` - syslog filter CRON

### SDK

[Content](#content)

Installation

```
sudo apt-get install unzip 
sudo apt-get install zip 
curl -s "https://get.sdkman.io" | bash 
source "$HOME/.sdkman/bin/sdkman-init.sh"
```


Verify Installation
`sdk version`

` sdk list java`

`sdk current java`

`sdk default java ..`

`sdk use java ..`

`sdk install java 8.0.292.j9-adpt`


Install without sdkMan

`sudo apt install openjdk-8-jdk`



Check current JRE:

$ java -version

Check current JDK:

$ javac -version



. Switch JRE version
Check installed JREs:

$ sudo update-alternatives --config java
The response will look like:

There are 4 choices for the alternative java (providing /usr/bin/java).
```
  Selection    Path                                            Priority   Status
------------------------------------------------------------
* 0            /usr/lib/jvm/java-14-openjdk-amd64/bin/java      1411      auto mode
  1            /usr/lib/jvm/java-11-openjdk-amd64/bin/java      1111      manual mode
  2            /usr/lib/jvm/java-13-openjdk-amd64/bin/java      1311      manual mode
  3            /usr/lib/jvm/java-14-openjdk-amd64/bin/java      1411      manual mode
  4            /usr/lib/jvm/java-8-openjdk-amd64/jre/bin/java   1081      manual mode

Press <enter> to keep the current choice[*], or type selection number: 
Now you can switch to another JRE or keep the current version.
```
2. Switch JDK version
Check installed JDKs:

$ `sudo update-alternatives --config javac `
The response will look like:
```
There are 4 choices for the alternative javac (providing /usr/bin/javac).

  Selection    Path                                          Priority   Status
------------------------------------------------------------
* 0            /usr/lib/jvm/java-14-openjdk-amd64/bin/javac   1411      auto mode
  1            /usr/lib/jvm/java-11-openjdk-amd64/bin/javac   1111      manual mode
  2            /usr/lib/jvm/java-13-openjdk-amd64/bin/javac   1311      manual mode
  3            /usr/lib/jvm/java-14-openjdk-amd64/bin/javac   1411      manual mode
  4            /usr/lib/jvm/java-8-openjdk-amd64/bin/javac    1081      manual mode

Press <enter> to keep the current choice[*], or type selection number: 
Again, you can now switch to another JDK or keep the current version.
```
Step 3. Add JAVA_HOME environment variable
Java applications may use environment variables. JAVA_HOME is a common one so we will now we add this.

Edit /etc/environment file:

$ `sudo nano /etc/environment`
Add the following line to the file and save:

JAVA_HOME="/usr/lib/jvm/java-11-openjdk-amd64/bin/"
In the above example we are using Java 11.

To apply the changes you will need to log out then log in again. To apply the changes in your current terminal session use the source command:

$` source /etc/environment`
Check the environment variable was set:

$ `echo $JAVA_HOME`
The response should look like:

sr/lib/jvm/java-11-openjdk-amd64/bin/
We have now set up our Java environment for development.





### Solving problem 

commands when the problem with apache and root cause other programm

`sudo systemctl status apache2`

`sudo systemctl restart apache2`

`sudo systemctl status apache2`

`sudo netstat -nlp`

`ps -ax | grep python3`

`cat /usr/local/bin/jimmytest.py`

`sudo kill [process-id]`

`ps -ax | grep python3`

`sudo systemctl --type=service | grep jimmy`

`sudo systemctl stop jimmytest && sudo systemctl disable jimmytest`

`sudo netstat -nlp`

`sudo systemctl start apache2`



[Content](#content)
