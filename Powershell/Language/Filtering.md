# Filtering

#### Filter Left

- Filter toward the beginning of the command line as much as possible

#### `Where-Object` or alias `Where`

- Filter any kind of object in the pipeline
- `Get-Service | Where-Object -filter { $_.Status -eq 'Running' }`
    - is equal to `Get-Service | Where { $_.Status -eq 'Running' }`
- For a single comparison, there is a simplified syntax
    - `Get-Service | Where Status -eq 'Running'`

#### `$_` placeholder

- Contains one object at a time from the ones piped into that cmdlet
