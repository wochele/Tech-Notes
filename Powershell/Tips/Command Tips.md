# Command Tips

#### Show a GUI interface for a command

```powershell
Show-Command COMMAND
```

#### Finding commands

```powershell
Get-Command [SEARCH_TERM_WITH_WILDCARDS]

# Search using -noun or -verb
gcm -Noun get*
gcm -Verb *event*

```

Alias - gcm

#### Finding command examples

```powershell
Help Get-EventLog -example
```

#### Finding about topics

```powershell
Help about*
```

#### Accessing online help

```powershell
Help Get-Eventlog -online
```
