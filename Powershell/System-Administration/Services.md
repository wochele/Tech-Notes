# Services

### Check the status of the service

> get-service –ComputerName <server_name> <service_name>

Ex> get-service –ComputerName mi-mke-srvteam1 PatrolAgent

### Restart the service

> get-service –ComputerName <server_name> <service_name> | restart-service [-Verbose]

Ex> get-service –ComputerName mi-mke-srvteam1 PatrolAgent | restart-service [-Verbose]

If the command is successful, you will not get any feedback unless you add –Verbose.
