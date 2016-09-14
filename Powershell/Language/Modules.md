# Modules

- List installed modules with `Get-Module`
- Use `Import-Module` to import a module not reference in $PSModulePath

### Create a module

- Create folder in modules folder for the module (use letters, numbers, underscores)
  - Folder is the module - easy to distribute
- Must be accessible through $PSModulePath or will have to be loaded manually
- Name of the file must match the name of the folder
- Save script file with a .psm1 extension
- Adding a module manifest
  - Use the .psd1 extension
  - Use same name as the folder
  - Use New-ModuleManifest to create
  
### Manually importing a module
```powershell
Import-Module -Name c:\path\ModuleName.psd1
```

### Add Module to System Path

```powershell
$p = [Environment]::GetEnvironmentVariable("PSModulePath")
$p += ";C:\Program Files\ WindowsPowerShell \Modules\"
[Environment]::SetEnvironmentVariable("PSModulePath",$p)
```

### Find Module Path

```powershell
$env:PSModulePath
```

### Modify Module Path

Edit the `PSModulePath` registry key to change the path for the machine


