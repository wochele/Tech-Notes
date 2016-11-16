# Updating Help

Powershell does not include the complete powershell help system, so it must be downloaded to a system

- Help files are stored in the `System32` folder.

- Run `Update-Help` as administrator to download the help files onto the system. Run regularly to keep it updated. 
- Run `Save-Help` to get a local copy of the help which can be placed on the network
- Run `Update-Help -Source ` to download the local network copy 
