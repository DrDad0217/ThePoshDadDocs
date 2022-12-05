
## Example

Installed **Avaya One-X Communicator**

```Powershell
Invoke-Command -ComputerName INT012055t -ScriptBlock {
Start-Process "C:\Support\Downloads\Avaya One-X Communicator\Avaya one-X Communicator Suite.exe" -ArgumentList '/silent' -Wait }
```

- Used the **Silent** Argument to stop any interactive dialog boxes from coming up
- Used the **Wait** Argument to ensure the remote session stays live until the install is done

Source **Kevin Marquette**

[Powershell: Remote install software (powershellexplained.com)](https://powershellexplained.com/2017-04-22-Powershell-installing-remote-software/)
