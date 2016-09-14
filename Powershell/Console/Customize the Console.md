# Customize the Console

### Add the following modules

- [PSReadline](https://github.com/lzybkr/PSReadLine)
- [Posh-Git](https://github.com/dahlbyk/posh-git)

### Resize the Console

```powershell
$pshost = Get-Host              # Get the PowerShell Host.
$pswindow = $pshost.UI.RawUI    # Get the PowerShell Host's UI.

$newsize = $pswindow.BufferSize # Get the UI's current Buffer Size.
$newsize.width = 250            # Set the new buffer's width to 150 columns.
$newsize.height = 3000
$pswindow.buffersize = $newsize # Set the new Buffer Size as active.

$newsize = $pswindow.windowsize # Get the UI's current Window Size.
$newsize.width = 250            # Set the new Window Width to 150 columns.
$newsize.height = 90
$pswindow.windowsize = $newsize # Set the new Window Size as active.
```

**NOTE** the window size cannot be larger than the buffer size



