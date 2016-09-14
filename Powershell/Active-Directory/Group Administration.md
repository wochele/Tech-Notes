# Group Administration

### Add User to a Group

```powershell
Add-ADGroupMember "GroupNAME" -Member USERNAME
```
### Find names of groups containing a string

```powershell
Get-ADGroup -Filter {name -like "*STRING*"} | select name
```

Or use the description :

```powershell
Get-ADGroup -Filter {description -like "*STRING*"} | select name
```
### Get Members of a Group

```powershell
Get-ADGroupMember GROUP_NAME | select name
```

Add `-Recursive` to include members in nested groups

### Get the names of members of an AD group and pipe to the clipboard

```powershell
Get-ADGroupMember GROUP_NAME -server SERVER_NAME | select name | foreach {$_.name.ToString()} | clip
```
