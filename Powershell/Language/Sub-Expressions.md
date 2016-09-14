# Sub-Expressions

Use sub-expressions within text to make sure it's parsed correctly

```powershell
$statusbar1.Text = "$($ComputerName): $($_.Exception.Message)"
```
