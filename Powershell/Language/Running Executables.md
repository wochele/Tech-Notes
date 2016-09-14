# Running Executables

### Resources for Running Executables in Powershell

- [Technet: Running Executables](http://social.technet.microsoft.com/wiki/contents/articles/7703.powershell-running-executables.aspx)
- [Using the Invoke-Item Cmdlet](https://technet.microsoft.com/en-us/library/ee176882.aspx?f=255&MSPPError=-2147217396)

### Running executables with non-standard arguments

Using the stop-parsing symbol `--%`

```powershell
icacls X:\VMS --% /grant Dom\HVAdmin:(CI)(OI)F
```


