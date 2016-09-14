# Drive Administration

### Create a persistent drive

Use `New-PSDrive` with the `-Persist` parameter to create drives which are visible in the file explorer

#### PSDrive

- A PSDrive is a single provider to connect to data storage (disks and a whole lot more)
- Can map to a file system, registry, certificate store
- Objects in PSDrives are referred to as "items" to encompass the many types of providers
- cmdlets are intentionally generic to work with a variety of data stores
