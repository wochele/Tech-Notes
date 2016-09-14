# Get-Help

- `Help` is the same as `Get-Help` except it pipes the output to `More`
  - Press *CTL-C* to exit from the pagination of the help and return to the command line
- `Get-Help | More` = `Help`
- `Get-Help` parameters
  - `-Name` is the first positional parameter which accepts wildcards
    - `Help *log*` will list all the commands available with log in the name
    - Will include all extensions not loaded into memory too

