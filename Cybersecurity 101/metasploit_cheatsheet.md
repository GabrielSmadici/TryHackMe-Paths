This is a cheatsheet for metasploit commmands and my understanding of them.

msfconsole -> opens metasploit console

use -> changes module used

show options -> shows context working in

back -> leave context

search [exploit] -> searches for exploits that you want to use, format: search CVE/exploit_name/...

info [exploit] -> gives information about an exploit

set -> sets parameters for the exploit you are using, format: set [parameter name] [value]

setg -> set but globally, ie. for all modules

exploit/run -> runs the epxloit, CTRL+Z to background the session

sessions -> see sessions
-i -> show sessions number

msfvenom --list payloads | grep meterpreter -> this is a command i've used in a lab environment that works as a remote connection that allows me to run commands direclty on the target machine, the exploit used to run meterpreter on the target is know as EternalBlue and it targets a vulnerability with SMBv1 allways being enabled in older versions of Windows.

