Q. How to explain the command/shell/terminal to a lay person.

A. The command line, also known as the terminal or shell, is a way to send text commands to a computer directly instead of going via a graphical user interface.  The responses are generally simple text listings, but could also be the results of running a command, script or program.  

Commands include:
pwd - (print working directory) which shows what directory, we are currently in; 
ls - lists all the files and directories in the current directory
cd - change directory up or down (to a sub-directory for example "cd sprint-1", up one level "cd .." or to a specific directory "cd /home/PeterTorr")
mkdir abc - creates a directory called abc under the current working directory.
rmdir abc - deletes the directory abc (if it is a sub-directory of the current working directory)
touch abc.md - creates an empty file called abc.md in the current working directory
mv abc.md .. - moves the file abc.md up one directory (..)
mv abc.md xyz.md - renames abc.md to xyz.md
cp abc.md abc - copies the file abc from the current working directory into the sub-directory abc
cp abc.md xyz.md - makes a copy of abc.md called xyz.md
cat command-line.md - outputs the entire contents of command-line.md
less command-line.md - pages through the contents of command-line.md (useful for longer files)
rm abc.md - deletes / removes abc.md
rm -r abc - recursively deletes / removes the abc directory and any of its child directories and files
Note: rm has no undo. It is done.

The > symbol can be used to send the output to a file (creates or overwrites the file). e.g. ls > ls.md could result in:
abc
abc.md
command-line.md
ls
ls.md

The >> symbols can be used to append the output to a given file (creates if not exists). e.g. ls >> ls.md could result in:
abc
abc.md
command-line.md
ls
ls.md
abc
abc.md
command-line.md
ls
ls.md

The < symbol can redirect standard input to a command

The | (pipe) symbol can be used to redirect the output of one command to the input of another. e.g. ls | less



Many commands take parameters to change the behaviour of the command.  e.g. 
ls -a - lists all files and directories, including hidden files and directories... i.e. those beginning with a . 
ls - results in 
abc  abc.md  command-line.md  ls  ls.md
ls -a - also shows the hidden files
.  ..  .git  abc  abc.md  command-line.md  ls  ls.md

ls -l - lists files and directories in their long form
ls -l results in
drwxrwxr-x+ 1 PeterTorr PeterTorr    0 Aug 11 12:24 abc
-rw-rwxr--+ 1 PeterTorr PeterTorr    0 Aug 11 12:23 abc.md
-rw-rwxr--+ 1 PeterTorr PeterTorr 2100 Aug 11 13:34 command-line.md
-rw-rwxr--+ 1 PeterTorr PeterTorr   36 Aug 11 12:41 ls
-rw-rwxr--+ 1 PeterTorr PeterTorr   72 Aug 11 12:49 ls.md

The 7 columns in the result refer to:
- Access rights (d for directory)
- number of linked files and directories, including the current (.) and parent (..) directories.  Counts the number of results from ls -l
- Owner username
- Group owner username
- Size of file in bytes
- Date and time last modified
- The name of the file or directory

ls -t - lists files and directories in order of last modified datetime



