# Running Executables in Powershell

- [PowerShell: Running Executables](http://social.technet.microsoft.com/wiki/contents/articles/7703.powershell-running-executables.aspx)

```powershell

foreach($Server in $ServerList) {
    Write-Host $Server; 
    $CMD = '.\PsInfo.exe'
    $arg1 = '\\'+$Server
    $arg2 = '-s'
    $arg3 = '>'
    $arg4 = ".\servers\$($Server).txt"
    
    & $CMD $arg1 $arg2 > $arg4
}

```
