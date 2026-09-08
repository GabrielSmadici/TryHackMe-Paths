This is a cheatsheet of linux commands and my understanding of them.

echo {a} -> prints 'a', if the 'a' has a space quotations marks are required (eg. echo "hello world")

whoami -> prints the user

ls -> lists files and directories
-a -> shows hidden files
-lh -> shows permissions to files (r/w,rw)

cd -> change directory

cat -> read flies

pwd -> lists the path to the current directory you are in (eg. you are in home directory, it whould print /home)

find ->finds files
-name -> in the format find -name "name of file" it will show the path to the file
can also be used to find files by filetype, format: find -name *.txt, would find all .txt files

grep -> searchs and prints line where the text appears in a file, format: grep "text to find" "file-name"
-R "text" /directory/ -> searches all the files iin the directory and it's subdirectories
-i -> case-insensitive

& -> run commands in the background of your terminal
&& -> combine mutiple commands in 1 line
> -> redirects output
>> -> redirects output but appends, doesn't replace

ssh -> remote connect, format: ssh user@machine.ip

man -> manual for a command

touch -> create a file

mkdir -> create folder

cp -> copy file or folder

mv -> move file for folder

rm -> remove file
-R -> to romve directory

file -> determines type fo file

su -> switch user, format: su user
-l -> also switches user but also switches to the new user's home directory

Permissisons:
-read (4)
-write(2)
-execute(1)
-the numebrs add up depending on what you can do, so for exmaple if you can add all 3, the number would be 7
-files have premissions set up for 3 types fo users, the owner, the group and other users, so each files has 3 numbers eg.760

chmod -> changes permissions, format: chmod 777(the numbers from above) file.txt

wget -> downloads file, format: wget ip/file

scp -> copies file from remote computer to host and vice versa
-from remote computer to host format: scp user@ip:path/file file_to_copy_to
-from host to remote computer format: scp file user@ip:path/file
- basic idea of format, source first-destination second

ps -> provides a list of running processes, their status codes, session that is running it, how much usage time of the cpu, name of program/executed command
-aux -> see processes run by other users and those that don't run from a session

top -> real time statistics about the processes running on your system, you can refresh them with arrow key or they autop refresh every 10 seconds

kill -> kills process, format: kill PID(eg. 1137)

sigterm -> kills process with clean up beforehand
sigkill -> just kills
sigstop -> stops/suspends process

systemctl -> performs actions on service, format: systemctl option(start/stop/enable/disable) service(app)

CTRL+Z -> backgrounds the process (like &)

fg -> foregrounds the process

apt - > install software


 