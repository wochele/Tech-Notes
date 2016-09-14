# Objects

#### Sorting objects

- `Sort-Object` or alias `Sort` can sort based on a property
    - `Get-Process | Sort-Object -property VM [-descending]`
    - `Get-Process | Sort VM,ID -desc`

#### Selecting objects

- `Select-Object` or alias `Select` to specify objects to display
- Allows access to properties normally filtered out by the config rules
    - `Get-Process | Select Name,ID,VM,PM | ConvertTo-HTML | Out-File test3.html`
- `-First` and `-Last` Parameters will keep a subset of objects
    - `Get-Process | Select -First 10` keeps the first 10 objects
- The pipeline contains objects until the last command
- Objects may be changed into PSObject
- `Get-Process | Sort VM -descending | Select Name,ID,VM | gm`

#### Use parenthsis when command won't accept pipeline input

- `Get-WmiObject -class Win32_BIOS -ComputerName (Get-Content .\computers.txt)`
    - Parenthesis are executed first, create list of names
- 

