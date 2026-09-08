This is a cheatsheet for JohnTheRipper commands and my understanding of them.

Basic format of command: john [options] [file_path] - or john.exe on windows

Automatic hash detection:

john --wordlist=[path_to_wordlist] [path_to_file_to_crack]

For specific hash:

john --format=[format]

Unshadowing:

john unshadow [local_passwd] [local_shadow]
local_passwd -> /etc/passwd -> contains user account info (other then the password hash which is replaced with an x)
local_shadow -> /etc/shadow -> contains the acctual encrypted password hashes, salt info and account expiration date
It's also better to redirect the output to a file to to crack later (eg. by adding > unshadowed.txt to the command)

For single cracking (mangling words):

john --single --format=[format] [path_to_file_to_crack]
file hashes must be in the format name:hash, eg. if you want to mage the word Plane, the format would be Plane:[acctual hash] in the file

Custom rules:

You can change the rules of how john does work in /opt/john.cfg and use them using --rule=[rule]