This is a cheatsheet of cmd commands and my understanding of them.

ver -> shows version of os

systeminfo -> shows system information

driverquery -> displays a list of installed device drivers

| more -> can add to any command and allows you to display the output page by page, Q to exit, spacebar moves 1 pg, enter moves 1 line

help -> add to a command for info

cls -> clear the CLI

set -> chesks your path from the command line

ping -> checks if the server can access a particular server on the internet, format: ping website.com

tracert -> traces the path of a rout (shows the router hops, if visible), format: tracert target_name

nslookup -> looks up host or domain and retuns ip address, format: nslookup website.com

netstat -> displays current netowrk connections and listening ports
-h -> help page
-a -> all established connections and listening ports
-b -> shows programs associated with connections and listening ports
-o -> shows process id
-n -> numerical form of addresses and port numbers
these ca be used in combination eg. netstat -abon

cd -> displays current directory, also used for chsanging directory, eg. cd .. will go to the directory your current directory is in

dir -> displays files and directory of current directory (like ls for linux)
/a -> shows hidden
/s -> shows files in curent directories and all sub directories

mkdir -> make directory, format: mkdir directory_name

rmdir -> romove directory, format: rmdir directory_name

type -> reads file (cat in linux), format: type file_name

copy -> copies files, format: copy file file_to_copy_to

move -> moves files, format: move file where_to_move

del -> deletes file

erase -> erases file

tasklist -> shows running processes
/? -> help page
/FI -> allows you to filter, format: tasklist/FI "filter_name operator value", eg. tasklist/FI "IMAGENAME eq program.exe"
(eq -> operator for equal)

taskkill -> kill a task
/PID -> specify which task by pid, eg. taskill/PID 1123

chkdsk -> check file system and disk volume for errors and bad sectros

sfc /scannow -> scans system files for corruption and repairs them if possible




