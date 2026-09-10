This is a cheatsheet for PowerShell commands and my understanding of them.

Get-Command -> acts as a built in search for commands in your current session
-CommandType -> filters the search by types, format: Get-Command -CommandType [type]
-Name -> filters the search by name, format: Get-Command -Name [name]

Get-Help -> manual for command, format: Get_Help [command]

Get-Alias -> displays a list of all active aliases

Set-Alias -> allows you to use shorter words for long values/data, like setting a path to a wordlist to just wd-list and using that insead

Find-Module -> search tool to find modules online (colletions of CMDlets(commands in powershell))
-Name -> filters by name

Install-Module -> install unit of commands (module)

Get-ChildItem -> list directories and files
-Path -> allows you to specify of what, eg. get the child items of ./Documents

Set-Location -> changes active directory (equivalent to cd)
-Path -> allows you to change to a specific directory

New-Item -> creates a file or folder
-Path -> allows you to dictate where to create it
-ItemType -> allos you to choose what you want to make, file, directory, etc.

Remove-Item -> revmoes items
-Path -> dictate what to remove from where

Copy-Item -> copies a file from one location to another
-Path -> location of file to copy
-Destination -> location of file/directory to copy to

Move-Item -> same as copy but move instead, so deletes the initial file after copying
-Path -> location of file to move
-Destination -> where to move the file to

Get-Content -> reads files (type or cat equivalent)

| -> pipeing allows you to redirect output (equivalent to >)

Sort-Object -> sorts objects by specific attributes, like files size

Where-Object -> filters the objects by a specific attribute
-Property -> allows you to set the attribute to filter by
-eq/ne/gt/lt/ge/le/... ->  operator that decides how the filder works based on a certain value
eg. Get-Command | Where-Object -Property Status -eq Stopped -> gets all the objects what have their status set to stopped

Select-String -> filter files by a specific string (like grep)

Get-FileHash -> calculates the hash of a file (in the hasing algorithm specified)

