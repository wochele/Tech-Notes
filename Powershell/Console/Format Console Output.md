# Format Console Output

##### Format columns as close together as possible

```powershell
Get-PSDrive -PSProvider FileSystem | select name, root | Format-Table -AutoSize
```

