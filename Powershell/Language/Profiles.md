# Profiles

### Profile Paths

Description | Path
------------|-----
Current User, Current Host - console | $Home\[My ]Documents\WindowsPowerShell\Profile.ps1
Current User, All Hosts   | $Home\[My ]Documents\Profile.ps1
All Users, Current Host - console   | $PsHome\Microsoft.PowerShell_profile.ps1
All Users, All Hosts      | $PsHome\Profile.ps1
Current user, Current Host - ISE | $Home\[My ]Documents\WindowsPowerShell\Microsoft.P owerShellISE_profile.ps1
All users, Current Host - ISE  | $PsHome\Microsoft.PowerShellISE_profile.ps1
<br>
- [Understanding the Six PowerShell Profiles](http://blogs.technet.com/b/heyscriptingguy/archive/2012/05/21/understanding-the-six-powershell-profiles.aspx)

### Include in profile

```powershell
Set-Location C:\ScriptRepo
$env:PSModulePath = "C:\ScriptRepo\Modules;" + $env:PSModulePath

if ($host.Name -eq 'ConsoleHost')
{
	Import-Module PSReadline
	Import-Module Posh-git
}

# Set Aliases -------------------------------------------------------------------------------------

# Push - Pop folder locations
# http://suhinini.blogspot.com/2010/03/using-push-location-and-pop-location-in.html

Set-Alias pd pushd
Set-Alias ppd popd

# Custom functions --------------------------------------------------------------------------------

function gd
{
	Get-PSDrive -PSProvider FileSystem
}

```

