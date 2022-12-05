
#### First test using test-netconnection inside the function

```powershell
 measure-command  {start-covsoftwareSearch -ComputerName (Get-Adcomputer -filter 'name -like "int*"').name | where displayname -like 'teams*'}
```

#### Run time was 4:02

