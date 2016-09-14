# Files and Folders

### Resources

- [Remove Top Line of Text File with Powershell](http://stackoverflow.com/questions/2074271/remove-top-line-of-text-file-with-powershell)
- [Text File Tricks: Tail and Wait](https://blogs.technet.microsoft.com/heyscriptingguy/2013/02/24/weekend-scripter-two-way-cool-powershell-text-file-tricks-tail-and-wait/)
- [About Parsing](https://technet.microsoft.com/en-us/library/hh847892.aspx)
- [How To Build Events On New Files With WMI Events](http://www.tomsitpro.com/articles/build-events-wmi-events-powershell,2-12.html)

### Append to a file

```powershell
... | out-file <FILENAME> -append
```

### Bulk rename of folders

```powershell
ls -Directory <BASEFOLDER> | foreach-object {rename-item $_.fullname -NewName "$($_.fullname)zzz"}
```

### Copy names of folders to clipboard with whitespace removed from end

```powershell
ls -dir "\\brkdata\BCCData\Data" | select-object fullname | foreach {$_.fullname.ToString()} | clip
````

### Create a new file

```powershell
New-Item c:\scripts\new_file.txt -type file [-Force] [-Type ASCII]
```

- `-Force` will create the file even if one with the same name exists

### Check if a file exists

[Using the Test-Path Cmdlet](https://technet.microsoft.com/en-us/library/ee177015.aspx)

```powershell
Test-Path c:\scripts\test.txt
```

### Delete Files Older than a Date/Time

```powershell
Get-ChildItem -Path FILEPATH -Recurse -Force | Where-Object { !$_.PSIsContainer -and $_.CreationTime -lt  "2015-05-31 00:00:00" } | Remove-Item -Force
```

### Get Last X Lines of a File

```powershell
Get-Content <filename> -tail NUM_LINES [-wait]
```

- `-wait` will output as more lines are added to the file

### List files in a folder sorted by date

```powershell
ls | sort-object -Property LastWriteTime
```

### Search Files in a Folder for a Text pattern

```powershell
Get-ChildItem -recurse | Select-String -pattern "STRING-TO-SEARCH" | group path | select name
```

### Text File Manipulation

Read the contents of a text file and output to the console:
```powershell
Get-Content <filename> 
```

Read the contents of a text file and assign to a variable:
```powershell
$FileContents = Get-Content <filename>
```

Get the first x lines of a text file:
```powershell
(Get-Content <filename>)[0 .. x]
or
Get-Content <filename> -totalcount x
```

Get the last x lines of a text file:
```powershell
(Get-Content <filename>)[-1 .. -x]  #-1 is the last line in the file
```

Sort the lines alphabetically:

```powershell
(Get-Content <filename>) | Sort-Object
```

<a href="http://stackoverflow.com/questions/2074271/remove-top-line-of-text-file-with-powershell">Remove Top Line of Text File with Powershell</a> (Stack Exchange)<br>


### Text file encoding

- [PowerTip: Control Text-File Encoding with PowerShell](https://blogs.technet.microsoft.com/heyscriptingguy/2013/09/06/powertip-control-text-file-encoding-with-powershell/)

### Get AD Groups/Users for a folder

List the users/groups with access and their access level 

```powershell
Get-Acl | select -ExpandProperty AccessToString
```

List users/groups in a simple autosized table

```powershell
Get-Acl | select -ExpandProperty Access | select identityreference, filesystemrights | format-table -AutoSize
```

### Tail a file

```powershell
Get-Content c:\Windows\WindowsUpdate.log -Wait -Tail 0
```

- This command will show updates to the file as they happen
- Remove `-wait` and the 0 to X to get the last X lines of the file 

### Add AD account to folder

```powershell
$ACLCommand = "iCACLS.exe $FullHomeFolderName /grant:r $($ADAccountName):(OI)(CI)(M) /T /C"
