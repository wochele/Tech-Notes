# Using ConsoleZ with Powershell

- Download from [ConsoleZ download wiki page](https://github.com/cbucher/console/wiki/Downloads)
- Copy files from .zip to folder on system, launch `Console.exe`, pin to task bar
- Customize settings
  - Change buffer to maximum of 32766
  - Change font to **Lucida Console** with a size of 10
  - menu > View > Toolbar off
  - menu > View > Status Bar off
  - menu > View > Tabs on
  - Add Powershell tab
    - menu > Edit > Settings > Tabs > Add
    - Add a new tab and set the Title: to PowerShell.
    - Set the Shell: value to %SystemRoot%\system32\WindowsPowerShell\v1.0\powershell.exe
    - Set the Icon: to use that same file path.
    - Set to run as administrator
    - Move the Powershell tab to the top of the list
- `CTL`+`F1` will open a new Powershell tab
  
More info - [Make the Windows Command Prompt, Linux-like](https://devtidbits.com/2014/05/21/create-a-better-windows-command-line-prompt/)
