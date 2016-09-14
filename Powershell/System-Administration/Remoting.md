# Remoting

- Commands are run on the remote computer and only results come back
- Uses WS-MAN (Web Services for Management) communication protocol for HTTP or HTTPS
- Service it uses is WinRM (Windows Remote Management)
- Output from the commands are serialized into XML and transmitted back, then deserialized into objects on the other end

#### 1 to 1 remoting

- Accessing a shell prompt on a remote computer
- Uses a fraction of the overhead that RDP requires
- Establish connection to remote computer
    - `Enter-PSSession -computerName Server-R2`
- Security token passed to remote maching by kerberos and will run under same credentials
- Uses remote computer's execution policy
- Exit the session
    - `Exit-PSSession`

#### 1 to many remoting

- Use `Invoke-Command` for 1 to many remoting
- `Invoke-Command -computerName Server-R2,Server-DC4,Server12 -command { Get-EventLog Security -newest 200 | Where { $_.EventID -eq 1212 }}`
    - `-command` is alias for `-ScriptBlock`
- Can also specify a script to send to the remote computers
- 
#### Running a remote session against another computer with Enter-PSSession

PSSessions cannot be scripted and are to be used interactively.  I was looking for a way to run a script against a remote computer.  The solution I found was to use Invoke-Command with a scriptblock

First, create the scriptblock containing the commands to be run on the remote computer.  These will run natively on the remote machine and regular executables can be run.
```powershell$RemoteScript
$RemoteScript = { 
    omnicellinfo -cell > C:\users\user1\clientlist.txt
    . . . <add more lines here> . . .
}
```

Next, execute the script block on the remote computer

```powershellInvoke
Invoke-Command -ComputerName <RemoteComputerName> -ScriptBlock $RemoteScript
```

Here is an older command I used to launch a script from a different file

```powershell
Invoke-Command -computer $CellManager -FilePath .\Include\RunReportGroup.ps1 -ArgumentList $SessionID
```
