# Usage

### Remove All Characters Before Backslash

[Regex to remove what ever comes in front of “\” using powershell](http://stackoverflow.com/questions/16694662/regex-to-remove-what-ever-comes-in-front-of-using-powershell)

```powershell
$result = $subject -creplace '^[^\\]*\\', ''
```



