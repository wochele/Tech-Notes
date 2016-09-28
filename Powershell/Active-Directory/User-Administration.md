# User Administration



### Get a list of groups a user is in

```powershell
Get-ADPrincipalGroupMembership 61408a | select name
```
### Check if AD User Exists

```powershell
$ADUser = Get-ADUser -Filter {SamAccountName -eq $User.Name}
```

- If user does not exist $ADUser will be $null
- [Get-ADUser Default and Extended Properties](http://social.technet.microsoft.com/wiki/contents/articles/12037.active-directory-get-aduser-default-and-extended-properties.aspx)

![](http://admin-tools.com/assets/ExtendedProperties.jpg)

![](http://admin-tools.com/assets/ExtendedProperties2.jpg)

### Remove User from a Group

```powershell
remove-adgroupmember "GroupNAME" -Member USER_NAME
```
