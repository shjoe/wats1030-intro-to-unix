# *nix Scavenger Hunt

Complete the following challenges using the command-line interface on your favorite
Unix or Linux operating system. You are welcome and encouraged to consult any
additional documentation online or in books.

Please add your answers/responses/text pastes to the document after each prompt.

Note: For some of the challenges you will need to reference files included with
this repository, so you will need to fork the repo into your own Github account
and then clone it to your development environment.

## The Challenges

### Navigating the Filesystem

* Get an idea of where you are in the operating system. Use the `pwd` command to find your "path to working directory"--your current location in the filesystem of your devbox. *Paste the output of the `pwd` command here:* 

```
/c/Users/Shure/projects/wats1030-intro-to-unix
```

* Discover more about this filesystem. Use `ls` (the "list" command)to see what is in this directory. *What directories and files do you see when you run `ls`?* 

```
challenge_files  nix_scavenger_hunt.md          README.md
LICENSE          nix_scavenger_hunt_stretch.md  super_scavengers.md
```

* You can use *options* to modify how a command runs. Try using `ls -alh` to see the contents of your current directory. *How are the results different when you use the `-alh` options?*

```
total 78K
drwxr-xr-x 1 Shure 197121    0 Jan 14 18:40 .
drwxr-xr-x 1 Shure 197121    0 Jan 14 18:40 ..
drwxr-xr-x 1 Shure 197121    0 Jan 14 18:40 .git
drwxr-xr-x 1 Shure 197121    0 Jan 14 18:40 challenge_files-rw-r--r-- 1 Shure 197121 1.1K Jan 14 18:40 LICENSE
-rw-r--r-- 1 Shure 197121 5.7K Jan 14 18:48 nix_scavenger_hunt.md
-rw-r--r-- 1 Shure 197121  325 Jan 14 18:40 nix_scavenger_hunt_stretch.md-rw-r--r-- 1 Shure 197121 2.8K Jan 14 18:40 README.md
-rw-r--r-- 1 Shure 197121  268 Jan 14 18:40 super_scavengers.md

This option returns hidden files as well as more information regarding the files like file size and date of last change.
```

* The `man` ("manual") command tells you more about how any given command works. (*WARNING:* CodeAnywhere does not support the man command. You can click the following link to complete this task: http://man.he.net/). Run `man` to see instructions about how to use `man`. Then use `man` to learn what the `a`, `l`, and `h` options mean when used with the `ls` command. *Write down what those options do?*

```
`man -a intro`
           Display,  in  succession,  all  of the available intro manual pages
           contained within the manual.  It is possible to quit  between  suc-
           cessive displays or skip any of them.

           Shows all files including hidden files.
`man -l -Tdvi ./foo.1x.gz > ./foo.1x.dvi`
           This  command  will  decompress  and format the nroff source manual
           page ./foo.1x.gz into a device independent (dvi) file.   The  redi-
           rection is necessary as the -T flag causes output to be directed to
           stdout with no pager.  The output could be viewed  with  a  program
           such  as  xdvi or further processed into PostScript using a program
           such as dvips.

           Lists everything in long form.
`-H[browser], --html[=browser]`
              This  option  will  cause groff to produce HTML output, and will
              display that output in a web browser.  The choice of browser  is
              determined  by the optional browser argument if one is provided,
              by the $BROWSER  environment  variable,  or  by  a  compile-time
              default  if  that  is unset (usually lynx).  This option implies
              -t, and will only work with GNU troff.

              Print size in human readable format.
```

* Commands can also take *arguments*, which are usually the names of files or locations that you want the command to work with. Try running `ls /` to see what files are in the *root* directory of the filesystem. *What files and directories do you see listed?*

```
bin  cmd  dev  etc  git-bash.exe  git-cmd.exe  LICENSE.txt  mingw64  proc  ReleaseNotes.html  tmp  unins000.dat  unins000.exe  unins000.msg  usr
```

* A Unix filesystem has a few special shortcuts to refer to specific locations. `/` indicates the *root* of the filesystem, meaning the top-most directory in the filesystem hierarchy. Use the `cd` ("change directory") command to move to the root directory. (Hint: Use `man` to look up the `cd` command if you have any issues) *Then run `pwd` and paste the output here:*

```
/c/Users/Shure
```

* Another special shortcut in Unix is the `~` location. This indicates the *user root* directory, meaning the top-most directory in the hierarchy that comes below your user account. Use `cd` to move to `~`. *Run `pwd` and paste the response here:*

```
/c/Users/Shure
```

* Change directory into the `challenge_files` directory. Use `ls` to find only the files with a `.demo` pattern. *How many files do you find?*

```
3
```

* Use the `cd` command to move "up" one directory. *Where are you in the filesystem now?*

```
Shure@DESKTOP-JAOUQL9 MINGW64 ~
Back in the root
```

* Press the up arrow on your keyboard. *What just happened?*

```
Previous command auto populates.
```

* Press the up arrow a few more times. *What do you see?*

```
Previous command/s auto populate beginning with most recent executed command.
```

* Run the `history` command. *What do you see?*

```
History of commands as well as account details (email, user name).
```

### Observing the System

* Discover what account you are logged into using the `whoami` command. *What username are you currently using?*

```
Shure
```

* Discover who else is on your system with the `who` command. *Are any other users using your system? If so, list them here:*

```
No other users
```

* How long has your system been running? Use `uptime` to see, and *paste the result here:*

```
17:43:26 up 2 min,  1 user,  load average: 0.00, 0.00, 0.00t
```

* Run `ps aux` and review the results. (Hint: Use `man` to learn more about the `ps` command and options.) *How do you interpret what you see here?*

```
Snapshot of current processes.
```

* Run `top` and review the results. (Hint: You may need to use `ctrl-c` to get out of this app.) *How do you interpret what you see here?*

```
Realtime capture of current processes.
```

### Finding and Viewing Files

* Make sure you are in the `challenge_files` directory. Use the `*` wildcard to find all the files that have the word "credit" in the filename. *How many files did you find?*

```
2
credit_cards.txt  credit_cards2.txt
```

* Use the `more` command to view one of the `credit_cards` files you just discovered. (Hint: Type `q` to quit viewing the file. Press the `spacebar` to page down. Use your keyboard arrows to move up/down.) *What is the date in the file you have viewed?*

```
Last updated: 01-15-2015
```

* Use the `find` command to search for files more effectively. Search the sub-directories under `challenge_files` to find the location of the file named `modi_laboriosam.txt`. *Where is that file located?*

```
./tmp/modi_laboriosam.txt
```

* Use the `grep` command to search for text within a file. Use `grep` on all the `.user` files in `challenge_files` to find which files contain "WA" (the abbreviation for Washington state). *How many files did you find?*

```
2 files:
Britt-Erdman.user:O'Harachester, WA 37261
Lissie-Strosin.user:Jewessfurt, WA 00816-724
```

* Use the `-r` option of `grep` to *recursively* find the text "Waldo" hidden in a file somewhere under the `challenge_files` directory. *Paste the result showing the file and line where the word "Waldo" shows up.*

```
serial-numbers/eaque_molestiae.txt:Ut est maiores quia autem. Nisi modi Waldo sed corporis sit explicabo ut est. Et est placeat ea sunt sunt consectetur sunt incidunt. Explicabo vel esse blanditiis dolorem culpa non quia.
```

### Pipes and Connecting Commands

* Sometimes it's useful to output the results of a command to a text file for further analysis, reference, or processing. Try running `ls > files.txt`. Notice that the file `files.txt` was created. View that file using `more`. *What do you see in the `files.txt` file?*

```
01
2015_special_stuff.demo
Afton-Jast.user
Aimee-Maggio.user
Alfonso-Gottlieb.user
Allen-Kemmer.user
Almina-Cormier.user
Alta-Lemke.user
Amina-McGlynn.user
Anabel-Hammes.user
Ancel-Conn.user
Anjali-Halvorson.user
Ardath-Kuvalis.user
Avah-Dickinson.user
Ayaan-Stiedemann.user
Aylin-Grant.user
Bedford-Sipes.user
Benita-King.user
Benito-Stoltenberg.user
Beverlee-Moen.user
Brad-Thiel.user
Brayan-Douglas.user
Bria-Satterfield.user
Bridgette-Reichel.user
Britta-Hammes.user
Britt-Erdman.user
Bryant-Kuhic.user
Bryton-Aufderhar.user
Caitlin-Grady.user
Carroll-Hartmann.user
Claudie-McClure.user
Clemente-Haley.user
Cleo-VonRueden.user
cloaked-wookie.demo
Codie-Romaguera.user
Cooper-Reynolds.user
Corrie-Bogisich.user
credit_cards2.txt
credit_cards.txt
Dannielle-Green.user
Deedee-Jacobson.user
Desiree-Marks.user
Deven-Rutherford.user
Doyle-Jones.user
Dustyn-O'Connell.user
Elza-Mraz.user
Emory-Crona.user
Erin-Walker.user
Estela-Schultz.user
Fernanda-Tromp.user
files.txt
Fletcher-Rice.user
Fred-Ryan.user
Genie-Abshire.user
Grace-Tromp.user
Grant-Cronin.user
Hali-Roob.user
Harland-Schoen.user
Harrell-Quitzon.user
Hillard-Ziemann.user

Seems to be the titles to all the files in the challenge files subfolder.
```
* Notice that if you run `ls -alh` in the `challenge_files` directory, the files scroll by very quickly. Sometimes it would be better to get the results in a paginated format. Try running `ls -alh | more`. *Describe what you see when you run `ls -alh | more`.*

```
Same list of files with details but fewer returns (easier to see) and an option to see more of the list.
```

* Earlier, when you viewed the list of active processes on your devbox using `ps aux`, the list was probably really long. You can make this list more manageable by using the pipe (`|`) to filter the results of `ps` using `grep`. Run `ps aux | grep <your_username>` to see what processes are running for your specific user. *Paste the list of processes that reference your username here:*

```
cabox      555  0.0  0.4  12888  1072 pts/0    S+   02:01   0:00 grep --color=auto Shure
```
