# Powershell and PHP

### Links

- [Executing PowerShell using PHP and IIS](http://theboywonder.co.uk/2012/07/29/executing-powershell-using-php-and-iis/)
- [jQuery getJSON from PowerShell via PHP on IIS: A Frustrating Gotcha](https://jthiede.wordpress.com/2013/10/01/jquery-getjson-from-powershell-via-php-on-iis-a-frustrating-gotcha/)
- [executing a Powershell script from php](http://stackoverflow.com/questions/5317315/executing-a-powershell-script-from-php)

### Use `shell_exec()`

- Will return the output of the script as a string
- Returns ALL output, so keep script silent with try/catch blocks
- Need `< NUL` to pass info to PHP and not have it wait and wait

```powershell
shell_exec(“powershell -NoProfile -File $scriptPath $argString < NUL”)

shell_exec(“powershell -NoProfile -File C:\web\script1.ps1 -User jdoe < NUL”)
```

- May need to `-ExecutionPolicy` if necessary

# IIS

- **Basic with HTTPS** - each page runs as the authenticated user and their permissions
- Install with the following:
  - CGI
  - Basic Authentication
  - Recommended: URL authorization (if you want to limit access to particular Active Directory users or groups).
  - Optional: IP and Domain Restrictions (if you want to limit access to a particular IP range on your LAN).
  - Install any Windows patches that may be needed by adding IIS to your server.

# Return JSON

# Powershell 

```powershell
#*=============================================================================
#* INITIALISE VARIABLES
#*=============================================================================
# Increase buffer width/height to avoid PowerShell from wrapping the text before
# sending it back to PHP (this results in weird spaces).
$pshost = Get-Host
$pswindow = $pshost.ui.rawui
$newsize = $pswindow.buffersize
$newsize.height = 3000
$newsize.width = 400
$pswindow.buffersize = $newsize
```

